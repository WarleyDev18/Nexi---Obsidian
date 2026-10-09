---
tipo: projeto
status: ativo
atualizado: 2026-10-08
---

# Integração ERP ↔ Pedidos

**Objetivo:** pedidos aprovados na plataforma de vendas chegam ao ERP sem digitação manual,
em até 5 minutos. Hoje o time de operações copia 40–60 pedidos/dia à mão.

**Solicitante:** [[Area Operacoes]] · **Responsável técnico:** Warley

## Estado atual (08/10)
- Webhook de pedido aprovado recebido e validado (assinatura HMAC) ✅
- Fila com reprocessamento automático em falha ✅ (ver [[ADR-002 Fila para integracoes]])
- Mapeamento de produtos → códigos do ERP: 80% feito; faltam produtos sazonais
- Homologação com Operações marcada para 14/10

## Próximos passos
1. Fechar mapeamento dos produtos sazonais com [[Marina Duarte]]
2. Teste de carga com 500 pedidos simulados
3. Escrever runbook de falha ([[Runbook Reprocessar fila]])

## Riscos
- ERP tem janela de manutenção nas madrugadas de domingo → pedidos acumulam na fila (aceito, ver ADR-002)
- Limite de 60 req/min da API do ERP; pico de promoção pode estourar

## Reuniões
[[2026-10-06 - Daily]] · [[2026-10-08 - Alinhamento Operacoes]]
