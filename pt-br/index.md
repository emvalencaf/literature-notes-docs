---
title: literature-notes (PT-BR)
---

# literature-notes

[English](../) | **Português (Brasil)**

Oito skills de agente que transformam fontes acadêmicas (artigos, dissertações,
teses e livros) em uma wiki estruturada e consultável de notas de leitura.
Cada nota é ancorada a uma página, marcada com um glossário controlado e lida
à luz da sua pergunta de pesquisa.

Disponível na Agensi. Licença de um usuário.

![O fluxo de trabalho](../assets/d1.png)

## O que faz

- Extrai notas de um PDF, uma por conceito, em três tipos: **autoral** (ideia
  sua), **interpretativa** (sua leitura do autor) e **resumo** (relato neutro),
  com metadados de citação ABNT.
- Mantém um escopo de pesquisa (`RESEARCH.md`) e um glossário controlado
  (`Glossary.md`) a que toda nota responde.
- Consulta por tag, fonte, tipo de nota, página, links de influência, status
  de verificação ou texto livre.
- Valida a base: tags desconhecidas, links quebrados, termos sem definição.
- Gera um site HTML somente leitura, com busca, backlinks e grafo de links.
- Escreve no seu idioma. Uma citação mantém o idioma da fonte.

## As oito skills

| Skill | Para que serve |
| --- | --- |
| `setup-literature-notes` | Preparação única: cria `.literature-notes/` e escolhe o estilo de links. |
| `literature-notes-scope` | Definir a pergunta de pesquisa e o glossário. |
| `literature-notes` | Ler um PDF e escrever as notas. |
| `literature-notes-query` | Buscar o que você já anotou. |
| `literature-notes-rescope` | Conciliar notas pendentes com o escopo. |
| `literature-notes-validate` | Checar referências quebradas antes do commit. |
| `literature-notes-visualize` | Gerar o site HTML. |
| `literature-notes-ask-how` | Perguntar qual skill serve ao que você faz. |

## Como usar

![Estrutura em disco](../assets/d2.png)

1. `/setup-literature-notes`: uma vez por projeto.
2. `/literature-notes-scope`: pergunta de pesquisa, limites e glossário.
3. `/literature-notes <caminho-do-pdf>`: ler uma fonte, filtrada pelo escopo.
4. `/literature-notes-query`: buscar o que já está anotado.
5. `/literature-notes-rescope`: de tempos em tempos, em lote.
6. `/literature-notes-validate`: antes de cada commit.

**Instalação:** copie cada pasta de `skills/` para a pasta de skills do seu
agente (no Claude Code, `~/.claude/skills/` ou `.claude/skills/`). Requer
Python 3. A skill `rescope` usa a skill gratuita `grilling`, de terceiros. O
visualizador HTML carrega fontes e bibliotecas de CDNs públicas.

**Licença:** de um usuário. As notas que você cria são suas.
