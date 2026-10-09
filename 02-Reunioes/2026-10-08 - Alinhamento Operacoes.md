---
tipo: reuniao
status: fechada
atualizado: 2026-10-08
---

# Alinhamento com Operações — 2026-10-08

**Participantes:** Warley, [[Marina Duarte]], gerente de Operações

- Idempotência implementada e testada: pedido duplicado não gera segundo lançamento no ERP.
- Homologação marcada para 14/10. Operações precisa de 2 pessoas disponíveis por 1 hora.
- Gerente perguntou o que acontece se o ERP cair: explicado que a fila retém e reprocessa ([[ADR-002 Fila para integracoes]]). Pediu aviso automático quando a fila passar de 100 itens.
- Operações pediu que a mensagem de erro seja em português simples, não código HTTP.

**Ações:** alerta de fila > 100 (Warley) · mensagens de erro amigáveis (Warley) · agendar homologação (Marina).

Projeto: [[Integracao ERP-Pedidos]]
