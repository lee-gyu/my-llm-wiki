---
type: concept
title: Code Review
created: 2026-07-03
updated: 2026-07-03
sources: [20260703-google-code-review.md, 20260703-artificial-adventures.md, 20260703-rules-engineering-leaderhsip.md]
tags: [code-review, engineering-practices, ai-coding]
status: current
---

# Code Review

동료 개발자가 작성한 변경사항(CL)을 병합 전에 검토해 코드 상태(code health)를
유지·개선하는 소프트웨어 엔지니어링 실천.

## Explanation
Google의 엔지니어링 실천 가이드에 따르면 코드 리뷰의 핵심 기준은 "완벽함"이
아니라 "그 변경이 전체 코드 상태를 확실히 개선하는가"이다. 완벽한 코드는
존재하지 않고 더 나은 코드가 있을 뿐이므로, 사소한 다듬기 문제로 승인을
지연시키기보다 "Nit:" 같은 라벨로 비필수 제안임을 표시한다
(source: [[sources/2026-07-03-google-code-review]]).

리뷰어가 확인해야 할 항목은 설계, 기능, 복잡도(특히 과잉 설계), 테스트,
네이밍/주석("왜"를 설명해야 함), 스타일 일관성, 문서화로 나뉜다. CL을 훑어볼 때는
먼저 변경이 존재해야 하는지 큰 그림을 판단하고, 논리적 변경이 가장 큰 파일부터
검토해 근본적 설계 문제를 조기에 잡아낸다
(source: [[sources/2026-07-03-google-code-review]]).

리뷰 속도는 개인의 작업 속도보다 팀 전체의 속도(velocity)를 우선시하는 관점에서
중요하게 다뤄진다. 리뷰 요청에는 영업일 기준 1일 이내에 응답해야 하며, 핵심은
전체 사이클을 빨리 끝내는 것보다 "빠른 응답"이다. 코멘트는 코드에 대해서만
정중하게 작성하고, 이유를 함께 설명하며, 문제 해결의 책임은 개발자에게 남겨둔다
(source: [[sources/2026-07-03-google-code-review]]).

개발자가 리뷰 의견에 반발할 때는 먼저 상대가 맞을 가능성을 진지하게 고려하되,
스스로 판단에 근거가 있다면 정중하게 계속 주장해야 한다. "나중 CL에서 정리하겠다"는
요청은 실제로 지켜지지 않는 경우가 많아 권장되지 않는다
(source: [[sources/2026-07-03-google-code-review]]).

한편 사람이 아니라 AI(LLM)가 리뷰어 역할을 하는 사례도 보고된다. 한 개인 개발자는
"git diff main을 리뷰해서 버그를 찾아줘" 정도의 단순한 프롬프트만으로도 지금까지
AI 도구에서 얻은 것 중 "가장 압도적으로 가치 있는" 용도가 코드 리뷰였다고 평가하며,
frontier 모델(opus)이 fuzzer도 놓친 double-free 버그를 발견한 사례를 든다. 다만
저가형 모델은 확신에 찬 허풍을 자주 내놓고, 검증은 여전히 사람이 상세히 읽어야
한다고 지적한다
(source: [[sources/2026-07-03-artificial-adventures]]; 자세한 내용은
[[concepts/ai-coding-assistants]]).

조직 규모에서 AI 리뷰어를 상시 운영에 편입한 사례도 보고된다. Imprint에서는 "1차
코드 리뷰를 변경을 구현한 것과 같은 하네스가, 그 변경을 작성할 때 쓴 맥락을 비운
상태로 수행"해 사람은 더 높은 가치의 피드백에 집중하도록 한다. 저자는 좋은 하네스의
1차 리뷰가 사람의 1차 리뷰보다 빠르고 효과적이라고 평가하되, 고위험 영역은 여전히
사람이 처리해야 한다고 본다
(source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]; 자세한
내용은 [[concepts/engineering-leadership]]).

## Positions and disagreements
아직 기록된 상반된 입장은 없다. Google 가이드는 사람 리뷰어의 표준·속도·태도를
다루고, artificial-adventures와 revised-rules-of-engineering-leadership 두 소스는
AI(하네스)가 리뷰어 역할을 하는 사례(각각 개인·조직 규모)를 다뤄 서로 다른
각도지만 상충하지는 않는다.

## See also
- [[concepts/ai-coding-assistants]] — AI 코딩 도구 전반의 효용과 한계(코드 리뷰는
  그 중 한 활용처)
- [[concepts/engineering-leadership]] — 하네스 기반 1차 코드 리뷰를 조직의 프로세스
  자동화 원칙 중 하나로 다룬다.
