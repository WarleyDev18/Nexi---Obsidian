---
tipo: decisao
status: aceita
atualizado: 2026-09-29
---

# ADR-002 — Toda integração externa passa por fila

**Contexto:** sistemas de terceiros caem, ficam lentos ou limitam requisições. Chamar a API direto no fluxo do usuário propaga a falha.

**Decisão:** eventos entram numa fila; um worker consome com retry exponencial e dead-letter após 5 tentativas. Nenhuma tela espera resposta síncrona de sistema externo.

**Consequências:**
- Tolera indisponibilidade do ERP (pedidos acumulam e reprocessam).
- Latência fim a fim passa de "imediata" para "até alguns minutos".
- Exige monitoramento da fila (alerta por tamanho) e runbook de reprocessamento.

Relacionado: [[Integracao ERP-Pedidos]] · [[Runbook Reprocessar fila]]
