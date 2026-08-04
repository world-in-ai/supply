# 유리기판(Glass Core Substrate) — 자체 vs 협력 축 — 리서치 브리프

> 목적: CPO 제조 4사(+삼성전기)의 유리기판 접근을 **"자체 개발 vs 타사 협력"** 축으로 정확히 정리 — 워드 최종본용 재료
> 작성일 2026-08-04 · 리서치 기준일 2026-08-04
> 상위: [`foundry-packaging-brief.md`](foundry-packaging-brief.md) / 본편 [`report.md`](report.md)

## TL;DR — 사용자 가정 정정
- **자체 개발은 Intel만** (종합 IDM 중 유일하게 유리코어를 직접 R&D). 단 **아직 프로토타입** — 상용은 "10년 후반~2030년대"(Clearwater Forest 탑재설은 오보).
- **TSMC는 "자체"가 아니라 협력** — Ibiden(ABF 기판)+Innolux(패널/유리 핸들링)와 **3사 검증**. TSMC 자체 몫은 CoPoS 패키징 통합.
- **삼성전자는 유리기판을 직접 안 함** → 계열사 **삼성전기(SEMCO)**가 담당하며, 그 삼성전기조차 **JV(GLASEM, +동우화인켐/스미토모)**로 진행 → 삼성전자 기준 **이중 외부**.
- **GF는 유리"기판(코어)" 경쟁에 아예 없음** — 유리 **도파관(GlassBridge, 광결합)**만 Corning과 협력(≠패키지 기판).

## 자체 vs 협력 — 한눈에
| 주체 | 유리기판(glass core substrate) 접근 | 판정 |
|------|--------------------------------------|------|
| **Intel** | **자체 R&D** — 미 챈들러(Arizona) 팹, 10년+·10억 달러+ 투자. 종합 IDM 중 유일하게 유리코어 직접 개발. **단 아직 프로토타입**(상용 '10년 후반~2030s) | **자체** ✅ |
| **TSMC** | **Ibiden(ABF 기판)+Innolux(패널) 3사 협력 검증**. TSMC "유리코어는 반드시 확보할 역량"이라며 협력으로 진행. 자체 강점은 CoPoS(패널레벨 패키징) 통합 | **협력** (자체 아님) ⚠️ |
| **삼성전자** | 유리기판 **직접 안 함** → 계열사 삼성전기가 담당 | **외부(계열사)** |
| **삼성전기(SEMCO)** | JV **GLASEM**(삼성전기 66% + 동우화인켐 34%)로 진행 — 삼성전기조차 타사 JV. **별도 상장사**(≠삼성전자) | **협력**(타사 JV) ✅ |
| **GlobalFoundries** | 유리**기판(코어)** 미참여. 유리 **도파관**(Corning 'GlassBridge', 광섬유↔PIC 결합)만 협력 | 유리기판 경쟁 **밖** |

> 사용자 가정("TSMC·인텔 자체 / 삼성전자·GF 협력")은 **절반만 맞음** → **Intel만 자체, TSMC도 협력**. 삼성전기는 지적대로 **타사(별도 상장사)**이며 그마저 JV.

## 주체별 상세

### Intel — 유일한 "자체" (but 프로토타입)
- **자체 개발**: 미 챈들러 팹에서 10년+·10억 달러+ 투자한 자사 R&D. 유리코어+EMIB 결합 샘플(NEPCON Japan '26.1), 유리+CPO 시제품(OFC 2026).
- **⚠️ 상용 시점 = "10년 후반"(인텔 공식) ~ 2030년대**. 콘텐츠팜이 "Xeon 6+ Clearwater Forest = 첫 유리코어 양산칩('26)"이라 주장하나 **오보** — TrendForce는 CWF를 "18A 칩렛+**Foveros Direct 3D**"로만 기술, 반도체 분석가 Ian Cutress는 "유리코어는 2030년대 기술, CWF에 없음, 지금까진 연구 프로토타입 한 건뿐"이라 명시 반박.
- Rio Rancho(뉴멕시코)를 유리기판 세계 첫 양산 사이트로 추진(추진 단계).

### TSMC — "협력"(Ibiden+Innolux 3사 검증)
- **JPCA Show 2026(6/11) 첫 공개**: Ibiden·Innolux와 유리코어 기판 공동 검증. 3층 구조(유리코어 + 양면 ABF 빌드업).
- **역할 분담**: Ibiden=ABF 기판 전문(엔비디아·AMD 기판 공급사), Innolux=패널/유리 핸들링·대면적 공정, **TSMC=CoPoS 패키징 통합**. TSMC 발언 "유리코어는 TSMC가 반드시 가져야 할 역량" → 자체 완성이 아니라 **협력으로 확보 중**.
- 검증 데이터(1차 공개): warpage(COP) 16%↓, 유효 CTE 19%↓, 유효 모듈러스 31%↑.
- **시점**: CoPoS 파일럿 '27 → 양산 2H28, **유리코어 본격 상용은 2030 이후** 전망.

### 삼성 — 삼성전자(직접 X) → 삼성전기(JV)
- **삼성전자**는 광반도체(PIC)·패키징은 하나 **유리기판은 직접 안 함**. 그룹 커버는 **계열사 삼성전기(SEMCO)** 몫.
- **삼성전기 JV "GLASEM"(잠정명 GlaSSEM)**: 삼성전기 66% + **동우화인켐 34%**(스미토모화학 한국 자회사). 총자본 ~3억 1,000만 달러(약 4,800억 원), 평택 동우화인켐 부지. **2H27 공급 목표**, 2030 양산 확대.
- → 삼성전자 관점에선 **이중 외부**(계열사 + 그 계열사의 타사 JV). 삼성전기는 **별도 상장사**이므로 사용자 지적대로 "타사"가 맞음.

### GlobalFoundries — 유리기판 경쟁 밖
- 유리**기판(패키지 코어)** 미참여. 대형 로직-광 결합 플랫폼(CoWoS급)도 없음.
- 유리 **도파관(glass WAVEGUIDE)**: Corning과 'GlassBridge' 협력 — 광섬유↔PIC 결합용(detachable fiber), **패키지 기판이 아님**. → "GF가 유리한다"는 이 도파관을 가리키며, 유리기판(코어)과 혼동 금지.

## 유리기판 판(전체) — 실제 선두는 기판 전문사
| 주체 | 성격 | 시점·근거 |
|------|------|-----------|
| **SK 엔펄스(Absolics)** | 기판 전문(SKC 자회사) | 선두 — 美 조지아 공장, '26 양산 목표, AMD 샘플 |
| **삼성전기(GLASEM JV)** | 기판 전문 계열사 + 스미토모 JV | 2H27 공급, 2030 양산 확대 |
| **Ibiden** | ABF 기판 전문(일본) | TSMC 유리코어 파트너, 엔비디아·AMD 기판 공급 |
| **TSMC** | 파운드리(패키징 통합) | 협력 검증(Ibiden·Innolux), 상용 2030+ |
| **Intel** | IDM(자체 R&D) | 자체 개발, 상용 '10년 후반~2030s(프로토타입) |
| **Corning / AGC / Schott** | 유리 소재 원판 공급 | 위 업체들에 유리 원판 공급 |

> 층위: 유리기판은 근본적으로 **기판 전문사(SK·삼성전기·Ibiden)**가 주도하는 층 → 광반도체(광엔진) 파운드리 경쟁과는 다른 축. 파운드리(TSMC·인텔)는 패키징 통합 관점에서 참여.

## 워드용 문구 (사실 기반)
> "유리기판은 **인텔만 자체 개발**(챈들러 팹, 프로토타입·상용 '10년 후반), **TSMC는 Ibiden·Innolux와 협력 검증**, **삼성은 계열사 삼성전기가 스미토모(동우화인켐)와 JV(GLASEM)로 추진**(2H27), GF는 유리기판(코어) 미참여(광결합용 유리 도파관만 Corning 협력). 실제 선두는 기판 전문사(SK Absolics·삼성전기)."

## 출처 (등급)
- **TSMC 협력(Ibiden·Innolux)**: Digitimes(2026.6.16) https://www.digitimes.com/news/a20260616PD217/tsmc-innolux-ibiden-packaging-cowos.html / TrendForce(JPCA Show, CoPoS·유리코어) https://www.trendforce.com/presscenter/news/20260617-13107.html / Ming-Chi Kuo(JPCA 슬라이드 분석) https://x.com/mingchikuo/status/2067438616188739960
- **Intel 자체·프로토타입/CWF 오보 반박**: TrendForce(CWF=18A+Foveros Direct 3D) https://www.trendforce.com/news/2026/03/03/news-intel-unveils-xeon-6-clearwater-forest-at-mwc-with-18a-chiplet-design-and-foveros-direct-3d/ / Ian Cutress(유리코어 2030s, CWF 미탑재) https://x.com/IanCutress/status/2056313353736179802 / Intel Newsroom 유리기판(2023) https://newsroom.intel.com/artificial-intelligence/intel-unveils-industry-leading-glass-substrates
- **삼성전기 JV(GLASEM)**: Sumitomo Chemical 공식 https://www.sumitomo-chem.co.jp/english/news/detail/20260702e_2.html / Seoul Economic(GLASEM·2030) https://en.sedaily.com/finance/2026/07/02/samsung-electro-mechanics-sets-up-glass-substrate-jv-glasem / TrendForce(2H27) https://www.trendforce.com/news/2026/07/06/news-samsung-electro-mechanics-reportedly-signs-deal-to-form-glass-core-jv-with-sumitomo-unit-targeting-2h27-production/
- **GF 유리 도파관(≠기판)**: optics.org(Corning GlassBridge) https://optics.org/news/16/9/49
- **SK Absolics·삼성전기 선두**: 기 foundry-packaging-brief.md 출처 참조

> 주의: "Clearwater Forest 유리코어 양산"은 콘텐츠팜(tokenring/financialcontent 계열) 오보 — 권위 출처(TrendForce·Ian Cutress) 반박. 유리코어 상용은 2030년대. TSMC·삼성전기 시점은 파일럿/양산/공급 기준이 혼재하므로 문맥별 확인.
