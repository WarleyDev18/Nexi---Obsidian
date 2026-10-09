# CLAUDE.md — Vault de trabalho (Warley)

> Este arquivo é lido automaticamente pelo Claude Code sempre que ele é aberto nesta pasta.
> Ele é o "quem sou eu e como trabalho" — o resto do contexto vive nas notas.

## Quem sou eu

Warley, desenvolvedor na Nexi. Meu trabalho é **integração entre sistemas**: ligar APIs,
bancos, filas e ferramentas de terceiros para que times de negócio parem de copiar dado à mão.
Também escrevo documentação técnica e apresento resultados para pessoas não técnicas.

## Como este Vault está organizado

| Pasta | O que mora aqui | Quando consultar |
|---|---|---|
| `00-Inbox/` | Captura rápida, sem organizar | Triagem semanal; nunca tratar como fato |
| `01-Projetos/` | Uma nota por projeto (status, objetivo, próximos passos, riscos) | Qualquer pergunta sobre "em que pé está X" |
| `02-Reunioes/` | Dailies e atas, nome `AAAA-MM-DD - assunto.md` | Resumos, "o que ficou combinado" |
| `03-Decisoes/` | Decisões técnicas, uma por arquivo (contexto → decisão → consequências) | Antes de propor algo que pode já ter sido decidido |
| `04-Pessoas-e-Areas/` | Quem é quem, o que cada área precisa, como prefere ser comunicada | Ao escrever algo para alguém |
| `05-Conhecimento/` | Runbooks, glossário, how-tos reutilizáveis | Dúvida técnica recorrente |
| `06-Entregas/` | Relatórios, resumos e apresentações já produzidos | Para manter tom e formato consistentes |
| `Templates/` | Modelos de nota (Obsidian) | Ao criar nota nova |
| `99-Privado/` | **Ignorada pelo git.** Dado real/sensível, só local | Só quando eu pedir explicitamente |

## Convenções

- Idioma: português do Brasil. Termos técnicos em inglês quando for o uso comum (webhook, endpoint).
- Toda nota tem frontmatter YAML com `tipo`, `status` e `atualizado`.
- Links internos com `[[wikilinks]]`. Ao citar um fato, cite a nota de origem.
- Datas no formato `AAAA-MM-DD`. Converter "ontem/semana passada" para data absoluta.

## Regras para o Claude (o que eu espero)

1. **Leia as notas antes de perguntar.** Se a resposta está em `01-Projetos/` ou `03-Decisoes/`, use-a;
   só me pergunte o que o Vault não cobre.
2. **Não invente.** Se um dado não está no Vault, diga "não consta" em vez de preencher.
3. **Decisão registrada vale mais que opinião.** Se o que eu pedir contradiz uma nota em `03-Decisoes/`,
   avise antes de seguir.
4. **Nunca escreva em `99-Privado/` nem copie conteúdo dela para fora do Vault** sem eu pedir.
5. **Não commite nem faça push sozinho.** O repositório é público: antes de qualquer push, varrer o
   conteúdo por nomes reais de cliente, pessoa, token ou URL interna.
6. Saídas para terceiros (relatório, e-mail): comece com uma linha dizendo para quem escreveu.
7. Ao terminar uma tarefa que muda o estado de um projeto, proponha a atualização da nota do projeto.

## Skills do Vault

- `resumo-semanal` (`.claude/skills/resumo-semanal/`): lê dailies e projetos da semana e gera um
  resumo de status para gestão. Skill local porque depende da estrutura *deste* Vault.

## Limites conhecidos

O Vault é memória que **eu** mantenho. Nota desatualizada vira informação errada com cara de
confiável — o campo `atualizado` existe para o Claude desconfiar de nota velha (> 30 dias).
