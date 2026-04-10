# PDF to Markdown Conversion Sample

한국어 PDF 문서에 대한 다양한 PDF-to-Markdown 변환 도구 비교 샘플입니다.

## 원본

- `original/` — 원본 PDF (2026년 예산안 홍보자료, 65페이지)

## 변환 결과

| 폴더 | 도구 | 설정 |
|---|---|---|
| `markitdown/` | [markitdown](https://github.com/microsoft/markitdown) | pdfminer 기반 텍스트 추출 |
| `mineru-hybrid-zh/` | [MinerU](https://github.com/opendatalab/MinerU) v3.0.8 | hybrid-auto-engine, lang=ch (기본값) |
| `mineru-hybrid-ko/` | [MinerU](https://github.com/opendatalab/MinerU) v3.0.8 | hybrid-auto-engine, lang=korean |

## 참고

- MinerU hybrid 모드는 VLM(Qwen2VL 1.2B) + 전통 OCR/Layout 조합
- 한국어 표(table) 추출 시 VLM 모델의 한계로 텍스트 오인식 발생
- markitdown은 텍스트 기반 PDF에서 더 깨끗한 결과를 보여줌
