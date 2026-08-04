# 글로벌파운드리스(GlobalFoundries) CPO/실리콘 포토닉스 동향 — 리서치 브리프

> 목적: GF의 CPO·광반도체 위치를 정확히 정리 — 워드 최종본용 재료
> 작성일 2026-08-03 · 리서치 기준일 2026-08-03
> 상위: [`foundry-packaging-brief.md`](foundry-packaging-brief.md) / 본편 [`report.md`](report.md)

## TL;DR
- GF는 **광반도체(실리콘 포토닉스) 전문 파운드리** — **광학칩(PIC)을 2018년부터 실제 양산**한 유일 업체(4사 중), AMF 인수로 **세계 최대 순수 SiPh 파운드리**.
- CPO는 **"merchant CPO provider"** 지향 — 남의 프로세서에 붙는 **광엔진(SCALE) 모듈을 제조·판매**. 단 **대형 로직 결합(CoWoS급)은 안 하고 고객이 함**.
- ⚠️ **CPO 본격 양산 시점은 GF 공식 미발표** — "2028말~2029 변곡점" 등은 trade press/실적 콜 코멘터리뿐(공식 실적 press release 미기재). 사실로 단정 금지.

## 핵심 팩트 / 수치 (검증 완료)
| 항목 | 내용 | 출처 등급 |
|------|------|-----------|
| **광학칩(PIC) 양산 시작** | **2018년**(90WG, 첫 90nm SiPh 300mm) → Fotonix 출시 '22 → 양산 램프 '24 | 2급(권위 trade) |
| **현재 위상** | **세계 최대 순수 실리콘 포토닉스 파운드리**(AMF 인수 후) | 2급 |
| **기술 계보** | IBM 마이크로일렉트로닉스 인수('15)로 확보 → 자체 상용화(Fotonix '22) → **AMF 인수('25.11)로 확장** | 1급(GF 공식) |
| **CPO 제품** | **SCALE**(광엔진 모듈) 출시 '26.5 — 업계 첫 OCI MSA 호환, 8λ/16λ DWDM | 1급(GF 공식) |
| **3D 하이브리드 본딩 대상** | **PIC + EIC**(광엔진 내부 결합) — 구리-구리 다이본딩, sub-10µm 피치, 솔더 없이 | 2급 |
| **OFC 2026 CPO 파트너십** | SENKO(wafer-level detachable fiber), **Corning+GF+EXFO(CPO 생태계)**, Siluxtek(200G/lane SiPh 수신칩 GF 공정 제조) | **1급(GF Q1'26 실적)** |
| **CPO 양산 전망** | (하향) "2028말~2029 변곡점·SiPh 매출 '28 $1B"은 **trade press/실적 콜 코멘터리**뿐 — **GF 공식 실적 press release엔 미기재**. 사실로 단정 금지 | ⚠️ 미검증 |
| **CHIPS 보조금** | 美 상무부 **3억 달러 지원 의향서(LOI) 체결('26.7.29)**, 정부 ~1% 지분 (SiPh 웨이퍼·광소재·패키징·NPO/CPO) | 1급(GF 공식) |

## 포지션 — "광엔진까지, 로직 결합은 고객"
CPO 제조를 3층위로 나누면 GF의 역할이 명확:
```
① PIC + EIC ─3D 하이브리드 본딩(GF)→ ② 광엔진(SCALE)
                                         ↓ + 로직(스위치/AI ASIC) — 고객이 CoWoS급으로 결합
                                       ③ CPO 완성
```
- **GF가 하는 것**: PIC·EIC 자사 제조 → **광엔진(SCALE)까지** (2.5D/3D 본딩 보유)
- **고객이 하는 것**: 광엔진을 자기 스위치/AI ASIC과 **co-package**(SCALE은 CoWoS-S/L 호환 설계)
- **EMIB/CoWoS급 대형 로직-광 결합 플랫폼은 GF 자체 없음** — TSMC(CoWoS)·인텔(EMIB)이 그 captive 시장 지배

## 유리(glass) 관련 — 구분 필요
- **유리기판(glass CORE substrate, 패키지 기판)**: GF **미참여** (삼성전기·SK Absolics·인텔·TSMC 경쟁 밖)
- **유리 도파관(glass WAVEGUIDE)**: **Corning과 'GlassBridge' 협력** — 광섬유↔PIC 결합용(detachable fiber), 패키지 기판 아님
- → "GF가 유리기판 한다"는 부정확. "유리 도파관(광 결합)은 협력, 유리기판은 미참여"가 정확.

## 워드용 문구 (사실 기반)
> "글로벌파운드리스 : 광학칩(PIC)을 2018년부터 양산해온 실리콘 포토닉스 전문 파운드리 — Ayar Labs·Lightmatter 등 팹리스 광기업 제조처(엔비디아 공급망 연결). CPO는 광엔진(SCALE) 공급형(merchant) 전략, 美 CHIPS 3억 달러 보조금 의향서 체결('26.7)"
- 각주: 대형 로직 결합(CoWoS급)은 고객 몫 / CPO 본격 양산 시점은 GF 공식 미발표(보도는 '28말~'29 언급) / 유리기판(패키지 기판)은 미참여

## 출처 (등급)
- **1급(GF 공식)**: SCALE 발표 https://gf.com/gf-press-release/globalfoundries-accelerates-adoption-of-co-packaged-optics-for-advanced-ai-data-centers-with-scale-optical-module-solution/ / CHIPS LOI https://gf.com/news-and-events/news/globalfoundries-signs-letter-of-intent-with-the-us-department-of-commerce-for-a-300-million-award-to-accelerate-us-silicon-photonics-leadership/ / AMF 인수·실리콘포토닉스 https://gf.com/technologies/silicon-photonics/
- **2급(권위 trade)**: Tom's Hardware(CPO 파운드리 로드맵·역할분담) https://www.tomshardware.com/tech-industry/artificial-intelligence/co-packaged-optics-cpo-foundry-roadmaps-breaking-down-tsmc-intel-samsung-and-globalfoundries-approach-to-next-generation-scale-up-connectivity / TrendForce(SiPh 매출·AMF) / Digitimes / Techtimes(3D 하이브리드 본딩 PIC+EIC) / optics.org(Corning GlassBridge) https://optics.org/news/16/9/49 / The Register(CHIPS 1% 지분)
- **참고**: Forbes·Moor(2020, "GF 조용히 SiPh 제조 강자") https://www.forbes.com/sites/moorinsights/2020/03/31/globalfoundries-has-quietly-become-a-player-in-silicon-photonics-manufacturing/

> 주의: "CPO 양산 2028말~2029"는 **GF 공식 실적 press release(EX-99.1) 미기재** — trade press/실적 콜 코멘터리 수준. GF 공식 "CPO 양산 연도" 발표는 없음. CHIPS 3억 달러는 **의향서(LOI)** 단계로 최종 확정 아님.
