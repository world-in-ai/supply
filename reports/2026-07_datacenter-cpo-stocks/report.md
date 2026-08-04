# CPO 도입과 데이터센터 관련주 — 밸류체인별 영향 분석

> **주제** 엔비디아·브로드컴 외 데이터센터(AI 네트워크) 관련주와, CPO 도입이 각 관련주에 미치는 영향
> **작성일** 2026-07-30 · **리서치 기준일** 2026-07-30
> **분류** 기술 동향 + 관련주 매핑 리포트
> **관련 리포트** [`../2026-07_ai-network-cpo/report.md`](../2026-07_ai-network-cpo/report.md) (CPO 기술 본편)

> ⚠️ **면책**: 본 문서는 기술·산업 동향 정리를 위한 자료이며 **투자 조언이 아닙니다**. 티커·수치는 2026년 중반 공개 보도 기준이고 시황은 수시로 변합니다. 투자 판단·손익의 책임은 본인에게 있습니다.

---

## 0. 요약 (Executive Summary)

- CPO의 본질은 **밸류체인 언번들링(unbundling)**이다. 광 기능이 스위치 패키지 안의 **실리콘 포토닉스 엔진**으로 이동하고, 레이저는 **별도 CW 광원**으로 분리되며, **DSP는 대부분 사라진다**. → 가치가 **실리콘 포토닉스·첨단 패키징·광원**으로 이동하고, **독립형 트랜시버 DSP·플러거블 모듈 조립**에서 멀어진다.
- **수혜 축**: 광 부품·레이저(Coherent, Lumentum), 광섬유·커넥터(Corning, Amphenol), 파운드리·패키징(TSMC, ASE, Amkor).
- **혼재(구조 전환 대응 필요) 축**: 커스텀 실리콘·DSP(Marvell, Credo, Astera Labs), 아날로그/드라이버(MACOM, Semtech), 정밀 광 제조(Fabrinet).
- **구조적 역풍 축**: 플러거블 모듈 조립 중심 업체(중국 InnoLight·Eoptolink, 일부 AAOI). 단, **2026년 CPO 침투율은 신규 광인터커넥트의 5% 미만**, 플러거블 호황 창은 2027~2028년까지 → **단기 수혜 + 중장기 리스크** 공존.
- **중립/적응 축**: 스위치 시스템 OEM(Arista, Cisco, HPE) — BOM은 바뀌나 시스템 통합으로 적응.

---

## 1. 프레임: CPO는 누구의 파이를 옮기는가

기존 플러거블 광통신의 가치사슬은 대략 이렇게 구성된다.

```
스위치 ASIC → SerDes/DSP → 드라이버/TIA → 레이저(EML) → 광모듈 조립 → 광섬유/커넥터
```

CPO로 넘어가면:

```
스위치 ASIC ─(패키지 내)─ 실리콘 포토닉스 엔진 ── 광섬유/커넥터
                              ▲                외부 CW 레이저(별도 광원)
                       (DSP 대부분 소멸, 조립 단계 축소)
```

→ **가치 이동의 방향**
- **↑ 커진다**: 실리콘 포토닉스, 첨단 패키징(3D 집적), CW 레이저 광원, 광섬유·정밀 커넥터
- **↓ 줄어든다**: 독립형(standalone) 트랜시버 DSP, 플러거블 모듈 "조립"의 부가가치

이 프레임으로 관련주를 5개 축으로 분류한다.

---

## 2. 밸류체인별 관련주 & CPO 영향

### 2-1. 광 부품 · 레이저 · 실리콘 포토닉스 — **최대 수혜 축**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| Coherent | **COHR** (NYSE) | 광 재료·레이저·트랜시버, CPO 광엔진 | **강한 수혜** — 엔비디아 ~$2B 투자, CPO 협력사 |
| Lumentum | **LITE** (NASDAQ) | EML·CW 레이저(광원) | **강한 수혜** — 엔비디아 ~$2B 투자, Spectrum-X 레이저 |
| Applied Optoelectronics | **AAOI** (NASDAQ) | 수직통합 트랜시버·레이저 | **혼재** — 플러거블 노출 크나 SiPh로 전환 |
| MACOM | **MTSI** (NASDAQ) | 아날로그·드라이버·TIA·포토닉스 | **혼재** — LPO·CPO 부품 수요 vs DSP 대체 |
| Semtech | **SMTC** (NASDAQ) | 커넥티비티 칩·TIA(LPO/광모듈) | **혼재** — 800G/1.6T·CopperEdge 수혜, CPO는 중립 |
| POET Technologies | **POET** (NASDAQ/TSX) | 광 인터포저(레이저·변조기 집적) | **잠재 수혜** — CPO 지향 플랫폼, 초기 매출 단계 |

> 레이저(CW 광원)는 CPO에서 오히려 **더 중요**해진다. DSP·조립이 빠져도 광원은 반드시 필요하기 때문. Coherent·Lumentum이 엔비디아 자본을 받은 이유.

### 2-2. 파운드리 · 첨단 패키징 — **핵심 인에이블러(수혜)**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| TSMC | **TSM** (NYSE) / 2330.TW | COUPE 포토닉 패키징·실리콘 포토닉스 파운드리 | **강한 수혜** — CPO 집적의 핵심 인에이블러 |
| ASE Technology | **ASX** (NYSE) / 3711.TW | 후공정 패키징(OSAT), SPIL 모회사 | **수혜** — CPO 패키징 물량 |
| Amkor | **AMKR** (NASDAQ) | 첨단 패키징(OSAT), TSMC 애리조나 10년 협약 | **수혜** — AI·CPO 패키징 확대 |

> CPO의 병목은 소자가 아니라 **첨단 패키징**이다. 3D 전자-광 집적 캐파를 쥔 파운드리/OSAT가 구조적 수혜.

### 2-3. 광섬유 · 커넥터 — **수혜 축**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| Corning | **GLW** (NYSE) | 광섬유·광 커넥티비티 | **수혜** — 엔비디아 ~$0.5B 투자, 광섬유 직결 |
| Amphenol | **APH** (NYSE) | 커넥터·IT Datacom(엔비디아 주력 커넥터) | **수혜** — AI capex, 광/전 커넥터 |
| TE Connectivity | **TEL** (NYSE) | 커넥터·인터커넥트 | **수혜(간접)** — 데이터센터 물량 |

> CPO는 광섬유를 스위치 패키지까지 직접 끌어오므로 **정밀 광 커넥터·섬유 결합** 수요가 오히려 늘어난다.

### 2-4. 스위치 ASIC · 커스텀 실리콘 · DSP/리타이머 — **혼재 축**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| Marvell | **MRVL** (NASDAQ) | 커스텀 XPU·광 DSP·실리콘 포토닉스 | **혼재** — DSP 역풍 vs Celestial AI 인수로 CPO 진입, 엔비디아 ~$2B 투자 |
| Credo | **CRDO** (NASDAQ) | 광 DSP(1.6T Cardinal)·AEC·SerDes | **혼재** — DSP·AEC 역풍 가능성 vs 광 DSP 확장 |
| Astera Labs | **ALAB** (NASDAQ) | PCIe/CXL 리타이머·스마트 케이블·광 결합 | **혼재** — aiXscale(글래스 커플러) 인수로 광 내재화 |
| AMD | **AMD** (NASDAQ) | AI 가속기(MI 시리즈), 광 스타트업 투자 | **간접** — Enosemi 인수·Teramount/Celestial AI 투자로 광 확보 |
| MaxLinear | **MXL** (NASDAQ) | 광 DSP·PAM4 | **역풍 가능** — 독립형 DSP 축소 리스크 |

> 핵심 긴장: **CPO/LPO는 DSP를 줄인다**. 하지만 이들은 커스텀 실리콘·광 결합·리타이머 등으로 **가치를 재배치**하며 대응 중. 특히 Marvell은 인수로 CPO 진영에 올라탔다.

### 2-5. 광모듈 조립 · EMS — **단기 수혜 + 중장기 역풍 축**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| Fabrinet | **FN** (NYSE) | 정밀 광 제조·조립(Lumentum·Coherent 위탁) | **혼재** — 플러거블 조립 노출 vs CPO 정밀조립 수주 |
| InnoLight(中际旭创) | **300308.SZ** | 세계 1위 광모듈(400G/800G) | **단기 수혜, 중장기 역풍** — 조립 부가가치 축소 리스크, LPO/SiPh로 헤지 |
| Eoptolink(新易盛) | **300502.SZ** | 광모듈(800G/1.6T) | **단기 수혜, 중장기 역풍** — 플러거블/LPO/XPO/NPO/CPO 다변화로 헤지 |

> 중국 모듈 2강은 **2026년 800G/1.6T 호황**을 누리면서도, CPO가 "조립 단계"의 부가가치를 잠식하는 중장기 리스크에 대비해 LPO·SiPh·CPO로 포트폴리오를 넓히는 중.

### 2-6. 스위치 시스템 · 네트워킹 OEM — **중립/적응 축**

| 기업 | 티커 | 역할 | CPO 영향 |
|------|------|------|----------|
| Arista Networks | **ANET** (NYSE) | 데이터센터 스위치·AI 네트워킹 | **중립/적응** — CPO/XPO 옵티컬 모듈 채택, BOM 변화 흡수 |
| Cisco | **CSCO** (NASDAQ) | 네트워킹·Acacia(코히어런트 광) | **중립/적응** — 광 내재화(Acacia)로 대응 |
| HPE | **HPE** (NYSE) | 서버·네트워킹(Juniper 인수) | **중립** — 시스템 통합 관점 |

> 시스템 OEM은 CPO로 스위치 내부 BOM이 바뀌지만, **완제품 통합·소프트웨어**로 가치를 유지 → 큰 방향성 리스크는 제한적.

---

## 3. 비상장 / 인수된 핵심 플레이어 (티커 없음)

CPO 밸류체인의 무게중심이지만 아직 상장 전이거나 인수된 곳:

| 기업 | 상태 | 기술 |
|------|------|------|
| **Ayar Labs** | 비상장 (엔비디아·AMD 등 투자, Series E $500M) | 인패키지 광 I/O |
| **Lightmatter** | 비상장 (밸류 ~$44억) | 3D 실리콘 포토닉스 엔진 Passage |
| **Xscape Photonics** | 비상장 (엔비디아·Cisco 투자) | 다파장 레이저 FalconX |
| **Celestial AI** | **Marvell(MRVL) 인수** (2025.12) | 광 인터커넥트(Photonic Fabric) |
| **Enosemi** | **AMD 인수** (2025) | 실리콘 포토닉스 |

> 이들의 상장·M&A 여부는 상장 관련주(특히 MRVL·AMD)의 광 역량 평가에 직접 영향.

---

## 4. 종합 매핑 — CPO 영향 방향성

| 방향성 | 관련주(티커) | 논리 |
|--------|--------------|------|
| **↑ 구조적 수혜** | COHR, LITE, GLW, APH, TSM, ASX, AMKR | 광원·광섬유·커넥터·패키징 — CPO에서 오히려 가치 증가 |
| **↔ 혼재(대응 관건)** | MRVL, CRDO, ALAB, MTSI, SMTC, FN, AAOI | DSP·조립 역풍 vs 실리콘 포토닉스·커스텀·정밀조립으로 재배치 |
| **↓ 중장기 역풍** | 300308.SZ, 300502.SZ, MXL | 플러거블 조립·독립형 DSP 부가가치 잠식 (단, 2027~28까지 단기 호황) |
| **= 중립/적응** | ANET, CSCO, HPE | 시스템 통합으로 BOM 변화 흡수 |

### 타이밍 유의점
- **2026년 CPO 침투율 < 5%** (신규 DC 광인터커넥트 기준). 플러거블 시장 창은 **2027~2028년**까지.
- 그 사이 **800G/1.6T 수요는 계속 두 배**로 성장 → 플러거블·LPO 진영도 단기 실적 호조.
- 즉 "CPO 수혜"와 "플러거블 호황"은 **당분간 공존**하며, CPO 잠식은 **점진적**으로 나타난다.

---

## 5. 시사점

1. **가장 견고한 수혜는 "빠질 수 없는 것"에 있다** — 광원(레이저)·광섬유·커넥터·패키징. CPO가 DSP·조립을 없애도 이들은 남는다.
2. **혼재 그룹은 "전환 성공 여부"가 관건** — Marvell처럼 인수로 CPO에 올라타는지, Credo·Astera처럼 광 결합을 내재화하는지가 분기점.
3. **플러거블 조립주는 단기 트레이딩 vs 중장기 구조 리스크를 분리해서 볼 것** — 2026~2027 실적과 2028+ 침투율은 다른 이야기.
4. **엔비디아의 자본 지도가 곧 공급망 지도** — COHR·LITE·GLW·MRVL·Ayar Labs 등 엔비디아가 돈을 넣은 곳이 CPO 공급망의 급소. (상세: [`../2026-07_ai-network-cpo/nvidia-supply-chain-investments.md`](../2026-07_ai-network-cpo/nvidia-supply-chain-investments.md))

---

## 참고 문헌

1. Chipstrat, "Optics Primer, Part 3: Co-Packaged Optics (CPO)", https://www.chipstrat.com/p/optics-primer-part-3-co-packaged
2. exoswan, "Top Silicon Photonics Stocks 2026: Breaking the Copper Wall", https://exoswan.com/photonics-stocks/
3. 24/7 Wall St., "Which Optics Stock Has Dominated in 2026: AAOI, Lumentum, or Coherent?" (2026.05), https://247wallst.com/investing/2026/05/12/which-optics-stock-has-dominated-in-2026-applied-optoelectronics-lumentum-or-coherent/
4. Seeking Alpha, "Lumentum, Coherent, Applied Optoelectronics surge on AI optical demand", https://seekingalpha.com/news/4565713-lumentum-coherent-applied-optoelectronics-surge-on-strong-optical-demand-momentum-tied-to-ai
5. StockTitan, "TSMC and Amkor Announce Long-Term Partnership for Advanced Packaging in Arizona", https://www.stocktitan.net/news/TSM/tsmc-and-amkor-technology-announce-long-term-partnership-to-sv316wnmjbm1.html
6. Yahoo Finance, "ASE Technology vs. Amkor: Which Chip Packaging Stock Is the Better Buy?", https://finance.yahoo.com/markets/stocks/articles/ase-technology-vs-amkor-chip-162800664.html
7. HTX Insights, "Standing in the Light: A Comprehensive Guide to the Optical Module and CPO Supply Chain", https://www.htx.com/news/Research%20&%20Analysis-W6PlkLJd/
8. BigGo Finance, "The Truth and Strategic Calculus Behind CPO Mass Production Delays", https://finance.biggo.com/news/wZGWtJ4BYH_ypPqO6d_I
9. Arista Networks / Globe and Mail, "Arista's XPO Optical Modules for AI Networks", https://www.theglobeandmail.com/investing/markets/stocks/ANET/pressreleases/738641/
10. Forbes, "Nvidia's $4 Billion Investment In Optics Companies Lumentum And Coherent" (2026.03), https://www.forbes.com/sites/stevemcdowell/2026/03/04/nvidias-optical-strategy-4-billion-reshapes-ai-data-center-economics/

> 티커 표기: 미국 상장은 거래소(NYSE/NASDAQ), 중국 A주는 선전 `.SZ`, 대만은 `.TW`로 병기. 미국 ADR이 있는 경우 ADR 티커(TSM, ASX)를 우선 표기.
