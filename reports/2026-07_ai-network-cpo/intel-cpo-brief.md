# 인텔(Intel) CPO/광 집적 동향 — 리서치 브리프

> 목적: 인텔의 CPO·광 집적 위치를 정확히 정리(과장·오해 제거) — 워드 최종본용 재료
> 작성일 2026-07-30 · 리서치 기준일 2026-07-30
> 상위: [`foundry-packaging-brief.md`](foundry-packaging-brief.md) / 본편 [`report.md`](report.md)

## TL;DR
- 인텔은 **광 집적(실리콘 포토닉스) 원천기술·자체 팹을 보유**하나, **"남의 CPO를 만들어주는 파운드리"로는 약체** — TSMC·삼성(·GF) 대비 뒤처짐.
- **가장 최신 소식 = 유리기판(glass substrate) + CPO 시제품**(OFC 2026), 상용 **~2029~2030(인텔: "10년 후반")**.
- 연산용 광 I/O **OCI는 2024 시연 이후 2년째 프로토타입** — 양산·상용일·탑재 제품 **없음**.

## 3개 트랙으로 본 인텔 CPO
| 트랙 | 내용 | 상태 |
|------|------|------|
| **① 스위치용 CPO** | 과거 Tofino 스위치에 실리콘 포토닉스 통합 시연 | **'23.1 스위치 사업(Barefoot/Tofino) 철수 → 노선 소멸** |
| **② 연산용 CPO(광 I/O·OCI)** | 광 엔진을 연산칩에 직접 결합(스케일업 광 연결) | **프로토타입** (4Tbps 시연, 양산·상용일 없음) |
| **③ 유리기판 + CPO** | 유리기판 위에 광반도체 직접 집적(차세대 패키징) | **시제품(OFC 2026), 상용 ~2030** ← 최신 |

## 핵심 팩트 / 수치
- **OCI(연산용)**: OFC 2024 세계 첫 완전통합 광 I/O 칩렛 시연 — **4Tbps 양방향**, PCIe Gen5, **5pJ/bit**(플러거블 약 15의 1/3), 온칩 DWDM 레이저·SOA 내장(외부 레이저 불필요). 단일 PIC **최대 8Tbps 지원 '역량'** 서술.
- **원천기술**: 온칩 레이저·광증폭기를 광칩에 직접 집적하는 실리콘 포토닉스(외부 레이저 불필요) — 과거 광 트랜시버로 **PIC 800만개+·온칩 레이저 3,200만개+ 양산 이력**.
- **⚠️ 양산 사업은 매각**: 인텔은 **2023년 Q3 플러거블 광모듈 사업을 Jabil에 매각**(2023.11 완료) → **현재 광 부품을 양산·판매하지 않음.** 남긴 실리콘 포토닉스 기술·팹은 **OCI·CPO 연구개발용.** (즉 "양산 라인 가동 중"은 틀림 — 현재는 R&D 단계)
- **CPO/OCI 양산 여부**: ❌ 없음. 2024 데모의 결합 대상은 인텔 CPU였으나 **판매 제품 아님**(시연용). 어떤 Xeon/Gaudi에도 미탑재.
- **유리기판**: EMIB+유리 샘플('26.1), 유리+CPO 시제품(OFC 2026), 美 Rio Rancho 양산 추진 보도, 광반도체 외부 고객 공급(파운드리) 시작 보도.
- **경쟁 환경**: 가속기측 광 I/O(OCI) 범주의 대표주자는 **Ayar Labs**(엔비디아·AMD 투자), Lightmatter도 경쟁 → 인텔은 이 범주의 여러 구현 중 하나.

## 정정·주의 (오해 방지 — 근거 없어 쓰지 말 것)
- ❌ **"OCI 상용 = 2030"** — 2030은 **유리기판** 트랙 시점. OCI 단독 상용일은 미정.
- ❌ **"SC25에서 8Tbps 실증"** — 확인 안 됨. 8Tbps는 PIC의 **역량(ceiling)** 서술, 시연 수치는 **4Tbps**.
- ❌ **"Q2 2026 하이퍼스케일러 공급 협의"** — 약한 출처(철회). 공식은 "일부 고객 협업"까지.
- ❌ **"스위치 안 거치는 게 인텔 차별점"** — 스위치리스는 **가속기측 광 I/O 방식 전체**의 특성(Ayar Labs·Lightmatter 동일), 인텔 고유 아님.
- ❌ **"유리기판은 인텔만의 강점"** — 업계 공통 경쟁(SK Absolics·삼성전기가 오히려 앞섬). 인텔은 유리기판 상용 시점 **최후발**.

## 포지션 판단
- "TSMC·삼성·**인텔**"은 **로직 파운드리 3강** 프레임에서 온 것 — **CPO(광반도체) 지형은 주자가 다름**.
- CPO 제조 기준 실질 3강 = **TSMC·삼성·GlobalFoundries**(GF가 팹리스 광기업 실제 제조). 인텔은 여기서 **약체**.
- 인텔을 넣을 명분 = ①광반도체 원천기술·자체 팹, ②미국 대표·지정학(정부 지분·CHIPS), ③유리기판 등 차세대 패키징 first-mover → 단 "**현재 CPO 수주 경쟁자**"가 아니라 "**역량 보유·개발/잠재 단계**".

## 워드용 한 줄 표현 (권장)
> "인텔은 광 집적 원천기술과 유리기판 등 차세대 패키징을 보유하나, 스위치 CPO는 철수했고 연산용 광 I/O(OCI)는 아직 시연 단계 — CPO 제조 사업화는 3사 중 가장 뒤처져 '잠재 참가자'에 가깝다."

## 출처 (등급)
- **1급(공식)**: Intel Newsroom, "First Fully Integrated Optical I/O Chiplet", https://newsroom.intel.com/artificial-intelligence/intel-unveils-first-integrated-optical-io-chiplet / Intel 실리콘 포토닉스 제품페이지 https://www.intel.com/content/www/us/en/products/details/network-io/silicon-photonics.html
- **1급(공식)**: Intel Newsroom, "Industry-Leading Glass Substrates" (2023), https://newsroom.intel.com/artificial-intelligence/intel-unveils-industry-leading-glass-substrates
- **2급(trade)**: Tom's Hardware(Barefoot/Tofino 철수) https://www.tomshardware.com/news/intel-sunsets-network-switch-biz-kills-risc-v-pathfinder-program / HPCwire(OCI) / TrendForce(유리기판·Rio Rancho, 2026.05) https://www.trendforce.com/news/2026/05/26/news-intel-reportedly-eyes-worlds-first-glass-substrate-output-at-rio-rancho-offers-silicon-photonics-to-customers/
- **3급(주의·교차확인)**: ico-optics·wccftech(유리기판 "2030" 세부) → Intel 공식 "10년 후반"으로 앵커 권장

> 주의: 인텔 광 사업은 발표·시연 위주라, 상용 시점·탑재 제품은 "미정/없음"이 현재 가장 정확한 표현.
