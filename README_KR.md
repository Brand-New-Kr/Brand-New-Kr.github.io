# Fig. 4 (261027) Windows cp949 hotfix / resumed Python stages

## 무엇이 실제로 완료됐나?

사용자 RStudio 로그에 따르면 01_import_SRS, 02_diversity, 02B_family_overlap, 03_figures, 04_tables가 **모두 PASS**.
Python QC 또한 7개 내부 검사 각각 PASS. 오류는 마지막 `Fig4_numeric_QC.json` 저장 시 기본 인코딩이 `cp949`여서 en dash (`–`)를 출력할 수 없어서 발생했음.
따라서 R 전처리, alpha/beta diversity, UpSet, Tables를 **재실행하지 말 것**.

## 기존 프로젝트에 설치

아래의 3개 `.py` 파일을 동일한 이름으로 기존 `R_pipeline_ET_amplicon_261027` 안에 덮어쓰고, `08_resume_Fig4.R`을 새로 추가:

- `05_Fig4.py`: R-generated `verification.json`을 명시적 UTF-8로 읽음. 시각화 로직 그대로.
- `06_validate_Fig4.py`: QC JSON 파일을 명시적 UTF-8로 기록. 검사 로직 그대로.
- `07_provenance_manifest.py`: Python environment JSON을 명시적 UTF-8로 기록. SHA256 로직 그대로.
- `08_resume_Fig4.R`: 06 QC -> 05 Figure -> 07 SHA256만 실행하는 재개용 코드.

나머지 `00_config.R`, `00_run_all.R`, Rmd 파일, 이미 생성된 `ET_amplicon_R_outputs_261027` 파일은 절대 건드리지 않음.

## 실행

RStudio에서 새 파이프라인 폴더의 `08_resume_Fig4.R`을 열어 `Source` 클릭.
`00_run_all.R`을 **다시 실행하면 안 됨**. 기존 코드에는 261027 output이 이미 존재하면 중단하는 보호 장치가 있음.

재개 코드에는 `PYTHONUTF8=1` 설정이 추가되어 Windows 기본 인코딩 문제를 예방함.

## 최종 결과 확인

```
01_Amplicon_DNA/ET_amplicon_R_outputs_261027/
  figures/Fig4/Final_Python/
    Fig4_numeric_QC.json       # "all_pass": true
    Fig4_final.png
    Fig4_final.pdf
    Fig4_final.svg
    Fig4_final_preview.png
  SHA256_MANIFEST_261027.tsv
  PYTHON_ENVIRONMENT_261027.json
```

## 재현성에 대한 정직한 구분

- 현재의 7 PASS는 서식/입력 정합성 + UpSet 검증이지, 기존 원고의 모든 diversity 통계 숫자와 독립적으로 수치 일치 비교했다는 뜻은 아님.
- `RUN_PROVENANCE_261027.txt`, 원본 R-generated CSV, Rmd output, Fig. 4 and manifest를 함께 동결해야 함.
- 이 패치는 분석 수치, 생태학적 해석, figure design을 전혀 변경하지 않음.

## 이 패치 자체의 로컬 시험

- Python 세 파일 문법 검사 통과.
- 이전에 보관된 참조 Figure CSV 사본으로 06 -> 05 -> 07을 순서대로 실행, 7 PASS, Fig4_final PNG/PDF/SVG, manifest 생성 확인. 테스트용 참조 sample manifest에는 최신 스키마의 `substrate` 열이 없어 테스트용 CSV에 그 열만 채워 검증함.
- 사용자의 실제 Windows RStudio에서의 재개 실행은 아직 별도 확인 전임.
