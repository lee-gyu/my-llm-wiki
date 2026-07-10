## [2026-07-03] ingest | 20260703-why-i-stopped-arguing-with-people.md
Created wiki/sources/2026-07-03-why-i-stopped-arguing-with-people (raw 파일은 URL 스텁만 포함하여, 링크된 URL에서 전문을 직접 fetch 후 요약). 위키 최초 ingest — index.md, overview.md, log.md 신규 생성. 신규 entity/concept 페이지 없음(3회 언급 규칙 미충족). 충돌 없음.

## [2026-07-03] ingest | 20260703-google-code-review.md
Created wiki/sources/2026-07-03-google-code-review (raw 파일은 6개 URL 스텁만 포함; google.github.io/eng-practices/review/reviewer/ 하위 6개 페이지를 직접 fetch 후 요약). Created wiki/concepts/code-review (이 소스만으로 신규 생성 — 소스 전체가 코드 리뷰를 다루므로 3회 언급 규칙 이전에 즉시 생성). index.md, overview.md 갱신. 충돌 없음.

## [2026-07-03] ingest | 20260703-artificial-adventures.md
Created wiki/sources/2026-07-03-artificial-adventures (raw 파일은 URL 스텁만 포함; scattered-thoughts.net 원문을 직접 fetch하고, WebFetch 요약과 raw HTML을 대조 검증 후 원문 기반으로 요약). Created wiki/concepts/ai-coding-assistants (AI 코딩 도구 활용 전반을 다루는 첫 소스라 즉시 생성). Updated wiki/concepts/code-review (AI가 리뷰어 역할을 하는 사례 문단 추가, sources에 이 소스 추가). index.md, overview.md 갱신. 충돌 없음 — Google 가이드(사람 리뷰어)와 이 소스(AI 리뷰어)는 관점만 다를 뿐 상충하지 않음.

## [2026-07-03] ingest | 20260703-rules-engineering-leaderhsip.md
raw 파일의 H1 제목("Why I Stopped Arguing With People")과 실제 URL(lethain.com,
Will Larson의 "Revised rules of engineering leadership")이 서로 다른 문서를 가리키는
불일치 발견 — 사용자 확인 후 URL 기준으로 진행(제목은 복사·붙여넣기 실수로 판단).
raw 파일은 URL 스텁만 포함; lethain.com 원문을 curl+extract_source.py로 직접 fetch해
전문 추출 후 WebFetch 요약과 대조 검증. Created wiki/sources/2026-07-03-revised-rules-of-engineering-leadership.
Created wiki/concepts/engineering-leadership (이 소스만으로 신규 생성 — 소스 전체가
AI 시대 엔지니어링 리더십 5원칙을 다루므로 3회 언급 규칙 이전에 즉시 생성). Updated
wiki/concepts/ai-coding-assistants (조직 규모의 하네스 채택·마이그레이션·트리아지
자동화 사례 추가), wiki/concepts/code-review (하네스가 수행하는 1차 코드 리뷰 사례
추가). index.md, overview.md 갱신. 충돌 없음 — 개인 개발자 관점(artificial-adventures)과
조직 리더십 관점(이 소스) 모두 "검증 비용이 싼 영역에서 AI 도구가 강하다"는 같은
결론으로 수렴.

## [2026-07-10] schema | research-workspace
Updated CLAUDE.md to define `research/<topic-slug>/` as the workspace for agent-conducted
topic research. Added the research directory layout, provenance rules, operation flow,
index and log bookkeeping, and the `research:` commit prefix. Research findings remain
separate from established wiki claims until promoted through the normal wiki workflow.

## [2026-07-10] research | critical-decision-method
Created research/critical-decision-method with a 13-source ledger, evidence notes, and a
Korean synthesis covering CDM's origins, four-sweep interview process, probes, analysis,
applications, evidence strength, conflicts, and validity limitations. Added the topic to
research/index.md. Wiki promotion was not performed.
