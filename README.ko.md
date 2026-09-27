
> 원본 권위 고지: 본 기술 명세의 최상위 법적·공학적 권위는 한글 원본(README.ko.md)에 있습니다. README.md는 보조 영문 참고본입니다. 불일치 시 한글 원본이 우선합니다.
> 
Machine-Tools-Edge-Safety-Paper
> [상위 범용 아키텍처 연계 고지] 본 백서는 범용 공작기계 최상위 마스터 저장소로서, 산하 하위 백서(Sub-Whitepaper)들을 총괄 연계 및 통제하며, 최상위 거점 soma-moa의 철학과 연동하여 구동됩니다.
> 
1. 개요 및 확장 서사
본 백서 체계는 초기부터 거대한 단일 통합 안전 시스템으로 기획된 것이 아니라, 프레스·절곡기·절단기 부문의 에지 안전장치 설계(Press-Brake-Shear 백서)라는 명확한 단일 과제에서 출발하였습니다.
가공 현장의 실제 협착·비산·말림 위험 요소를 분석하는 과정에서, 단일 위험 요소에 대한 방어 기법이 회전체 근접 감지, NC 제어 클램프 간섭, 휴대용 절단 공구의 반동 완화 등 다변화된 공작기계 환경으로 자연스럽게 확장·분화되었습니다.
 * 최초 출발점: 프레스·절곡기·절단기 중심의 정교한 에지 안전 아키텍처 정립 (Press-Brake-Shear 백서)
 * 범용 분화: 회전축 말림 및 근접 감지 메커니즘의 특수성을 고려하여 독립 범용 프로젝트(Universal 시리즈 1호)로 분리
 * 영역 확장: 고정형 전통 공작기계(선반·밀링 등), NC 판금 제어(터렛펀치), 휴대용 연삭기(그라인더) 등으로 위험 모델별 전문화 진행
2. 백서 체계 및 위치 구조
본 저장소 내부에 직접 위치하는 하위 백서 폴더(각 폴더 내 README.ko.md 한글 원본 및 README.md 영문 참고본 탑재)와, 외부 최상위 리포지토리로 연계되는 독자 백서의 위치 및 편제 정보는 다음과 같습니다.
 * Lathe-Milling-Drillpress-Edge-Safety-Paper — ./Lathe-Milling-Drillpress-Edge-Safety-Paper/README.ko.md (마스터 리포 내 하위 폴더 / 고정형 공작기계 부문 2번 백서)
 * Sheet-Metal-NC-Punch-Clamp-Avoidance-Safety-Architecture — ./Sheet-Metal-NC-Punch-Clamp-Avoidance-Safety-Architecture/README.ko.md (마스터 리포 내 하위 폴더 / NC 터렛펀치 클램프 간섭 회피 안전 아키텍처)
 * Grinder-Portable-Cutting-Tool-Safety-Architecture — ./Grinder-Portable-Cutting-Tool-Safety-Architecture/README.ko.md (마스터 리포 내 하위 폴더 / 소형 및 휴대용 절단·연삭 공구 안전 아키텍처)
 * Press-Brake-Shear-Edge-Safety-Paper — [https://github.com/deundeuni/Press-Brake-Shear-Edge-Safety-Paper](https://github.com/deundeuni/Press-Brake-Shear-Edge-Safety-Paper) (별도 최상위 독립 리포지토리 / 고정형 공작기계 부문 하위 백서 1 / 특허 검증 완료 원안)
 * Universal-Rotating-Machinery-Entanglement-Safety-Architecture — [https://github.com/deundeuni/Universal-Rotating-Machinery-Entanglement-Safety-Architecture](https://github.com/deundeuni/Universal-Rotating-Machinery-Entanglement-Safety-Architecture) (별도 최상위 독립 리포지토리 / Machine-Tools 산하가 아닌 범용 회전체 말림 방지 Universal 1호 프로젝트)
3. 사고 확장 순서에 따른 세부 백서 개요
 * 프레스·절곡기·절단기 안전 백서 (Press-Brake-Shear)
   * 주요 내용: 수평·수직 직선 운동에 따른 협착 및 절단 위험 지역을 비전 및 에지 센서로 방어하는 아키텍처로, 특허 검증이 완료된 출발점 백서입니다.
   * 참조: 상위 고정형 공작기계 부문 하위 백서 1로 연계 선언되어 있습니다.
 * 회전체 신체 근접·말림 감지 백서 (Universal-Rotating)
   * 주요 내용: 고속 회전축 및 주축 부위의 신체/의복 말림 위험을 초고속 에지 컴퓨팅으로 감지하는 메커니즘입니다.
   * 참조: 특정 공작기계에 국한되지 않는 범용 공통 모듈로 분화하여 독립 프로젝트로 운용됩니다.
 * 선반·밀링·드릴프레스·연삭기 백서 (Lathe-Milling-Drillpress)
   * 주요 내용: 고정형 공작기계 부문 2번 백서로, 회전 가공 중 칩 비산, 치공구 접촉, 가공물 탈락 위험을 완화하기 위한 멀티 센서 퓨전 안전 아키텍처입니다.
 * NC 터렛펀치 클램프 간섭 회피 백서 (Sheet-Metal-NC-Punch)
   * 주요 내용: 판금 가공 시 고속 이동하는 NC 클램프와 펀칭 금형 간의 충돌 및 작업자 영역 침범을 동적으로 계산하여 회피 및 제동을 유도하는 시스템입니다.
 * 그라인더·절단기 안전 백서 (Grinder-Portable-Cutting-Tool)
   * 주요 내용: 핸드헬드 및 소형 가공기에서 발생하는 숫돌 파손, 비산, 킥백(Kickback) 및 반동 발생 시 작업을 신속히 제어하여 상해를 완화하는 휴대형 에지 아키텍처입니다.
4. 백서 간 상위 연계 및 운용 원칙
 * 상위 연계 고지 명시: 각 하위 백서는 독립된 폴더 또는 별도 리포지토리로 존재하더라도 서두에 "Machine-Tools-Edge-Safety-Paper 하위 백서"임을 명시하여 종합 안전 아키텍처 내의 위치를 고지합니다.
 * 상세 조항 위임: 본 README는 전체 사고 확장 서사와 하위 백서 간의 연계 구조만을 정의하며, 세부적인 제어 알고리즘, 특허 청구 범위, 센서 배치 및 인터페이스 명세는 각 하위 백서 본문에 위임합니다.
 * 원본 우선 조항: 본 백서 및 산하 모든 하위 문서의 기준 원본은 한국어 원문(Korean Original / README.ko.md)입니다. 타 언어 번역본(README.md 등)은 이해를 돕기 위한 참고용(Reference Only) 문서이며, 해석상 차이가 존재할 경우 한국어 원문의 내용과 의도를 우선 적용합니다.
 * 사업화 내용 분리: 본 백서 원안에는 순수 기술적 개념, 센싱 아키텍처, 위험 모델 및 선행기술 원용 범위만을 다룹니다. 특정 제품화 명세, 상업적 비즈니스 모델, 수익 구조 등 사업화 관련 사항은 백서 원안에서 제외하며 별도의 문서로 작성 및 관리합니다.
 * 저장소 계정 편제에 관한 안내: 본 백서 체계 산하의 모든 저장소는 현재 설계자 개인 계정(deundeuni) 아래 운용되고 있습니다. 향후 프로젝트 성격이나 운영 필요에 따라 특정 저장소는 별도 조직 계정(예: soma-moa, deundeunilab 등)으로 이관될 수 있으며, 이관 시점의 최신 위치는 각 저장소 자체의 안내 또는 상위 마스터 리포지토리의 갱신된 링크를 따릅니다. 계정 소재지 변경은 본 백서의 기술적 내용이나 방어적 공개의 효력에 영향을 미치지 아니합니다.
5. 설계자 독자 아키텍처 선언, 유틸리티 활용 및 기술적 표기 방침
 * 설계 철학 및 기술 조합의 독자성 (Architectural Conception & Human-in-the-Loop): 본 아키텍처 규격의 모든 기술적 공학 구상, 시스템 경계 설정, 안전 제어 논리 및 핵심 메커니즘 정립은 설계자(deundeuni)의 주도적 결정(Human-in-the-Loop)하에 독자적으로 이루어졌습니다. 본 아키텍처의 통합 설계 권한은 설계자(deundeuni)에게 있습니다.
 * 소프트웨어 유틸리티 활용에 관한 명시 (Software Utility Limitation): 본 문서 작성 과정에서 활용된 도구는 설계자가 정의한 아키텍처 논리와 엣지 자율 제어 범주를 바탕으로 포맷팅 및 문맥 정제를 수행한 수동적 실행 유틸리티(Software Utility)에 국한됩니다.
 * 방어적 표현 적용 (겸양 고지): 본 아키텍처 및 산하 백서에서 언급하는 모든 안전 장치와 감지 알고리즘은 절대적 방어나 물리적 한계를 뛰어넘는 완벽성을 다투는 것이 아닙니다. 센서 오작동, 환경적 변수, 기계적 관성 등을 고려하여 '위험 완화', '사고 가능성 저감', '안전성 향상 지향' 등 방어적 개념으로 정의합니다.
 * 선행기술 원용 범위 확장: 각 백서에서 사용되는 상위 기술 개념(예: 센서, 제어기, 에지 컴퓨팅 등)은 특정 하드웨어 스펙에 갇히지 않도록 포괄적·광의의 개념으로 정의함으로써 선행기술 원용 및 지식재산권 범위 확장을 도모합니다.
6. 상위개념 포괄 및 구현 유연성 선언
 * 상위개념 포괄 선언: 본 마스터 백서에 제시된 사고 확장 서사, 계층적 편제 구조, 및 하위 백서군과의 인터록 연계 구조는 개별 공작기계 형태나 가공 스케일의 변화에 관계없이 상위 선행기술 범위로 포괄 적용됩니다.
 * 구현 유연성 및 시장 맞춤형 확장 선언 (Design-to-Cost Flexibility): 본 명세서의 하드웨어 구성 및 레이어 구조는 최적 성능을 발휘하는 일 실시예를 예시한 것입니다. 실제 양산 및 현장 적용 환경에서는 시장의 수요, 경제성, 가공 소재 및 운용 조건에 따라 특정 모듈 및 센서 구성의 선택적 생략, 축소, 스케일링 또는 커스텀 최적화가 유연하게 가능하며, 이러한 기능적 변형 및 등가 구현 역시 본 선행기술 공개 범주에 포괄 적용됩니다.
7. 실리보호, 법적 적용 범위 이원화 및 면책 고지
 * 원안 우선 원칙 (Korean Original Supremacy): 본 기술 명세 및 마스터 체계의 최상위 법적·공학적 권위는 한국어 원문(README.ko.md)에 있습니다. 기타 언어 번역본(README.md)은 보조 참고본이며, 내용상 불일치나 해석의 차이가 발생할 경우 한국어 원문이 우선합니다.
 * 저작권 및 표준 라이선스 이원화 적용 (LICENSE 파일 연동): 본 저장소의 문서, 명세, 아키텍처 청사진 등 텍스트 표현물에는 Creative Commons Attribution 4.0 International (CC BY 4.0)을 적용하고, 파생 코드 및 실행 구현물에는 Apache License 2.0 (Apache-2.0)을 이원화 적용합니다. 상세 SPDX 표준 식별자(SPDX-License-Identifier: CC-BY-4.0 AND Apache-2.0) 및 법적 조건은 본 저장소 루트의 LICENSE 파일을 따릅니다. 기존 커스텀 "DPL v1.0 (Defensive Patent License v1.0)" 고지는 2026년 9월 27일 자로 본 표준 라이선스 체계(CC BY 4.0 & Apache-2.0)로 전면 대체되었습니다.
 * 영업비밀 보호 및 구현체 분리 명시: 본 공개 백서는 상위 아키텍처 사상과 개념적 메커니즘 개시를 목적으로 하며, 실제 현장 캘리브레이션 파라미터(임계치), eFPGA RTL 회로 설계도, 정밀 CAD 파일, 양산 펌웨어 바이너리는 영업비밀(Trade Secret)로 별도 비공개 유지합니다. 개념 실증용(PoC) 참조 코드는 오프라인 레포지토리 자산으로 독자 분류·보관합니다.
 * 설계자의 상용화 권고, 법적 안전인증 준수 및 FTO 재검증 책임 귀속: 본 백서는 설계자(deundeuni)가 고난도 현장의 재해 예방을 위해 정립한 공학적 구상 및 선행기술 방어 백서입니다. 설계자는 본 아키텍처를 바탕으로 실제 장치를 제작·구현하려는 모든 후속 개발자 및 사업자가 해당 국가의 법적 안전인증(대한민국 KCs 의무/자율안전확인신고, CE, UL, OSHA 등)을 엄격히 취득하고, 기존 선행특허 및 FTO(Freedom to Operate) 최신 상태를 재검증하여 안전하게 상용화할 것을 권고합니다. 본 마스터 백서 자체는 인증받은 상용 완제품이 아닌 개념적 기술 사상의 개시물이므로, 실제 구현 과정에서의 법적 안전인증 취득, 선행특허 FTO 재검증, 위험성 평가 및 기능안전(SIL/PL) 검증 의무는 전적으로 '실제 구현 및 운용 주체'에게 귀속됩니다.
 * 개념적 방향성 정의, AS-IS 제공 및 면책 고지: 본 마스터 백서 및 서사 정리 내용 역시 선행기술 방어 공표 및 기술적 방향성 제시(Directional Guidance)를 유일한 목적으로 하며, 현장에 즉각 적용 가능한 물리적 완결성이나 시제품 동작을 직접 보증하지 아니합니다(AS-IS 제공). 설계자(deundeuni)는 본 문서에 개시된 논리를 원용하여 제작된 장치나 하위 백서 연계 적용으로 인해 발생할 수 있는 예기치 않은 신체적·재산적 손실에 대해 법적 책임(Liability)을 부담하지 아니하며, 실제 현장 적용 시의 모든 공학적 검증과 안전 담보 책임은 해당 시공·운용 주체에게 있습니다.
 * 비의도적 생략 및 예시적 미한정 고지 (Non-Intentional Omission & Non-Exhaustive Disclaimer): 본 명세서 및 하위 서사 개요에 인용되거나 열거된 기술 표준, 공지 원리, 법령, 하위 저장소 위치 및 관련 규격은 이해를 돕기 위한 예시적 서술이며 전면적·고착적 한정을 의미하지 아니합니다. 작성자의 주관적 한계나 인지적 착오로 인해 특정 세부 규격, 하위 백서의 최신 변경 사항, 관련 산업 표준 또는 균등 선행기술의 명시가 누락되거나 비의도적으로 생략되었을 수 있으나 이는 의도적인 은폐나 배척이 아닙니다. 최신 백서 세부 조항은 각 하위 백서 원문 본문을 따르며, 개시된 상위 기술 사상과 연결되는 모든 파생 표준, 개정 규격, 균등 기구 및 공지기술 조합은 본 방어적 공개 백서의 선행기술 포괄 범주에 포함된 것으로 간주합니다.
 * 방어적 공표 및 선사용권 병행: 본 백서는 방어적 선행기술(Prior Art) 공표를 1차 목적으로 하며, 대한민국 특허법 제103조 및 미국 특허법 35 U.S.C. §273에 따른 선사용권 확립을 위해 독자적인 설계도·시제품·개발 기록을 오프라인으로 병행 관리합니다.
8. 출처 및 관련 저장소
 * Machine-Tools-Edge-Safety-Paper (마스터 리포지토리): [https://github.com/deundeuni/Machine-Tools-Edge-Safety-Paper](https://github.com/deundeuni/Machine-Tools-Edge-Safety-Paper)
 * Press-Brake-Shear-Edge-Safety-Paper (고정형 1호 백서): [https://github.com/deundeuni/Press-Brake-Shear-Edge-Safety-Paper](https://github.com/deundeuni/Press-Brake-Shear-Edge-Safety-Paper)
 * Universal-Rotating-Machinery-Entanglement-Safety-Architecture (범용 1호 백서): [https://github.com/deundeuni/Universal-Rotating-Machinery-Entanglement-Safety-Architecture](https://github.com/deundeuni/Universal-Rotating-Machinery-Entanglement-Safety-Architecture)
 * Lathe-Milling-Drillpress-Edge-Safety-Paper: ./Lathe-Milling-Drillpress-Edge-Safety-Paper/README.ko.md
 * Sheet-Metal-NC-Punch-Clamp-Avoidance-Safety-Architecture: ./Sheet-Metal-NC-Punch-Clamp-Avoidance-Safety-Architecture/README.ko.md
 * Grinder-Portable-Cutting-Tool-Safety-Architecture: ./Grinder-Portable-Cutting-Tool-Safety-Architecture/README.ko.md
부록 A. 제개정 이력 (Revision History)
 * 2026-09-27: 라이선스 표기를 2026-09-27자로 표준 라이선스(CC BY 4.0 & Apache-2.0 이원화 체계)로 재편하고 저장소 루트의 LICENSE 파일과 정밀 연동함. 기존 커스텀 DPL v1.0 표기를 공식 대체하며, 변경 이력 자체도 방어적 공개 기록의 일부로 지속 보존을 도모함.
