---
tipo: projeto
status: ativo
atualizado: 2026-10-07
---

# Sincronização de cadastro de clientes

**Objetivo:** um único cadastro de cliente consistente entre CRM e financeiro, eliminando
duplicidades (hoje ~7% dos clientes aparecem duas vezes).

**Solicitante:** [[Area Financeiro]] · **Responsável técnico:** Warley (com apoio do time de dados)

## Estado atual (07/10)
- Regra de deduplicação desenhada (documento + e-mail normalizado) — em revisão
- Prova de conceito rodou em 2 mil registros: 94% de acerto automático, 6% vão para revisão humana
- Decisão de qual sistema é a "fonte da verdade": [[ADR-001 CRM como fonte da verdade]]

## Próximos passos
1. Validar com [[Carlos Menezes]] o que fazer com os 6% ambíguos
2. Rodar em homologação com base completa
3. Plano de rollback antes de qualquer escrita em produção

## Riscos
- Mescla errada de dois clientes diferentes é difícil de desfazer → sempre guardar snapshot antes
- Dado pessoal envolvido (LGPD): logs não podem conter documento completo

## Reuniões
[[2026-10-07 - Revisao deduplicacao]]
