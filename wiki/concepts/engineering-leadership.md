---
type: concept
title: Engineering Leadership in the AI Era
created: 2026-07-03
updated: 2026-07-03
sources: [20260703-rules-engineering-leaderhsip.md]
tags: [engineering-leadership, management, ai-coding]
status: current
---

# Engineering Leadership in the AI Era

AI 코딩 도구가 실행 속도를 바꾼 이후, 엔지니어링 조직을 이끄는 리더가 재정립해야
하는 원칙들(마이그레이션 소유 방식, 코드 품질과 하네스의 관계, 프로세스 자동화,
팀 구조, 의사결정 속도).

## Explanation
Will Larson은 2014~2020년 하이퍼그로스 경험과 최근 Imprint에서의 AI 도구 도입
경험을 토대로 다섯 가지 개정 원칙을 제시한다.

첫째, 복잡하고 규모가 큰 변경도 이제는 개인이나 소수 팀이 95%를 주도해 예전
대비 10%의 시간에 끝낼 수 있다. 이는 역설적으로 개인 판단력의 중요성을 높인다 —
마이그레이션 비용이 낮아질수록 사소한 결함이 동료들의 코드 멘탈 모델을 깨뜨리는
파급력은 그대로이거나 커지기 때문이다 (source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

둘째, 1차 초안 코드는 거의 공짜가 됐지만 "작동하는" 코드의 비용은 여전히 개발
하네스(테스트, CI/CD, 검증 환경, 변경 미리보기 등)의 성숙도에 달려 있다. 그래서
2년 전 엔지니어링 속도를 높이는 데 가장 가치 있었던 투자(좋은 테스트·CI/CD)가
지금도 여전히 가장 가치 있다고 저자는 강조한다
(source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

셋째, 대부분 프로세스의 기본 케이스(base case)는 적절한 하네스와 도메인 맥락,
설계자의 판단력만 있으면 완전 자동화할 수 있다고 본다. 예컨대 좋은 하네스의
1차 코드 리뷰는 사람의 1차 리뷰보다 빠르고 효과적이며, 고위험 영역에만 사람의
개입을 남겨두면 된다. 이 원칙의 따름정리로, 주간·격주 스프린트 같은 계획
프로세스는 지금보다 더 높은 전략적 고도에서 작동해야 한다고 지적한다
(source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

넷째, 개인 생산성이 올라가도 도메인 맥락을 가진 지속적(durable)·고소유 팀은
오히려 더 중요해졌다고 주장한다. Uber 시절 교훈을 인용하며, "소수의 천재
엔지니어가 완벽한 결과물을 하나씩 만들어 유지보수가 필요 없어진다"는 AI 시대의
통설에 명시적으로 반대한다 — 판단력이 뛰어난 개인도 결국 도메인 맥락 부족에
막힌다는 것이다 (source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

다섯째, 실행 속도가 빨라진 만큼 그 이득을 실현하려면 조직이 빠르고 되돌리지 않는
의사결정을 내려야 한다. 이 때문에 평균적인 CTO 역할이 이전보다 훨씬 기술적이고
덜 관료적으로 변했으며, 팀 간 이견이 있을 때 구속력 있는 결정을 내릴 수 있는
사람이 저자 본인뿐인 경우가 많아 지속적으로 결정을 내리게 된다고 말한다
(source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

이 다섯 원칙은 Imprint에서의 구체적 사례로 뒷받침된다: 배포 빈도를 주 6회에서
200~400회로 늘린 인프라 마이그레이션(2명이 2개월 주도), 설정 메커니즘을 다수에서
2개로 통합(1분기 내 완료), 멀티레포에서 모노레포로의 프론트엔드 전환(1명이 95%
주도, 약 1개월), 하네스 기반 고객 이슈 트리아지, 그리고 하네스가 수행하는 1차
코드 리뷰 등이다. 반면 저자는 설계 문서나 PR을 다른 팀에 "담 너머로" 던지는
방식은 실패했고, 이런 "슬롭(slop)" 산출물은 정리 비용뿐 아니라 LLM의 맥락을
오염시켜 처음부터 다시 하는 것보다 나쁜 결과를 낳는다고 경고한다
(source: [[sources/2026-07-03-revised-rules-of-engineering-leadership]]).

## Positions and disagreements
저자는 "AI 시대에는 소수의 천재 엔지니어가 조직을 대체한다"는 통설에 명시적으로
반대 입장을 취하지만, 이는 이 위키에 아직 등록된 다른 소스의 주장과 직접 상충하지는
않는다. [[concepts/ai-coding-assistants]]가 다루는 "검증 비용이 싼 작업엔 AI가
강하다"는 관찰과는 방향이 같다 — 이 소스는 조직 규모에서, 그 소스는 개인 개발자
관점에서 같은 패턴(검증·하네스가 갖춰진 영역은 자동화가 잘 통한다)을 보고한다.

## See also
- [[concepts/ai-coding-assistants]] — 개인 개발자 관점의 AI 코딩 도구 효용/한계.
  이 개념은 조직·리더십 관점에서 같은 도구들이 만드는 구조적 변화를 다룬다.
- [[concepts/code-review]] — 이 소스가 보고하는 "하네스가 수행하는 1차 코드 리뷰"
  사례가 통합되어 있다.
