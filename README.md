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
│   │   ├── nvidia-supply-chain-investments.md  # └ 부록: 엔비디아 CPO 공급망 투자 정리
│   │   ├── broadcom-brief.md      #   └ 브리프: 브로드컴(개방 진영) CPO·AI 네트워킹
│   │   ├── foundry-packaging-brief.md  # └ 브리프: 제조/패키징 진영(TSMC·삼성·GF·인텔)+유리기판
│   │   ├── intel-cpo-brief.md     #   └ 브리프: 인텔 CPO/광 집적 상세(OCI·유리기판·정정목록)
│   │   ├── gf-cpo-brief.md        #   └ 브리프: 글로벌파운드리스 CPO/실리콘 포토닉스 상세
│   │   ├── glass-substrate-brief.md  # └ 브리프: 유리기판 자체 vs 협력(인텔·TSMC·삼성전기·GF)
│   │   └── assets/               #   └ 도표·다이어그램·이미지
│   └── 2026-07_datacenter-cpo-stocks/  # CPO 도입과 데이터센터 관련주 영향
│       ├── report.md             #   └ 본문 (밸류체인별 관련주·티커·영향)
│       ├── summary.md            #   └ 1페이지 요약
│       └── assets/
├── research/                     # 리서치 노트·원자료 (보고서 주제별)
│   └── ai-network-cpo/
│       └── sources.md            # 출처 목록 및 핵심 수치 메모
└── templates/
    ├── report-template.md          # 완성형 보고서 템플릿
    └── research-brief-template.md   # 리서치 브리프 템플릿 (기본)
```

### 산출물 형식 (기본: 리서치 브리프)

최종본은 워드(Word)에서 직접 작성하므로, 이 레포의 기본 산출물은 **리서치 브리프**다 —
산문을 최소화하고 **요점·표·수치·출처** 중심으로 정리해 워드에 옮기기 좋게 한다.
템플릿: `templates/research-brief-template.md`.
(완성형 산문 보고서가 필요할 때만 `report-template.md` 사용. 기존 `2026-07_*` 2건은 완성형 참고자료.)

### 폴더 운영 원칙

- **`reports/`** : 주제별 산출물. 폴더명은 `YYYY-MM_슬러그` 규칙(예: `2026-07_ai-network-cpo`)으로 시간순 정렬과 주제 식별을 동시에 만족.
- **`research/`** : 보고서별 원자료·출처·메모. 보고서 폴더와 슬러그를 맞춰 1:1 대응.
- **`templates/`** : 신규 작업은 `research-brief-template.md`(기본) 또는 `report-template.md`를 복사해 시작.
- 이미지·도표 등 바이너리/에셋은 각 보고서의 `assets/`에만 둔다.

## 리포트 인덱스

| 발행 | 주제 | 핵심 | 위치 |
|------|------|------|------|
| 2026-07 | AI 네트워크(칩 간 데이터 전송) 기술 동향 | CPO(Co-Packaged Optics) 도입 | [reports/2026-07_ai-network-cpo](reports/2026-07_ai-network-cpo/report.md) |
| 2026-07 | CPO 도입과 데이터센터 관련주 영향 | 밸류체인별 관련주·티커 매핑 | [reports/2026-07_datacenter-cpo-stocks](reports/2026-07_datacenter-cpo-stocks/report.md) |
