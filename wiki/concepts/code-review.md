---
type: concept
title: Code Review
created: 2026-07-03
updated: 2026-07-03
sources: [20260703-google-code-review.md]
tags: [code-review, engineering-practices]
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

## Positions and disagreements
아직 다른 소스가 없어 기록된 상반된 입장은 없다.

## See also
(관련 개념 페이지 없음 — 아직 이 소스 하나뿐)
