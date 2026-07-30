# 브로드컴(Broadcom) — 엔비디아 반대 진영의 CPO·AI 네트워킹 — 리서치 브리프

> 목적: 엔비디아 대비 브로드컴의 CPO·AI 네트워킹 전략 정리(워드 최종본용 재료)
> 작성일 2026-07-30 · 리서치 기준일 2026-07-30
> 짝 문서: [`nvidia-supply-chain-investments.md`](nvidia-supply-chain-investments.md) · 본편: [`report.md`](report.md)

## TL;DR
- 브로드컴은 **개방형(open) 이더넷** 진영의 축. 엔비디아의 폐쇄형 NVLink/InfiniBand·수직통합에 맞서 **"이더넷 하나로 scale-up + scale-out"**을 내세움.
- **이더넷 스위치 ASIC 시장 ~80% 점유**. CPO도 **3세대**까지 왔고(Tomahawk 6 – Davisson, 102.4 Tbps) **엔비디아보다 타이밍 앞섬**.
- **커스텀 AI 가속기(XPU)** 설계로 하이퍼스케일러의 탈엔비디아를 지원 — 구글·메타·오픈AI·앤스로픽·(2026 신규)애플 등. 커스텀 ASIC 설계 시장 ~70%.
- CPO 철학 차이: 브로드컴은 **레이저를 현장 교체 가능(field-replaceable)**하게 설계 → 엔비디아 대비 **유지보수성**을 강조.

## 핵심 팩트 / 수치
| 항목 | 값 | 비고 |
|------|----|------|
| 이더넷 스위치 ASIC 점유율 | 약 80% | 시장 지배 |
| 커스텀 AI ASIC 설계 시장 점유 | 약 70% | Marvell과 듀오폴리 |
| Tomahawk 6 – Davisson | **102.4 Tbps**, 세계 첫 이 용량 CPO 이더넷 스위치 | 2025.10 발표, 2026.03 양산 |
| 채널 속도 | 200 Gbps/ch (TH5-Bailly의 2배) | |
| 800G 포트 전력 | 약 **3.5W** | TH5 CPO 대비 -36%, 플러거블 대비 -70%+ |
| Jericho 4 (패브릭 칩) | 51.2 Tbps, 100만+ XPU/데이터센터간 연결 | 2025.08 출하 |
| 4세대 CPO 로드맵 | 채널 **400 Gbps**로 2배 | 개발 중 |
| 공정 | TSMC 3nm | 커스텀 XPU |
| AI 백로그 | $73B, 2027년 칩 AI 매출 $100B+ "line of sight" | Hock Tan |

## 논점별 요점

### 1. 개방형 vs 폐쇄형 (엔비디아와의 핵심 대립축)
- 엔비디아: NVLink(scale-up)·InfiniBand·GPU-스위치-광 **수직통합·독점** → 고객 락인.
- 브로드컴: **표준 이더넷**으로 scale-up·scale-out 모두 커버, 다수 파트너와 **개방 생태계**. NVLink의 독점성을 "락인"이라 직접 저격.
- CPO에서도 브로드컴은 특정 패키징/포토닉스 벤더 종속을 피하는 **오픈 에코시스템** 접근(Bailly 계열부터의 전략).

### 2. 스위치 라인업 (제품 축)
- **Tomahawk 6 – Davisson**: 102.4 Tbps CPO 이더넷, chiplet 구조(SerDes 분리), scale-up/scale-out 겸용, 최대 **100만 XPU** 단일 이더넷 패브릭.
- **Jericho 4**: 51.2 Tbps 패브릭, 데이터센터 간 100만+ XPU 연결(딥버퍼 라우팅).
- CPO는 이미 **3세대**(TH3 → TH5-Bailly → TH6-Davisson) 축적 → 성숙도·타이밍 우위.

### 3. CPO 설계 철학 차이 (엔비디아 대비)
- **레이저 현장 교체 가능(field-replaceable)**: 전면 패널에서 교체, ASIC 근처에 두지 않음 → CPO 최대 약점인 **유지보수성**을 정면 대응.
- 전력: 800G 포트 ~3.5W로 플러거블 대비 70%+ 절감(엔비디아와 유사한 방향, 수치도 근접).

### 4. 커스텀 XPU (하이퍼스케일러 탈엔비디아 지원)
- 브로드컴이 하이퍼스케일러의 **자체 AI 칩 설계**를 대행 → 엔비디아 GPU 의존도↓.
- 확인 고객: **구글(TPU)·메타(MTIA)·오픈AI·앤스로픽·애플(2026 신규)**, ByteDance 협업 보도.
- OpenAI와 **10GW 규모** 공동 개발(가속기+이더넷, scale-up/scale-out). Apollo·Blackstone과 **20GW XPU 플랫폼**.

### 5. 타이밍 우위
- TH6 2026.03 양산 vs 엔비디아 Spectrum-X(1.6T) 대량은 **2H26** → 2026년 브로드컴이 시간 우위.

## NVIDIA vs Broadcom 대비표
| 축 | NVIDIA | Broadcom |
|----|--------|----------|
| 철학 | 폐쇄·수직통합 | 개방·모듈(이더넷) |
| Scale-up | NVLink(독점) | 이더넷(TH6) — "락인 없음" |
| Scale-out | InfiniBand/Spectrum-X | 이더넷(TH6/Jericho4) |
| CPO 세대 | 1세대(Quantum/Spectrum Photonics) | **3세대**(Davisson) |
| CPO 유지보수 | 통합형(교체 난이도↑) | **레이저 현장 교체** |
| 가속기 | 자사 GPU 판매 | 고객 **커스텀 XPU 설계 대행** |
| 공급망 | 광 부품사 지분 투자로 락인 | 개방 생태계·다벤더 |
| 2026 타이밍 | Spectrum-X 1.6T 2H26 | TH6 3월 양산(우위) |

## 워드 작성용 목차 제안
1. 개요 — 왜 브로드컴이 "엔비디아 반대 진영"인가 (개방 vs 폐쇄)
2. 시장 지위 (이더넷 스위치 80%, 커스텀 ASIC 70%)
3. 제품 라인업 (Tomahawk 6-Davisson, Jericho 4)
4. CPO 전략과 설계 철학 (3세대, 레이저 현장 교체, 전력)
5. 커스텀 XPU와 하이퍼스케일러 동맹 (구글·메타·오픈AI·애플…)
6. NVIDIA와의 대비 및 2026 타이밍
7. 시사점 (개방 진영의 확산 조건·리스크)

## 출처
1. Broadcom, "Broadcom Announces Tomahawk 6 – Davisson, Industry's First 102.4-Tbps Ethernet Switch with CPO" (2025.10.08), https://investors.broadcom.com/news-releases/news-release-details/broadcom-announces-tomahawkr-6-davisson-industrys-first-1024
2. ServeTheHome, "Broadcom Tomahawk 6 – Davisson 102.4T Switch with CPO Shipping", https://www.servethehome.com/broadcom-tomahawk-6-davisson-102-4t-switch-with-co-packaged-optics-shipping/
3. The Next Platform, "The Third Time Will Be The Charm For Broadcom Switch Co-Packaged Optics" (2025.10.17), https://www.nextplatform.com/2025/10/17/the-third-time-will-be-the-charm-for-broadcom-switch-co-packaged-optics/
4. Tom's Hardware, "The custom AI ASIC state of play (May 2026) — Broadcom, Google TPUs, Meta MTIA & beyond", https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia
5. Futuriom, "Broadcom Chip Advances Ethernet for AI" (2025.06), https://www.futuriom.com/articles/news/broadcom-chip-advances-ethernet-for-ai/2025/06
6. FinancialContent, "The Backbone of the Million-GPU Cluster: Broadcom's Dominance in the 2026 AI Networking Supercycle" (2025.12.29), https://markets.financialcontent.com/wral/article/marketminute-2025-12-29-the-backbone-of-the-million-gpu-cluster-broadcoms-dominance-in-the-2026-ai-networking-supercycle
7. DCD, "Broadcom, Apollo, and Blackstone launch 20GW XPU platform", https://www.datacenterdynamics.com/en/news/broadcom-apollo-and-blackstone-launch-20gw-xpu-platform/
8. Futurum, "Broadcom Q1 FY2026 Earnings Driven by XPU Momentum", https://futurumgroup.com/insights/broadcom-q1-fy-2026-earnings-driven-by-xpu-momentum/

> 주의: 시장 점유율·백로그·고객 명단은 언론·리서치 보도 기준의 추정/발표치. 일부 고객사(앤스로픽·애플·ByteDance)는 보도 기반으로 회사 공식 확인과 차이가 있을 수 있음.
