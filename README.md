# supply — AI 인프라·반도체 기술 동향 리포트

AI 인프라 및 반도체 공급망(supply) 관련 기술 동향을 정리하는 리포트 저장소입니다.
보고서 주제가 확장될 것을 전제로, 리포트/리서치/템플릿을 분리한 폴더 구조를 사용합니다.

## 폴더 구조

```
supply/
├── README.md                     # 본 문서 — 저장소 개요 및 리포트 인덱스
├── reports/                      # 완성된 보고서 (주제별 폴더)
│   └── 2026-07_ai-network-cpo/   # AI 네트워크(칩 간 데이터 전송) — CPO 중심
│       ├── report.md             #   └ 본문
│       ├── summary.md            #   └ 1페이지 요약(경영진용)
│       └── assets/               #   └ 도표·다이어그램·이미지
├── research/                     # 리서치 노트·원자료 (보고서 주제별)
│   └── ai-network-cpo/
│       └── sources.md            # 출처 목록 및 핵심 수치 메모
└── templates/
    └── report-template.md        # 신규 보고서 작성용 템플릿
```

### 폴더 운영 원칙

- **`reports/`** : 발행 단위의 완성 문서. 폴더명은 `YYYY-MM_슬러그` 규칙(예: `2026-07_ai-network-cpo`)으로 시간순 정렬과 주제 식별을 동시에 만족.
- **`research/`** : 보고서별 원자료·출처·메모. 보고서 폴더와 슬러그를 맞춰 1:1 대응.
- **`templates/`** : 신규 보고서는 `templates/report-template.md`를 복사해 시작.
- 이미지·도표 등 바이너리/에셋은 각 보고서의 `assets/`에만 둔다.

## 리포트 인덱스

| 발행 | 주제 | 핵심 | 위치 |
|------|------|------|------|
| 2026-07 | AI 네트워크(칩 간 데이터 전송) 기술 동향 | CPO(Co-Packaged Optics) 도입 | [reports/2026-07_ai-network-cpo](reports/2026-07_ai-network-cpo/report.md) |
