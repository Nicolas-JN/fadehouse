# FadeHouse — Sistema de Gestão para Barbearia

SPA completa de gestão de barbearia: agendamento para clientes e painel administrativo full, num único arquivo HTML, sem backend, com persistência via `localStorage`.

**[Ver demo ao vivo](#)** — *link do GitHub Pages, ativar em Settings → Pages → branch `main` → pasta `/root`*

## Funcionalidades

### Área do cliente
- Cadastro e login
- Agendamento em etapas (barbeiro → serviço → horário → confirmação)
- Histórico de agendamentos do usuário

### Painel administrativo
- **Dashboard**: visão geral dos agendamentos do dia, confirmação/cancelamento rápido
- **Agenda**: visão em calendário e tabela, com filtro por data, barbeiro e status
- **Clientes**: listagem e filtro da base de clientes
- **Estoque**: controle de produtos, giro, previsão de reposição, gráfico de valor em estoque (donut chart em canvas puro)
- **Faturamento**: gráficos de receita por período (dia/semana/mês)
- **Caixa**: abertura/fechamento de caixa com histórico de movimentações
- **Configurações**: gestão de serviços e barbeiros
- **Auditoria**: log de ações realizadas no painel

## Stack

- HTML/CSS/JS puro (sem frameworks, sem build step)
- `localStorage` como camada de persistência (dados ficam no navegador do usuário)
- Gráficos renderizados em `<canvas>` nativo, sem biblioteca externa
- Tipografia: Cormorant Garamond + Jost (Google Fonts)

## Como rodar

Não precisa de servidor nem instalação. Duas opções:

```bash
git clone https://github.com/SEU_USUARIO/fadehouse.git
cd fadehouse
```

- Abra `index.html` direto no navegador, **ou**
- Acesse a [demo ao vivo](#) publicada via GitHub Pages

## Credenciais de demonstração

O admin usa uma credencial fixa no código, só pra fins de demonstração (não há backend/autenticação real):

```
Email: admin@fadehouse.com
Senha: admin123
```

Para a área de cliente, use "Cadastrar" para criar um usuário — os dados ficam salvos no `localStorage` do navegador.

## Limitações (por design)

Este é um projeto de prototipagem/portfólio, não um produto em produção:

- Sem backend: todos os dados vivem no `localStorage` do navegador (limpar o cache apaga tudo).
- Sem autenticação real: credenciais e sessão não têm segurança de produção.
- Single-file: HTML, CSS e JS estão no mesmo arquivo por decisão de escopo do projeto (facilita distribuição e revisão).

## Contexto

Projeto desenvolvido para a disciplina de Prototipagem de Sistemas Computacionais, com todo o processo de engenharia por trás do código: modelagem BPMN (AS-IS/TO-BE), diagramas UML (casos de uso e classes), C4 Model, wireframes de baixa fidelidade e documentação ABNT.
