---
name: 'to-feature'
description: Turns an idea into a new verifiable feature in .ai/features.json; use for /to-feature or when registering a new feature
slash: true
---

1. Identify the project root; ask if it is unclear. Discuss only what is needed to define a description and observable criteria.
2. Show the proposed feature to the user before writing it. Suggest a SPEC only for complex scope or technical decisions; do not create it without agreement.
3. After approval, create `.ai/features.json` with `{"features":[]}` and `.ai/history.md` with `# History` if missing; preserve existing contents.
4. Add an object to `features`: `{"id":"F001","description":"...","acceptance_criteria":["..."],"status":"pending","spec":null}`. Use the next available ID; if a SPEC was agreed, create `.ai/features/<id>/spec.md` and store that path in `spec`, without duplicating criteria.
5. Record the creation and relevant decisions in `.ai/history.md`. Do not implement the feature or modify existing features.
