# 인텔(Intel) CPO/광 집적 동향 — 리서치 브리프

> 목적: 인텔의 CPO·광 집적 위치를 정확히 정리(과장·오해 제거) — 워드 최종본용 재료
> 작성일 2026-07-30 · 리서치 기준일 2026-07-30 · **개정 2026-08-03**(Rio Rancho 팹 현황 정정)
> 상위: [`foundry-packaging-brief.md`](foundry-packaging-brief.md) / 본편 [`report.md`](report.md)

## TL;DR
- 인텔은 **광 집적(실리콘 포토닉스) 원천기술·자체 팹(Rio Rancho)을 보유·운영**하며, **2026년 외부 고객에 SiPh 파운드리 제조를 제공하기 시작** — 단 "남의 CPO 대량 수주"로는 아직 **초기 진입**(TSMC·삼성·GF 대비 후발).
- **가장 최신 소식 = 유리기판(glass substrate) + CPO 시제품**(OFC 2026), 상용 **~2029~2030(인텔: "10년 후반")**. Rio Rancho를 **유리기판 세계 첫 양산 허브**로 추진.
- 다만 **자사 연산용 광 I/O(OCI) '완제품'은 2024 시연 이후 프로토타입** — 양산·탑재 제품 **없음**.

## 3개 트랙으로 본 인텔 CPO
| 트랙 | 내용 | 상태 |
|------|------|------|
| **① 스위치용 CPO** | 과거 Tofino 스위치에 실리콘 포토닉스 통합 시연 | **'23.1 스위치 사업(Barefoot/Tofino) 철수 → 노선 소멸** |
| **② 연산용 CPO(광 I/O·OCI)** | 광 엔진을 연산칩에 직접 결합(스케일업 광 연결) | **프로토타입** (4Tbps 시연, 양산·상용일 없음) |
| **③ 유리기판 + CPO** | 유리기판 위에 광반도체 직접 집적(차세대 패키징) | **시제품(OFC 2026), 상용 ~2030** ← 최신 |

## 핵심 팩트 / 수치
- **OCI(연산용)**: OFC 2024 세계 첫 완전통합 광 I/O 칩렛 시연 — **4Tbps 양방향**, PCIe Gen5, **5pJ/bit**(플러거블 약 15의 1/3), 온칩 DWDM 레이저·SOA 내장(외부 레이저 불필요). 단일 PIC **최대 8Tbps 지원 '역량'** 서술.
- **원천기술·팹**: 온칩 레이저·광증폭기를 광칩에 직접 집적하는 실리콘 포토닉스(외부 레이저 불필요, 하이브리드 III-V/Si) — 과거 트랜시버로 **PIC 800만개+·온칩 레이저 3,200만개+ 양산 이력('16~)**. **Rio Rancho 팹(Fab 9 '24.1 개소·$3.5B + Fab 11X) 운영 중 — EMIB·실리콘 포토닉스 제조.**
- **⚠️ 매각한 건 '제품 사업'이지 'PIC 기술/팹'이 아님**: 2023년 Q3 **플러거블 트랜시버 '완제품' 사업을 Jabil에 매각**(2023.11) → 그 제품군은 Jabil 소관. 단 **핵심 PIC·레이저 기술과 팹은 인텔이 보유·운영**(고부가 컴포넌트·OCI·유리기판용).
- **✅ 2026년 SiPh 파운드리 진입**: Rio Rancho에서 **외부 고객에 실리콘 포토닉스 제조 서비스 제공을 시작**(초기 단계) → "남의 것을 만들어주는" 파운드리에 발을 들임.
- **자사 OCI '완제품'은 프로토타입**: 2024 데모(인텔 CPU 결합)는 시연용, **판매 제품 아님**(Xeon/Gaudi 미탑재). 양산 아님.
- **유리기판**: EMIB+유리코어 샘플('26.1), 유리+CPO 시제품(OFC 2026), Rio Rancho를 **유리기판 세계 첫 양산 사이트**로 추진.
- **경쟁 환경**: 가속기측 광 I/O(OCI) 범주의 대표주자는 **Ayar Labs**(엔비디아·AMD 투자), Lightmatter도 경쟁 → 인텔은 이 범주의 여러 구현 중 하나.

## 정정·주의 (오해 방지 — 근거 없어 쓰지 말 것)
- ⚠️ **(개정)** "인텔 광 양산 전무·완전 R&D 단계"는 **과장** — Rio Rancho 팹은 **SiPh 제조 중이고 2026년 외부 파운드리 제공을 시작**함. 다만 **'자사 OCI 완제품'은 프로토타입**. → "팹·SiPh 제조 O / 자사 완제품 X"로 구분할 것.
- ❌ **"인텔이 PIC 기술/공정을 팔았다"** — 매각한 건 **트랜시버 '완제품' 사업(Jabil)**, PIC·레이저 **기술·팹은 인텔이 보유·운영** 중.
- ❌ **"OCI 상용 = 2030"** — 2030은 **유리기판** 트랙 시점. OCI 단독 상용일은 미정.
- ❌ **"SC25에서 8Tbps 실증"** — 확인 안 됨. 8Tbps는 PIC의 **역량(ceiling)** 서술, 시연 수치는 **4Tbps**.
- ❌ **"Q2 2026 하이퍼스케일러 공급 협의"** — 약한 출처(철회). 공식은 "일부 고객 협업"까지.
- ❌ **"스위치 안 거치는 게 인텔 차별점"** — 스위치리스는 **가속기측 광 I/O 방식 전체**의 특성(Ayar Labs·Lightmatter 동일), 인텔 고유 아님.
- ❌ **"유리기판은 인텔만의 강점"** — 업계 공통 경쟁(SK Absolics·삼성전기가 오히려 앞섬). 인텔은 유리기판 상용 시점 **최후발**.

## 포지션 판단
- "TSMC·삼성·**인텔**"은 **로직 파운드리 3강** 프레임에서 온 것 — **CPO(광반도체) 지형은 주자가 다름**.
- CPO 제조 기준 실질 선두 = **TSMC·삼성·GlobalFoundries**(GF가 팹리스 광기업 실제 양산). 인텔은 **후발이나 "잠재 참가자"에서 "초기 진입자"로 이동 중** — Rio Rancho SiPh 파운드리 제공 시작 + 유리기판 양산 허브 추진.
- 단, **규모·수주 실적은 TSMC·GF에 크게 못 미침(초기)**, 자사 OCI 완제품은 프로토타입.
- 인텔의 명분 = ①광반도체 원천기술·자체 팹(운영 중), ②미국 대표·지정학(정부 지분·CHIPS·Rio Rancho 허브), ③유리기판 등 차세대 패키징 first-mover.

## 워드용 한 줄 표현 (권장)
> "인텔은 광 집적 원천기술·자체 팹(Rio Rancho)을 보유·운영하며 2026년 SiPh 파운드리 제공·유리기판 양산을 추진하나, 자사 광 I/O(OCI) 완제품은 아직 프로토타입 — CPO 제조에선 TSMC·삼성·GF 대비 초기 진입 단계."

## 출처 (등급)
- **1급(공식)**: Intel Newsroom, "First Fully Integrated Optical I/O Chiplet", https://newsroom.intel.com/artificial-intelligence/intel-unveils-first-integrated-optical-io-chiplet / Intel 실리콘 포토닉스 제품페이지 https://www.intel.com/content/www/us/en/products/details/network-io/silicon-photonics.html
- **1급(공식)**: Intel Newsroom, "Industry-Leading Glass Substrates" (2023), https://newsroom.intel.com/artificial-intelligence/intel-unveils-industry-leading-glass-substrates
- **1급(공식)**: Intel Newsroom, "Intel Opens Fab 9 in New Mexico"(Rio Rancho 첨단 패키징 팹), https://newsroom.intel.com/intel-foundry/intel-opens-fab-9-in-new-mexico
- **2급(trade)**: Tom's Hardware(Barefoot/Tofino 철수) https://www.tomshardware.com/news/intel-sunsets-network-switch-biz-kills-risc-v-pathfinder-program / The Register(Jabil 매각 범위, 2023.10) https://www.theregister.com/2023/10/31/intel_silicon_photonics_jabil/ / ServeTheHome(Jabil 매각) / TrendForce(유리기판·Rio Rancho SiPh 파운드리 제공, 2026.05) https://www.trendforce.com/news/2026/05/26/news-intel-reportedly-eyes-worlds-first-glass-substrate-output-at-rio-rancho-offers-silicon-photonics-to-customers/ / Digitimes(Rio Rancho CPO 테스트케이스, 2026.05) https://www.digitimes.com/news/a20260526PD225/intel-packaging-advanced-process-technology-cpo.html
- **3급(주의·교차확인)**: ico-optics·wccftech(유리기판 "2030" 세부) → Intel 공식 "10년 후반"으로 앵커 권장

> 주의: 인텔은 **팹·SiPh 제조는 진행**하나 **자사 광 완제품(OCI)은 프로토타입** — "팹·파운드리 제공 O / 자사 완제품 X"로 구분해 표기해야 정확. Rio Rancho의 SiPh 파운드리·유리기판 양산은 "초기·추진 중" 단계로, 규모는 미미.
