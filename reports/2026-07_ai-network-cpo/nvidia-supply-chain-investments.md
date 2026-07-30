# 부록 — 엔비디아의 CPO 핵심 공급망 선점 투자 정리

> 본문: [`report.md`](report.md) · 작성일 2026-07-30 · 리서치 기준일 2026-07-30
> 주제: 엔비디아(NVIDIA)가 CPO/광통신(photonics) 공급망을 선점하기 위해 집행한 지분 투자·전략 파트너십

## 한눈에 보기

엔비디아는 **2단계 전략**으로 CPO 공급망을 확보했다.

1. **1단계 — 생태계 협력 (GTC 2025.03)**: 실리콘 포토닉스 스위치(Quantum-X/Spectrum-X) 발표와 함께 광 부품·패키징·광섬유 업체를 "이노베이션 협력사"로 묶음.
2. **2단계 — 지분·자본 투자 (2026.03~)**: 협력사 중 핵심 병목 업체에 **직접 지분 투자 + 대규모 구매 약정 + 향후 생산능력(캐파) 확보권**을 결합해 공급을 락인. **2026년 3월 이후 광통신에만 총 65억 달러+ 커밋**.

> 시사점: 광 부품 공급망을 "협력"만으로는 부족하다고 보고, **자본(지분)으로 캐파를 선점**한 것. AI 칩 리더가 광 공급망을 생태계의 **가장 취약한 급소**로 인식하고 있음을 드러낸다.

---

## 투자 통합 표 (주요 업체 · 투자 내용 · 투자 금액)

대형 전략 투자(A)와 스타트업 벤처 투자(B)를 한 표로 정리. 금액은 언론 보도 기준.

| 주요 업체 | 유형 | 투자 내용 | 투자 금액 (시점) |
|-----------|------|-----------|------------------|
| **Coherent** | 광 부품·레이저·CPO 광엔진 (전략 파트너십) | 지분 + 다년 수십억$ 구매약정 + 캐파/우선접근권, 美 생산라인 증설 지원 | **약 $2B** (2026.03) |
| **Lumentum** | CW 레이저(광원) (전략 파트너십) | 지분 + 구매약정 + 캐파 확보권, 美 신규 팹 지원 | **약 $2B** (2026.03) |
| **Marvell** | 커스텀 XPU·광 DSP·실리콘 포토닉스 (지분) | NVLink Fusion 연계, Celestial AI(Photonic Fabric) 기반 | **약 $2B** (2026.03~04) |
| **Corning** | 광섬유·광 커넥티비티 (광범위 딜) | 美 광섬유 캐파 50%+·커넥티비티 10배 확대, 공장 3곳 | **약 $3.2B** (광범위 딜 기준, 2026.05) |
| **기타 스타트업** (Ayar Labs, Xscape Photonics 등) | 인패키지 광 I/O·다파장 레이저 (벤처) | Ayar Labs Series E($500M) + Xscape Series A($44M) 참여 | **약 $0.54B** (참여 라운드 합산) |
| — **합계** — | 광통신(photonics) 전체 | 위 항목 합산 | **약 $9.74B** |

> 금액 주의:
> - 대형 4건은 지분+구매약정+캐파권이 섞인 패키지 딜의 **총 규모**(순수 지분과 다름). Corning은 "$500M 주식취득권" 보도와 별개로 **광범위 딜 최대 규모 $3.2B** 기준으로 표기.
> - 기타 스타트업은 엔비디아가 **참여한 라운드 전체 규모**(엔비디아 단독 출자액 아님). Lightmatter 등은 CPO 경쟁사이나 엔비디아 투자가 확인되지 않아 제외.
> - 합계 **$9.74B**는 위 딜/라운드 규모를 단순 합산한 값. 언론이 보도한 엔비디아 광통신 **커밋 총액은 "$6.5B+"**로, Corning을 딜 최대치로 잡은 본 표와 산정 기준이 다름.

---

## A. 대형 전략 투자 / 지분 (핵심 공급망 락인)

| 대상 | 규모(보도 기준) | 형태 | 발표 시점 | 내용 |
|------|-----------------|------|-----------|------|
| **Coherent** | 약 20억 달러 | 지분 + 구매약정 + 캐파/우선접근권 (비독점) | 2026.03.02 | R&D·미래 캐파·운영 및 **美 신규 생산라인 증설** 지원. 다년 수십억 달러 구매약정 + 첨단 레이저·광 네트워킹 제품에 대한 미래 접근·캐파 권리. CPO용 광 엔진·트랜시버 |
| **Lumentum** | 약 20억 달러 | 지분 + 구매약정 + 캐파 확보권 (비독점) | 2026.03.02 | R&D·미래 캐파·운영 및 **美 신규 팹(fab)** 지원. 다년 수십억 달러 구매약정 + 첨단 레이저 부품 캐파 권리. CPO 핵심 **CW 레이저(광원)** — Spectrum-X용 |
| **Marvell** | 약 20억 달러 | 지분 투자 (NVLink Fusion 연계) | 2026.03~04 | Marvell **커스텀 XPU + 광 DSP**를 NVLink Fusion으로 NVIDIA AI 팩토리 생태계에 연결. Celestial AI 인수로 확보한 **Photonic Fabric**(GPU↔외부 메모리 풀 근거리급 접속) 결합 |
| **Corning** | 약 5억 달러 (광범위 딜은 최대 ~$3.2B) | 주식 취득권(rights) + 캐파 파트너십 | 2026.05.06 | **광섬유·광 커넥티비티**. Corning은 美 광섬유 생산 캐파 **50%+ 확대**, 광 커넥티비티 캐파 **10배 확대**, NC·TX에 **신규 공장 3곳** 건설 |

### 딜별 상세

- **Coherent·Lumentum** — 원래 GTC 2025 생태계 협력사였는데, **2026년 3월 2일 각각 약 20억 달러 전략 파트너십**(합계 ~$4B)으로 격상. 단순 공급계약이 아니라 **지분 + 다년 수십억 달러 구매약정 + 미래 캐파/우선접근권**이 결합된 구조 → 사실상 두 회사의 광 부품·레이저 생산라인을 엔비디아 쪽으로 **예약(선점)**. 자금은 **미국 내 생산능력 증설**(Lumentum 신규 팹 등)에 투입. **비독점** 조건이라 두 회사는 타 고객도 계속 공급 가능.
  - Coherent·Lumentum은 **CPO의 핵심 병목인 레이저(광원)** 공급사 → 이 투자는 차세대 AI 인프라의 **핵심 공급망을 직접 확보**하는 의미.
- **Marvell** — **약 20억 달러 지분 투자**. Marvell의 **커스텀 XPU 실리콘 + 광 DSP**를 **NVLink Fusion**을 통해 NVIDIA 생태계에 결속(파트너십을 생태계 락인으로 전환). 기반 기술은 2025.12 발표·**2026.02 종결**된 **Celestial AI 인수**($3.25B = 현금 $1B + 주식 $2.25B, 언아웃 포함 최대 $5.5B)로 확보한 **Photonic Fabric** — GPU가 외부 메모리 풀에 근거리급 속도로 접속하게 하는 광 인터커넥트.
- **Corning** — **약 5억 달러 주식 취득권**(광범위 파트너십 기준 보도상 최대 ~$3.2B 규모). AI 데이터센터용 **광섬유·광 커넥티비티** 공급 확대가 핵심. Corning은 美 **광섬유 생산 캐파 50%+**, **광 커넥티비티 캐파 10배** 확대와 **NC·텍사스 신규 공장 3곳** 건설을 약속 → 광섬유 물량을 엔비디아 수요에 맞춰 선제 증설.

## B. 스타트업 벤처 투자 (NVentures / 전략 라운드 참여)

| 대상 | 라운드 | 엔비디아 역할 | 기술 |
|------|--------|---------------|------|
| **Ayar Labs** | Series E, 5억 달러 (2026.03, 밸류 $3.75B) | 라운드 참여 | 인패키지 **광 I/O(optical I/O)**, CPO 선구자 |
| **Xscape Photonics** | Series A $44M (+후속 $37M) | 참여(기존 투자자) | 다파장(8-color) 레이저 **FalconX** |

- **Ayar Labs**: CPO/광 I/O의 대표 스타트업. 엔비디아는 **2023.05 Series C($155M)부터 참여**해온 장기 투자자이며, 2026.03 **Series E($500M, 밸류 $3.75B, 누적 $870M)**를 AMD·Intel Capital·Neuberger Berman 등과 함께 참여. 가속기 패키지 안에 광 인터페이스를 직접 넣는 "in-package optical I/O"로, 스위치를 넘어 **가속기 단(scale-up)까지 광 확장**을 겨냥.
- **Xscape Photonics**: AI 데이터센터 네트워크용 다파장 레이저. Cisco와 함께 엔비디아가 참여.

## C. GTC 2025 CPO 생태계 협력사 (자본 투자와 별개인 공급/협력)

투자 여부와 무관하게 엔비디아가 CPO 공급망으로 공식 명시한 파트너:

| 업체 | 역할 |
|------|------|
| **TSMC** | COUPE 패키징 + 실리콘 포토닉스 파운드리 (핵심 인에이블러) |
| **Coherent** | 광 엔진·CPO 협력 *(→ B/A에서 지분 투자로 격상)* |
| **Lumentum** | Spectrum-X용 레이저 *(→ 지분 투자로 격상)* |
| **Corning** | 광섬유·광 커넥티비티 *(→ 지분 투자)* |
| **Fabrinet** | 광모듈 조립·제조(EMS) |
| **Foxconn** | 제조 |
| **SENKO** | 광 커넥터 |
| **Browave** | 광 부품(스위치/커넥터) |
| **Sumitomo Electric** | 광 부품 |
| **SPIL** | 후공정 패키징(OSAT) |
| **TFC** | 광 부품 |

> NVIDIA는 이 협력을 통해 "3.5배 전력 효율, 63배 신호 무결성, 10배 네트워크 복원력, 1.3배 빠른 배치, 레이저 사용량 25% 수준"을 주장.

---

## 정리 — 왜 이렇게 투자했나

1. **병목의 이동**: 연산이 아니라 **칩 간 광 연결**이 AI 스케일의 병목 → 광 부품(레이저·광엔진·광섬유·패키징)이 전략 자산이 됨.
2. **캐파 선점**: 실리콘 포토닉스 양산 캐파는 한정적. 지분 + 구매약정 + 캐파 우선권으로 **경쟁사보다 먼저, 안정적으로** 물량 확보.
3. **수직 통합 심화**: GPU→NVLink→스위치(CPO)→광 부품까지 **밸류체인 전 구간**을 자본으로 결속 → NVIDIA 생태계 락인 강화.
4. **경쟁 구도**: AMD도 병렬로 방어 — **Enosemi 인수(2025)**, **Teramount·Celestial AI 지분 투자** 등. 광 공급망 확보전이 AI 칩 경쟁의 새 전선.

---

## 참고 문헌

1. NVIDIA, "NVIDIA Announces Spectrum-X Photonics, Co-Packaged Optics Networking Switches" (GTC 2025.03), https://investor.nvidia.com/news/press-release-details/2025/NVIDIA-Announces-Spectrum-X-Photonics-Co-Packaged-Optics-Networking-Switches-to-Scale-AI-Factories-to-Millions-of-GPUs/default.aspx
2. Coherent, "Coherent Recognized as One of NVIDIA's Ecosystem Innovation Collaborators for Co-Packaged Optics at GTC", https://www.coherent.com/news/press-releases/coherent-recognized-as-nvidia-ecosystem-innovation-partner
3. Optica (OPN), "NVIDIA Looks to Co-Packaged Optics for AI 'Factories'", https://www.optica-opn.org/home/industry/2025/march/nvidia_looks_to_co-packaged_optics_for_ai_factories/
4. Forbes, "Nvidia's $4 Billion Investment In Optics Companies Lumentum And Coherent" (2026.03), https://www.forbes.com/sites/stevemcdowell/2026/03/04/nvidias-optical-strategy-4-billion-reshapes-ai-data-center-economics/
5. CNBC, "Nvidia is investing billions into this emerging technology" (2026.05), https://www.cnbc.com/2026/05/29/nvidia-photonics-investment-ai.html
6. The Next Web, "Nvidia spends $6.5B on photonics to fix AI's copper bottleneck", https://thenextweb.com/news/nvidia-photonics-investment-copper-bottleneck-ai-data-centre
7. The Next Platform, "Ayar Labs Gets $500 Million To Ramp Photonics Into 2028 AI Systems" (2026.03), https://www.nextplatform.com/connect/2026/03/04/ayar-labs-gets-500-million-to-ramp-photonics-into-2028-ai-systems/
8. optics.org, "Silicon photonics startup Xscape backed by Nvidia and Cisco in $44M funding round", https://optics.org/news/15/10/27
9. Xscape Photonics, "$37 Million in New Funding, Launches Eight-Wavelength Laser" (2026.03), https://www.businesswire.com/news/home/20260311692947/en/
10. optim.vc, "The State of Silicon Photonics: Who's Building, Who's Buying", https://www.optim.vc/the-state-of-silicon-photonics-whos-building-whos-buying-and-where-the-industry-is-heading/
11. NVIDIA Newsroom, "NVIDIA and Coherent Announce Strategic Partnership to Develop Optics Technology" (2026.03.02), https://nvidianews.nvidia.com/news/nvidia-and-coherent-announce-strategic-partnership-to-develop-optics-technology-to-scale-next-generation-data-center-architecture
12. NVIDIA Newsroom, "NVIDIA Announces Strategic Partnership With Lumentum" (2026.03.02), https://nvidianews.nvidia.com/news/nvidia-announces-strategic-partnership-with-lumentum-to-develop-state-of-the-art-optics-technology
13. CNBC, "Nvidia to invest $4 billion into photonics companies Coherent and Lumentum" (2026.03.02), https://www.cnbc.com/2026/03/02/nvidia-investment-coherent-lumentum.html
14. Marvell, "Marvell to Acquire Celestial AI, Accelerating Scale-up Connectivity" (인수 종결 2026.02), https://investor.marvell.com/news-events/press-releases/detail/1000/
15. TechFundingNews, "NVIDIA invests $2B in Marvell: NVLink Fusion ecosystem lock-in", https://techfundingnews.com/nvidia-2-billion-marvell-nvlink-fusion-ai-ecosystem/
16. CNBC, "Nvidia to invest up to $3.2 billion in Corning as part of massive optical fiber deal" (2026.05.06), https://www.cnbc.com/2026/05/06/nvidia-corning-optical-factories-nc-texas-ai.html
17. Bloomberg, "Nvidia Inks $500 Million Deal With Fiber-Optic Maker Corning" (2026.05.06), https://www.bloomberg.com/news/articles/2026-05-06/nvidia-buys-500-million-of-rights-for-stock-in-corning
18. The Register, "Ayar Labs raises $500M to mass-produce CPO chiplets" (2026.03.03), https://www.theregister.com/2026/03/03/ayar_labs_500m/
19. Ayar Labs, "Ayar Labs Secures $155M Series C, includes AMD, Intel Capital, NVIDIA" (2023.05), https://ayarlabs.com/news/ayar-labs-155m-series-d-to-address-ai-infrastructure-includes-amd-intel-capital-nvidia/

> 주의: 투자 금액은 언론 보도 기준의 근사치이며, 일부는 지분·구매약정·캐파 확보권이 혼합된 패키지 딜이라 "순수 지분 규모"와 다를 수 있음. Corning은 보도에 따라 "$500M 주식취득권"과 "최대 $3.2B 광범위 딜"이 함께 언급됨.
