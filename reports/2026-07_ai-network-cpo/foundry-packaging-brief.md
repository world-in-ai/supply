# CPO 제조/패키징 진영 — 파운드리 4사 + 유리기판 — 리서치 브리프

> 목적: CPO "제조/패키징" 축(설계 진영과 대비) 정리 — 워드 최종본용 재료
> 작성일 2026-07-30 · 리서치 기준일 2026-07-30
> 짝 문서: 설계 진영 = [`broadcom-brief.md`](broadcom-brief.md)·[`nvidia-supply-chain-investments.md`](nvidia-supply-chain-investments.md) / 본편 [`report.md`](report.md)

## TL;DR
- CPO 제조 경쟁 = **①광엔진(광반도체) 제조 + ②로직과의 집적(첨단 패키징)** 두 역량 싸움. (CPO = Co-Packaged = 로직 옆에 광엔진을 붙이는 것)
- **TSMC 선두**(COUPE+CoWoS, '26 양산, 엔비디아·브로드컴 채택) → **삼성 추격**(광반도체 파운드리 진입, 턴키 CPO '29) → **GF 광반도체 전문**(팹리스 광기업 제조) → **인텔 원천기술 보유하나 상용 최후발**.
- **유리기판**은 인텔 전유물이 아니라 **업계 공통 차세대 과제**(SK·삼성전기 선도, TSMC 신중, 인텔 최후발).

## 핵심 팩트 / 수치
| 업체 | 성격 | 핵심 현황 | CPO 상용 시점 |
|------|------|-----------|---------------|
| **TSMC** | 종합 파운드리 (선두) | 광엔진 공정 **COUPE** + 첨단패키징 **CoWoS** 연계, 엔비디아·브로드컴 채택 | **'26 양산** |
| **삼성전자** | 종합 파운드리 (추격) | 광반도체 파운드리 공식화(OFC 2026)·PDK 완비, 메모리(HBM) 턴키 차별화 | 턴키 CPO **'29** |
| **GlobalFoundries** | 광반도체 전문 파운드리 | **GF Fotonix**로 Ayar Labs·Lightmatter 등 팹리스 광기업 제조, AMF 인수('25.11) → 상세 [`gf-cpo-brief.md`](gf-cpo-brief.md) | **PIC 2018~ 양산 중**(광엔진 SCALE '26.5) / CPO 양산 시점은 GF 공식 미발표(보도만 '28말~'29) |
| **인텔** | IDM (원천기술 보유) | 광 집적 원천기술·**Rio Rancho 팹 운영**(SiPh 제조), '23년 광모듈 사업 매각(팹·기술 보유) | 자사 OCI는 프로토타입·유리기판 '10년 후반·외부 SiPh 파운드리는 미확정(보도) |

### 삼성 로드맵 (5단계, OFC 2026 발표)
`'26 PIC(광반도체) → '27 광엔진(OE·TC본딩) → '28 HC본딩 패키징 → '29 턴키 CPO → '30 차세대 CPO`

### 인텔 세부 → 별도 상세: [`intel-cpo-brief.md`](intel-cpo-brief.md)
- 스위치용 CPO: 과거 Tofino 스위치에 실리콘 포토닉스 통합 시연했으나 **'23.1 스위치 사업(Barefoot/Tofino) 철수** → 노선 소멸
- '23년 **재정악화로 광모듈(트랜시버) 완제품 사업 Jabil 매각**(≠기술/팹 매각) — **PIC·레이저 기술·팹은 보유·운영**(Rio Rancho)
- 연산용 광 I/O(OCI) '완제품'은 OFC 2024 시연 후 **프로토타입**(양산·탑재 제품 없음)
- 유리기판+CPO: OFC 2026 시제품, 상용 **'10년 후반**(인텔 공식) ← 최신
- ❓ 외부 SiPh 파운드리 제공은 **일부 보도(TrendForce)뿐, 인텔 공식·원문 미확인** → 사실로 단정 금지
- ※ CPO 제조에선 **후발**(원천기술·팹은 보유, 외부 수주는 미확정). 상세·정정목록은 인텔 브리프 참조

## 유리기판(glass substrate) — 업계 공통 과제, 인텔 최후발
| 주체 | 성격 | 시점·근거 |
|------|------|-----------|
| **SK 엔펄스(Absolics)** | 기판 전문(SKC) | 선두 — 美 조지아 공장, '26 양산 목표, AMD 샘플 |
| **삼성전기(SEMCO)** | 기판 전문 계열사 | 공격적 — 스미토모/동우화인켐 JV, **2H27 양산**, 애플·브로드컴 샘플 |
| **TSMC** | 파운드리 | 신중 — 'CoWoS용 유리기판(CoPoS)', 파일럿 '27 → 양산 2H28 |
| **인텔** | IDM | 원조 발표('23)·EMIB+유리 샘플('26.1)·CPO 시제품('26), 상용 ~'30 |

> 층위 구분: 유리기판은 주로 **기판 전문사**(SK·삼성전기·이비덴)가 주도 → 광엔진(광반도체) 파운드리 경쟁과는 다른 층. 삼성은 **삼성전자(광반도체)+삼성전기(유리기판)** 그룹 커버가 강점.

## 논점별 요점
### 1. 두 레이어 (임원용 단순화)
- CPO 구현 = **광엔진 '만들고'(파운드리) + 로직과 '붙이기'(첨단 패키징)**
- TSMC 강점 = 이미 엔비디아·브로드컴 로직을 만드는 파운드리라, 광엔진·패키징까지 자연 연계

### 2. 3사(4사) 포지션 요약
- **TSMC**: 기술·수주 모두 선두, 이미 시장 주도 (CoWoS가 AI 가속기 표준 된 흐름 재현)
- **삼성**: 후발이나 메모리(HBM)·턴키로 추격, 상용은 TSMC 대비 약 3년 후
- **GF**: 선단 로직은 안 하나 광반도체 전문 — 팹리스 광기업(Ayar Labs 등) 실제 제조처 (엔비디아 공급망과 연결)
- **인텔**: 광 집적 원천기술은 앞서나, 스위치 CPO 철수·OCI 프로토타입·유리기판 최후발 → 상용 실행이 가장 늦음

### 3. 경쟁 구도
- **직접 경쟁**: TSMC ↔ 삼성 (같은 고객 두고 CPO 수주)
- **전문 참가**: GF (광엔진 제조 특화)
- **잠재/최후발**: 인텔 (역량 보유, 사업화 관건)

## 워드 작성용 목차 제안
1. 제조/패키징이 왜 관건인가 (광엔진 제조 + 로직 집적)
2. TSMC (선두) / 삼성 (추격) / GF (전문) / 인텔 (최후발)
3. 공통 과제: 유리기판 경쟁 (SK·삼성전기·TSMC·인텔)
4. 시사점: 설계 진영(엔비디아·브로드컴) 대비 제조 진영 판도

## 출처
1. TrendForce, "Silicon Photonics Race: TSMC 2026 COUPE / Samsung 2029 CPO Turnkey" (2026.04), https://www.trendforce.com/news/2026/04/01/news-silicon-photonics-race-intensifies-as-tsmc-targets-2026-coupe-production-samsung-eyes-2029-cpo-turnkey/
2. THE ELEC, "삼성 실리콘 포토닉스 파운드리 진출", https://www.thelec.kr/news/articleView.html?idxno=54279
3. Intel Newsroom, "Intel Demonstrates First Fully Integrated Optical I/O Chiplet" (OFC 2024), https://newsroom.intel.com/artificial-intelligence/intel-unveils-first-integrated-optical-io-chiplet
4. Tom's Hardware, "Intel Sunsets Network Switch Biz" (2023.01), https://www.tomshardware.com/news/intel-sunsets-network-switch-biz-kills-risc-v-pathfinder-program
5. Intel Newsroom, "Intel Unveils Industry-Leading Glass Substrates" (2023), https://newsroom.intel.com/artificial-intelligence/intel-unveils-industry-leading-glass-substrates
6. TrendForce, "Intel Eyes World's First Glass Substrate Output at Rio Rancho; Offers Silicon Photonics to Customers" (2026.05), https://www.trendforce.com/news/2026/05/26/news-intel-reportedly-eyes-worlds-first-glass-substrate-output-at-rio-rancho-offers-silicon-photonics-to-customers/
7. TrendForce, "Samsung Electro-Mechanics Glass Core JV with Sumitomo, 2H27 Production" (2026.07), https://www.trendforce.com/news/2026/07/06/news-samsung-electro-mechanics-reportedly-signs-deal-to-form-glass-core-jv-with-sumitomo-unit-targeting-2h27-production/
8. SemiAnalysis, "GlobalFoundries Fotonix, The Leading Silicon Photonics Foundry", https://newsletter.semianalysis.com/p/globalfoundries-fotonix-the-leading

> 주의: 시점·수치는 각 사 발표·언론 보도 기준. 유리기판 양산 시점은 파일럿/양산 기준이 뒤섞여 보도되므로 문맥별 확인 권장.
