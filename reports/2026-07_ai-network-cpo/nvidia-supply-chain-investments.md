# 부록 — 엔비디아의 CPO 핵심 공급망 선점 투자 정리

> 본문: [`report.md`](report.md) · 작성일 2026-07-30 · 리서치 기준일 2026-07-30
> 주제: 엔비디아(NVIDIA)가 CPO/광통신(photonics) 공급망을 선점하기 위해 집행한 지분 투자·전략 파트너십

## 한눈에 보기

엔비디아는 **2단계 전략**으로 CPO 공급망을 확보했다.

1. **1단계 — 생태계 협력 (GTC 2025.03)**: 실리콘 포토닉스 스위치(Quantum-X/Spectrum-X) 발표와 함께 광 부품·패키징·광섬유 업체를 "이노베이션 협력사"로 묶음.
2. **2단계 — 지분·자본 투자 (2026.03~)**: 협력사 중 핵심 병목 업체에 **직접 지분 투자 + 대규모 구매 약정 + 향후 생산능력(캐파) 확보권**을 결합해 공급을 락인. **2026년 3월 이후 광통신에만 총 65억 달러+ 커밋**.

> 시사점: 광 부품 공급망을 "협력"만으로는 부족하다고 보고, **자본(지분)으로 캐파를 선점**한 것. AI 칩 리더가 광 공급망을 생태계의 **가장 취약한 급소**로 인식하고 있음을 드러낸다.

---

## A. 대형 전략 투자 / 지분 (핵심 공급망 락인)

| 대상 | 규모(보도 기준) | 형태 | 무엇을 확보했나 |
|------|-----------------|------|-----------------|
| **Coherent** | 약 20억 달러 | 성장지분 + 구매약정 + 캐파 확보권 | CPO용 광 엔진·레이저·트랜시버 |
| **Lumentum** | 약 20억 달러 | 성장지분 + 구매약정 + 캐파 확보권 | Spectrum-X용 레이저(광원) |
| **Marvell** | 약 20억 달러 | 지분 투자 | 실리콘 포토닉스 (Celestial AI 인수, 2025.12 / $3.25B~5.5B) |
| **Corning** | 약 5억 달러 | 지분 투자 | 광섬유·광 커넥티비티 |

- **Coherent·Lumentum**은 원래 GTC 2025 생태계 협력사였는데, 2026년 3월 각각 **약 20억 달러 규모의 전략 파트너십**으로 격상. 단순 공급계약이 아니라 **지분 + 다년 구매약정 + 미래 캐파 우선권**이 결합된 구조로, 사실상 두 회사의 광 부품 생산라인을 엔비디아 쪽으로 예약한 것.
- **Marvell**: 약 20억 달러 투자. Marvell은 2025년 12월 실리콘 포토닉스 스타트업 **Celestial AI를 인수**($3.25B, 언아웃 포함 최대 $5.5B)하며 광 네트워킹 역량 강화 → 엔비디아가 이 축에도 자본 참여.
- **Corning**: 약 5억 달러. AI 데이터센터용 첨단 광 연결(광섬유·도파관) 공급망 확보.

## B. 스타트업 벤처 투자 (NVentures / 전략 라운드 참여)

| 대상 | 라운드 | 엔비디아 역할 | 기술 |
|------|--------|---------------|------|
| **Ayar Labs** | Series E, 5억 달러 (2026.03, 밸류 $3.75B) | 라운드 참여 | 인패키지 **광 I/O(optical I/O)**, CPO 선구자 |
| **Xscape Photonics** | Series A $44M (+후속 $37M) | 참여(기존 투자자) | 다파장(8-color) 레이저 **FalconX** |

- **Ayar Labs**: CPO/광 I/O의 대표 스타트업. 5억 달러 Series E를 AMD·MediaTek·Intel Capital·Sequoia 등과 함께 참여. 가속기 패키지 안에 광 인터페이스를 직접 넣는 "in-package optical I/O"로, 스위치를 넘어 **가속기 단(scale-up)까지 광 확장**을 겨냥.
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

> 주의: 투자 금액은 언론 보도 기준의 근사치이며, 일부는 지분·구매약정·캐파 확보권이 혼합된 패키지 딜이라 "순수 지분 규모"와 다를 수 있음.
