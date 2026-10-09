---
tipo: runbook
status: rascunho
atualizado: 2026-10-05
---

# Runbook — Reprocessar itens da fila

1. Verificar tamanho da fila e da dead-letter no painel.
2. Se o ERP estiver fora do ar: **não reprocessar**; aguardar retorno (a fila retém).
3. Se itens estão na dead-letter: inspecionar o motivo (dado inválido vs. falha temporária).
4. Falha temporária → reenviar da dead-letter para a fila principal.
5. Dado inválido → corrigir na origem e reenviar; registrar na nota do projeto.
6. Confirmar que o contador de pendentes voltou a zero.

Ver [[ADR-002 Fila para integracoes]].
