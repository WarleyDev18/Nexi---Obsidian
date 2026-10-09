---
name: resumo-semanal
description: Gera o resumo semanal de status para gestão a partir das dailies em 02-Reunioes/, das notas em 01-Projetos/ e das decisões em 03-Decisoes/. Use quando eu pedir "resumo da semana", "status para o gestor" ou "o que andou esta semana".
---

# Resumo semanal

1. Descubra a semana pedida (padrão: últimos 7 dias). Liste `02-Reunioes/` e filtre pelas datas no nome.
2. Leia cada daily da janela e `01-Projetos/*.md` com `status: ativo`.
3. Leia `03-Decisoes/` com data na janela.
4. Gere o resumo em `06-Entregas/AAAA-MM-DD - resumo-semanal.md` com este formato:
   - **Linha de público** (ex.: "Escrito para: gestão, não técnica")
   - **Entregue** — por projeto, 1–2 linhas, com `[[link]]` para a nota
   - **Em andamento / próximos passos**
   - **Bloqueios e riscos** — só o que consta nas notas
   - **Decisões tomadas**
5. Regras: máximo de uma página; sem jargão sem explicar; **nenhuma informação fora do Vault** —
   se faltar dado, escreva "não consta no Vault" em vez de inferir.
6. Não leia nem cite `99-Privado/`.
