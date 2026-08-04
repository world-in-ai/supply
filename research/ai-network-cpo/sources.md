# 리서치 노트 — AI 네트워크 / CPO

> 보고서 `reports/2026-07_ai-network-cpo/` 의 근거 자료 및 핵심 수치 메모.
> 리서치 기준일: 2026-07-30

## 핵심 수치 (본문 인용 근거)

| 항목 | 수치 | 비고 / 출처 |
|------|------|-------------|
| CPO 전력 효율(비트당 에너지) | 15 → 5 pJ/bit (목표 <1) | IDTechEx |
| Broadcom CPO 포트 전력(800G) | 약 5.5W (플러거블 ~15W) | Broadcom, ~3.5x 개선 |
| 1.6T 링크 채널 손실 | 22 dB → 4 dB | LINK-PP 등 |
| 1.6T 링크 전력 | 30W → 9W (약 70% 절감) | NVIDIA GTC 2025 |
| NVIDIA Quantum-X Photonics | 115.2 Tb/s (CPO 모듈 2개) | GTC 2025.03.18 |
| Quantum-X800 ASIC | TSMC 4N, 1,070억 트랜지스터, 28.8Tb/s | |
| 변조기 | 200Gb/s Micro-Ring Modulator(MRM) | |
| CPO 침투율 전망 | 2025 ~0% → 2030 35%+ | IDTechEx |
| CPO 시장 규모 | 2036년 200억 달러 초과, CAGR 37%(2026~36) | IDTechEx |
| UALink 1.0 | 200Gbps/lane, 최대 1,024 accelerator 도메인 | UALink Consortium |

## 제품·일정 타임라인

- **2025.03 GTC**: NVIDIA Quantum-X Photonics(InfiniBand), Spectrum-X Photonics(Ethernet) 발표
- **2H25**: InfiniBand CPO(Quantum-X) 우선 출시
- **2H26**: Ethernet CPO(Spectrum-X, 1.6T/3.2T) 출시 예정
- **2026**: CPO 본격 양산·상용 롤아웃 원년으로 평가
- **2026~2027**: UALink / Ultra Ethernet(UEC) 실리콘 등장 전망

## 기술 스택 메모

- **TSMC COUPE** (Compact Universal Photonic Engine): 마이크로렌즈 표면 결합 + 3D 적층 전자-광 집적(EPIC)
- **TSMC SoIC** + 3D 하이브리드 본딩: 고집적 패키징
- 대안 기술: **NPO**(Near-Packaged Optics), **LPO**(Linear-drive Pluggable Optics), **LRO**

## 출처 목록

1. IDTechEx, "Co-Packaged Optics Race: Strategic Approaches from NVIDIA and Broadcom", https://www.idtechex.com/en/research-article/co-packaged-optics-race-strategic-approaches-from-nvidia-and-broadcom/34467
2. IDTechEx, "Co-Packaged Optics (CPO) 2026-2036: Technologies, Market, and Forecasts", https://www.idtechex.com/en/research-report/co-packaged-optics-cpo/1138
3. NVIDIA Investor, "NVIDIA Announces Spectrum-X Photonics Co-Packaged Optics Networking Switches", https://investor.nvidia.com/news/press-release-details/2025/NVIDIA-Announces-Spectrum-X-Photonics-Co-Packaged-Optics-Networking-Switches-to-Scale-AI-Factories-to-Millions-of-GPUs/default.aspx
4. optics.org, "Nvidia reveals plan to scale AI 'factories' with co-packaged optics", https://optics.org/news/16/3/26
5. LightCounting, "Nvidia's CPO is the First Step in a Long Journey" (2025.03), https://www.lightcounting.com/research-note/march-2025-nvidias-cpo-is-the-first-step-in-a-long-journey-395
6. APNIC Blog, "Co-Packaged Optics — a deep dive" (2025.05), https://blog.apnic.net/2025/05/07/co-packaged-optics-a-deep-dive/
7. Asterfusion, "1.6T Switch Era: Choosing Between CPO, NPO, And LPO", https://cloudswit.ch/blogs/1-6t-switch-choose-between-cpo-npo-and-lpo/
8. LINK-PP, "Co-Packaged Optics (CPO) vs Pluggable: 800G+ Scaling Limits", https://www.link-pp.com/resources/strategy/cpo-vs-pluggable-800g-architecture/
9. Synopsys, "Ultra Ethernet and UALink: Scalable AI Networks", https://www.synopsys.com/articles/ultra-ethernet-ualink-ai-networks.html
10. UALink Consortium, "An Open, High-Efficiency Scale-Up Interconnect for AI" (White Paper, 2026.01), https://ualinkconsortium.org/
11. HPCwire, "Upscale AI Eyes Late 2026 for Scale-Up UALink Switch" (2025.12), https://www.hpcwire.com/2025/12/02/upscale-ai-eyes-late-2026-for-scale-up-ualink-switch/
12. Tom's Hardware, "Inside optical and the battle for scale", https://www.tomshardware.com/tech-industry/inside-optical-and-the-battle-for-scale-how-the-ai-industry-is-racing-to-integrate-photonic-interconnects
