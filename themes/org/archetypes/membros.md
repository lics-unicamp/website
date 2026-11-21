---
title: "Your Name Here"
description: "Description of up to 150 chars"
cargo: "challenger OR researcher OR tutor OR agent OR associate"
github: "{{ .File.ContentBaseName }}"
linkedin: "https://www.linkedin.com/in/seu_usuario/"
external: "https://www.lattes.cnpq.br/seu_usuario"
points: 0
areas:
# Mantenha apenas as áreas das quais você participa
  - "management"
  - "advisors"
  - "training"
  - "external_relations"
  - "human_resources"
  - "marketing"
# Cargos da diretoria (use junto com "management")
  - "president"
  - "vice_president"
badges:
# A ser preenchido pelo RH
  - "none"
translationKey: "member_{{ .File.ContentBaseName }}"
---