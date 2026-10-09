---
tipo: decisao
status: aceita
atualizado: 2026-10-02
---

# ADR-001 — CRM como fonte da verdade do cadastro de clientes

**Contexto:** CRM e financeiro mantêm cadastros separados e divergem. Sem uma fonte única, qualquer sincronização vira briga de "qual dado ganha".

**Decisão:** o CRM é a fonte da verdade. O financeiro recebe dados do CRM; só edita campos fiscais (que voltam ao CRM como sugestão, não como sobrescrita).

**Consequências:**
- Sincronização é majoritariamente unidirecional → mais simples e auditável.
- Financeiro perde autonomia para corrigir nome/contato direto no seu sistema.
- Se o CRM sair do ar, a sincronização pausa (aceitável).

**Alternativas descartadas:** banco mestre separado (custo e prazo altos); "último a editar vence" (gera perda silenciosa de dado).

Relacionado: [[Sincronizacao de Cadastro de Clientes]]
