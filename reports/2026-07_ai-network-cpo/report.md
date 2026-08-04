# AI 네트워크(칩 간 데이터 전송) 기술 동향 — CPO(Co-Packaged Optics) 도입을 중심으로

> **주제** AI 인프라의 칩 간 데이터 전송(인터커넥트) 기술 동향
> **초점** CPO(Co-Packaged Optics, 광 공동 패키징) 도입
> **작성일** 2026-07-30
> **분류** 기술 동향 리포트

---

## 0. 요약 (Executive Summary)

- **문제**: AI 가속기(GPU/ASIC) 성능은 세대마다 두 배로 늘지만, 이를 잇는 **네트워크 대역폭과 전력**이 병목이 됐다. 800G를 넘어 1.6T 시대로 가면서 기존 **구리(copper) 배선과 플러거블 광모듈**은 전력·손실·밀도 한계에 부딪혔다.
- **해법**: **CPO**는 광 엔진을 스위치 ASIC과 같은 패키지에 통합해, ASIC↔광 사이 전기 배선을 수 cm에서 수 mm로 단축한다. 이를 통해 **비트당 에너지, 채널 손실, 지연**을 대폭 줄인다.
- **핵심 수치**: NVIDIA 기준 1.6T 포트 전력이 플러거블 **30W → CPO 9W(약 70% 절감)**, 채널 손실 **22 dB → 4 dB**. 비트당 에너지는 업계 목표로 **15 → 5 pJ/bit(궁극적으로 <1)**.
- **현황**: 2025년 3월 GTC에서 NVIDIA가 **Quantum-X Photonics(InfiniBand)·Spectrum-X Photonics(Ethernet)**를 공개하며 상용 CPO 스위치가 처음 등장. Broadcom은 **Bailly** 플랫폼으로 개방형 생태계 전략. **2026년이 CPO 본격 양산·롤아웃 원년**으로 평가된다.
- **전망**: CPO 침투율은 2025년 사실상 0%에서 **2030년 35%+**로 급성장, 시장 규모는 **2036년 200억 달러 초과(CAGR 37%)** 전망(IDTechEx).
- **유의점**: 신뢰성·유지보수성(현장 교체 불가)·발열·수율·생태계 종속이 과제. 당장의 대량 배치에는 **LPO(선형 구동 플러거블)**가 현실적 대안으로 병행된다.

---

## 1. 배경: 왜 "칩 간 데이터 전송"이 AI의 병목인가

생성형 AI의 학습·추론은 단일 칩이 아니라 **수천~수만 개의 가속기를 하나처럼 묶은 클러스터**에서 수행된다. 모델·데이터 병렬화 과정에서 가속기들은 끊임없이 파라미터와 활성값을 주고받으며, 이때 **연산 자체보다 칩 간 통신이 전체 성능을 좌우**하는 구간이 많다.

문제는 스케일의 불균형이다.

- **연산(FLOPS)**: 세대마다 급격히 증가
- **인터커넥트 대역폭 요구**: 연산 증가에 비례해 함께 급증 (포트 속도 400G → 800G → **1.6T → 3.2T**)
- **전력·물리 한계**: 대역폭이 오를수록 구리 배선의 손실과 광모듈의 전력이 **비선형적으로 악화**

즉 "칩을 더 빨리 만드는 것"보다 "칩들을 **얼마나 싸고, 낮은 전력으로, 촘촘하게** 잇느냐"가 AI 데이터센터의 핵심 경쟁력이 되었다. CPO는 바로 이 지점을 겨냥한 기술이다.

---

## 2. AI 네트워크의 계층 구조

칩 간 데이터 전송은 거리·목적에 따라 세 계층으로 나눌 수 있으며, CPO는 주로 **스케일업·스케일아웃의 스위치 계층**에 적용된다.

| 계층 | 범위 | 대표 기술 | 특징 |
|------|------|-----------|------|
| **패키지 내(die-to-die)** | 칩렛 간 (mm) | UCIe, 인터포저, 하이브리드 본딩 | 최단거리, 전기 신호 |
| **스케일업(scale-up)** | 노드/랙 내 가속기 묶음 | NVLink, **UALink**, NVSwitch | 초고대역·저지연, 수십~1,024개 도메인 |
| **스케일아웃(scale-out)** | 노드 간 / 클러스터 | InfiniBand, **Ethernet(UEC)** | 대규모 확장, 스위치 패브릭 |

- **스케일업**: NVIDIA **NVLink**가 사실상 표준이었고, 이에 맞서 AMD·Broadcom·Cisco·Intel·Meta·Microsoft 등이 개방형 **UALink** 진영을 형성(1.0 스펙: 200Gbps/lane, 최대 1,024 가속기 도메인, 첫 실리콘 2026~2027 전망).
- **스케일아웃**: **Ultra Ethernet(UEC)**이 AI 트래픽에 최적화된 이더넷 표준을 추진, Broadcom 실리콘 2026~2027 전망.

세대마다 대역폭이 두 배가 되면서 **랙 내부에서도 구리→광 전환**이 불가피해지고 있으며, 스위치 계층의 광 통합 방식으로 CPO가 부상했다.

---

## 3. 기존 방식의 한계: 플러거블 광모듈과 구리

현재 데이터센터 스위치는 전면 패널에 **플러거블 광 트랜시버(QSFP-DD, OSFP 등)**를 꽂는 방식이 지배적이다. ASIC에서 나온 전기 신호가 **PCB 구리 배선 → SerDes → DSP → 광모듈**을 거쳐 광으로 변환된다.

이 구조의 한계:

1. **전력**: 800G 플러거블 모듈은 **12~16W**, 1.6T는 약 30W. 스위치당 수십 개 포트를 곱하면 광통신에만 수 kW가 소모된다. DSP 기반 신호 보상이 전력을 크게 잡아먹는다.
2. **채널 손실**: ASIC↔광모듈까지 수십 cm의 구리 경로에서 고속 신호가 급격히 감쇠(1.6T 링크 기준 약 **22 dB**). 이를 보상하려 더 강한 SerDes·DSP가 필요 → 전력 악순환.
3. **대역폭 밀도**: 전면 패널 면적이 물리적으로 포화. 포트 속도만으로는 스위치 총 대역폭(radix) 확장에 한계.
4. **지연**: DSP 지연이 지연 민감형 AI 집단통신(collective)에 부담.

요약하면, **속도가 오를수록 "전기 신호를 오래 끌고 다니는 비용"이 폭증**한다. 해결의 방향은 명확하다 — **광 변환 지점을 ASIC 최대한 가까이 끌어당기는 것**.

---

## 4. CPO란 무엇인가

**CPO(Co-Packaged Optics)**는 광 엔진(광-전 변환 소자)을 **스위치 ASIC과 동일한 패키지 기판 위에 나란히 통합**하는 방식이다. 광 섬유가 스위치 패키지까지 직접 들어오고, ASIC↔광 엔진 사이 전기 경로가 **수십 cm → 수 mm**로 단축된다.

```
[기존 플러거블]
  ASIC ──(긴 구리 PCB, ~수십 cm)── SerDes/DSP ── 전면패널 광모듈 ── 광섬유

[CPO]
  ┌───────── 동일 패키지 ─────────┐
  ASIC ─(수 mm)─ 광 엔진 ─ 광섬유
  └───────────────────────────────┘
```

핵심 구성 요소:

- **광 엔진 / 실리콘 포토닉스**: 전기↔광 변환. NVIDIA는 **200Gb/s Micro-Ring Modulator(MRM, 마이크로링 변조기)**를 사용해 소형·저전력화.
- **첨단 패키징**: **TSMC COUPE**(Compact Universal Photonic Engine — 마이크로렌즈 표면 결합 + 3D 적층 전자-광 집적(EPIC)), **SoIC + 3D 하이브리드 본딩**으로 고집적 실현.
- **광원(레이저)**: 발열·신뢰성 이유로 외부 레이저(ELS, External Laser Source)를 별도 모듈로 두는 구조가 선호됨.

### 참고: NPO / LPO 와의 위치

- **NPO(Near-Packaged Optics)**: 광 엔진을 ASIC "근처"에 두되 같은 패키지는 아님. CPO의 과도기적 형태.
- **LPO(Linear-drive Pluggable Optics)**: DSP를 제거한 선형 구동 플러거블. 플러거블의 서비스성을 유지하면서 전력을 낮춘 **현실적 절충안**.

---

## 5. CPO의 기술적 이점 (정량)

| 지표 | 플러거블 | CPO | 개선 |
|------|----------|-----|------|
| 1.6T 포트 전력 | ~30W | **~9W** | **약 70% 절감** (NVIDIA) |
| 800G 포트 전력 | ~15W | **~5.5W** | **약 3.5배** (Broadcom) |
| 1.6T 링크 채널 손실 | ~22 dB | **~4 dB** | 대폭 감소 |
| 비트당 에너지 | ~15 pJ/bit | **~5 pJ/bit** | 목표 <1 pJ/bit |

이점의 원천은 **"짧고 손실 없는 전기 경로"** 한 가지로 수렴한다.

1. **전력 효율**: 구리 경로가 짧아 SerDes 구동·DSP 보상 부담이 급감. 데이터센터 규모에서 **전력 = 비용 = 탄소**이므로 직접적 TCO 절감.
2. **대역폭 밀도(radix)**: 전면 패널 제약에서 벗어나 스위치 총 대역폭을 크게 확장. NVIDIA **Quantum-X Photonics는 CPO 모듈 2개로 115.2 Tb/s** 달성.
3. **지연·신뢰성**: 신호 경로 단축으로 지연 감소, 대규모 GPU 집단통신 효율 개선.
4. **확장성**: 수십만~수백만 GPU 규모 "AI 팩토리"를 전력 예산 안에서 연결 가능하게 함.

---

## 6. 주요 업체 동향

### 6.1 NVIDIA — 실리콘 포토닉스 CPO 전면화 (GTC 2025)

2025년 3월 18일 GTC에서 NVIDIA는 CPO를 채택한 실리콘 포토닉스 스위치를 공개하며 사실상 **CPO 상용화의 스타트**를 끊었다.

- **Quantum-X Photonics (InfiniBand)**
  - CPO 모듈 2개로 **총 115.2 Tb/s**
  - 각 모듈: Quantum-X800 ASIC + 광 소자 6개(실리콘 포토닉 엔진 18개)
  - **Quantum-X800 ASIC**: TSMC 4N 공정, **1,070억 트랜지스터**, 28.8 Tb/s
  - **2H25 우선 출시**
- **Spectrum-X Photonics (Ethernet)**
  - **1.6T / 3.2T** 실리콘 포토닉스 CPO
  - **2H26 출시 예정**
- **기술**: 200Gb/s **MRM**으로 전력 3.5배 절감, TSMC **COUPE** 패키징
- **메시지**: "구리 이후(post-copper)" 네트워크로 수백만 GPU AI 팩토리 확장
- **공급망 선점**: 엔비디아는 GTC 2025 생태계 협력을 2026년 지분 투자(Coherent·Lumentum 각 ~$2B, Marvell ~$2B, Corning ~$0.5B, Ayar Labs Series E 등, 광통신에 총 $6.5B+)로 격상해 CPO 공급망을 락인 → 상세는 [`nvidia-supply-chain-investments.md`](nvidia-supply-chain-investments.md)

### 6.2 Broadcom — 개방형 생태계 전략 (Bailly)

스위치 ASIC 1위 사업자인 Broadcom은 **Bailly CPO 플랫폼**을 통해 특정 패키징·포토닉스 파트너에 종속되지 않는 **개방형(open ecosystem)** 접근을 강조한다. Tomahawk 계열 스위치 ASIC과의 결합으로, 하이퍼스케일러가 벤더 선택권을 유지하며 CPO를 도입하도록 유도하는 전략이다. 800G 포트 기준 약 5.5W를 제시한다.

> **NVIDIA vs Broadcom 구도**: NVIDIA는 GPU-스위치-광을 수직 통합한 **폐쇄·최적화형**, Broadcom은 다수 파트너와의 **개방·모듈형**. 두 회사가 스위치 ASIC 시장을 양분하고 있어 CPO 확산의 양대 축이다.

### 6.3 파운드리·패키징 — TSMC

TSMC의 **COUPE**와 **SoIC/3D 하이브리드 본딩**이 CPO 집적의 핵심 인에이블러다. 광 엔진과 전자 칩을 3D로 적층하고, 마이크로렌즈로 광섬유 결합을 단순화한다. CPO의 성패가 **파운드리의 첨단 패키징 역량**에 크게 의존함을 보여준다.

### 6.4 표준·주변 생태계

- **UALink**(스케일업 개방 표준): 1.0 스펙 200Gbps/lane, 1,024 가속기 도메인. 다만 전용 스위치 실리콘(Astera Labs·Marvell 등) 준비 지연으로 초기엔 과도기적 대응. AMD MI400과 함께 **2H26** 본격화 전망.
- **Ultra Ethernet(UEC)**: AI 스케일아웃용 이더넷 표준, Broadcom 실리콘 2026~2027.
- 향후 스케일업 링크에도 광 도입이 논의되며 CPO의 적용 범위가 스위치를 넘어 확장될 가능성.

---

## 7. 비교 분석: CPO vs NPO vs LPO

| 구분 | CPO | NPO | LPO |
|------|-----|-----|-----|
| 광 엔진 위치 | ASIC과 **동일 패키지** | ASIC **근처 기판** | 전면 패널(플러거블) |
| 전력 | 최저 | 중 | 중~저(DSP 제거) |
| 대역폭 밀도 | 최고 | 높음 | 제한적 |
| 유지보수성 | 낮음(현장 교체 불가) | 중간 | **높음(핫스왑)** |
| 성숙도/양산성 | 초기(2025~) | 과도기 | **즉시 배치 가능** |
| 주 적용처 | 초대형 스케일업 AI 클러스터 | 과도기 스위치 | 당장의 800G~1.6T 배치 |

**시사점**: CPO는 최고의 전력·밀도를 주지만 **서비스성과 양산 성숙도에서 아직 대가를 치른다**. 업계는 당분간 **LPO(즉시 배치) + CPO(차세대 최적화)**를 병행하며, 전력·밀도 요구가 극단적인 스케일업 AI 스위칭부터 CPO가 침투하는 경로가 유력하다.

---

## 8. 시장 전망

- **침투율**: CPO는 2025년 사실상 0%에서 **2030년 35% 이상**으로 급성장(IDTechEx).
- **시장 규모**: **2036년 200억 달러 초과**, 2026~2036년 **CAGR 37%**(IDTechEx).
- **변곡점**: 배치 가능한 CPO 제품이 2025년에 처음 등장했고, **2026년이 본격 양산·상용 롤아웃 원년**으로 평가된다.
- **동인**: 초대형 AI 데이터센터의 전력 제약, 1.6T/3.2T 포트 전환, 하이퍼스케일러의 TCO·탄소 목표.

---

## 9. 리스크 / 과제

1. **유지보수성(Serviceability)**: 광 엔진이 스위치에 통합되어 **개별 현장 교체 불가**. 고장 시 스위치 단위 교체 → 운영자 저항 요인. 외부 레이저(ELS) 분리 등으로 완화 시도.
2. **신뢰성·발열**: 레이저·포토닉스는 열에 민감. ASIC 옆 고온 환경에서의 장기 신뢰성 검증이 관건.
3. **수율·비용**: 이종 소자(전자+광)를 한 패키지에 3D 집적 → **패키징 난도·수율**이 초기 비용을 좌우.
4. **생태계 종속**: 특히 NVIDIA 방식은 수직 통합형이라 벤더 락인 우려. Broadcom·UALink의 개방형이 이를 견제.
5. **표준 부재**: 커넥터·광원·인터페이스 표준화 미성숙으로 상호운용성 제약.
6. **대안과의 경쟁**: LPO/LRO가 "충분히 좋은" 저전력·저비용 해법으로 CPO 채택 시점을 늦출 수 있음.

---

## 10. 시사점 / 결론

- 칩 간 데이터 전송은 이제 AI 인프라의 **1차 병목**이며, 전력 효율이 곧 경쟁력이다. CPO는 "**전기 신호를 짧게, 광을 칩 가까이**"라는 단순하지만 강력한 원리로 이 병목을 정면 겨냥한다.
- **2025년 등장, 2026년 양산**이라는 타임라인이 확인됐다. NVIDIA가 최적화·수직통합으로 선도하고, Broadcom·UALink가 개방형으로 대응하는 **양강 구도**가 확산 속도를 결정할 것이다.
- 다만 CPO는 **일괄 대체가 아니라 점진적 침투**다. 서비스성·수율 과제 때문에, 당분간 **LPO와 공존**하며 전력·밀도 요구가 가장 극단적인 스케일업 AI 스위칭부터 자리를 넓힐 전망이다.
- **공급망 관점**의 관전 포인트: (1) TSMC 등 **첨단 패키징(COUPE·SoIC) 역량**, (2) 실리콘 포토닉스·**외부 레이저(ELS)** 공급, (3) 광섬유 결합·커넥터 표준화, (4) 스위치 ASIC 양강(NVIDIA·Broadcom)의 로드맵. CPO의 병목은 소자가 아니라 **패키징과 생태계**에 있다.

---

## 참고 문헌

1. IDTechEx, "Co-Packaged Optics Race: Strategic Approaches from NVIDIA and Broadcom", https://www.idtechex.com/en/research-article/co-packaged-optics-race-strategic-approaches-from-nvidia-and-broadcom/34467
2. IDTechEx, "Co-Packaged Optics (CPO) 2026-2036: Technologies, Market, and Forecasts", https://www.idtechex.com/en/research-report/co-packaged-optics-cpo/1138
3. NVIDIA, "NVIDIA Announces Spectrum-X Photonics Co-Packaged Optics Networking Switches to Scale AI Factories to Millions of GPUs" (GTC 2025), https://investor.nvidia.com/news/press-release-details/2025/NVIDIA-Announces-Spectrum-X-Photonics-Co-Packaged-Optics-Networking-Switches-to-Scale-AI-Factories-to-Millions-of-GPUs/default.aspx
4. optics.org, "Nvidia reveals plan to scale AI 'factories' with co-packaged optics", https://optics.org/news/16/3/26
5. LightCounting, "Nvidia's CPO is the First Step in a Long Journey" (2025.03), https://www.lightcounting.com/research-note/march-2025-nvidias-cpo-is-the-first-step-in-a-long-journey-395
6. APNIC Blog, "Co-Packaged Optics — a deep dive" (2025.05), https://blog.apnic.net/2025/05/07/co-packaged-optics-a-deep-dive/
7. Asterfusion, "1.6T Switch Era: Choosing Between CPO, NPO, And LPO For Next-Gen AI Networks", https://cloudswit.ch/blogs/1-6t-switch-choose-between-cpo-npo-and-lpo/
8. LINK-PP, "Co-Packaged Optics (CPO) vs Pluggable: 800G+ Scaling Limits", https://www.link-pp.com/resources/strategy/cpo-vs-pluggable-800g-architecture/
9. Synopsys, "Ultra Ethernet and UALink: Scalable AI Networks", https://www.synopsys.com/articles/ultra-ethernet-ualink-ai-networks.html
10. UALink Consortium, "An Open, High-Efficiency Scale-Up Interconnect for AI" (2026.01)
11. HPCwire, "Upscale AI Eyes Late 2026 for Scale-Up UALink Switch" (2025.12), https://www.hpcwire.com/2025/12/02/upscale-ai-eyes-late-2026-for-scale-up-ualink-switch/
12. Tom's Hardware, "Inside optical and the battle for scale — how the AI industry is racing to integrate photonic interconnects", https://www.tomshardware.com/tech-industry/inside-optical-and-the-battle-for-scale-how-the-ai-industry-is-racing-to-integrate-photonic-interconnects

> 수치·출처 상세는 [`research/ai-network-cpo/sources.md`](../../research/ai-network-cpo/sources.md) 참조.
