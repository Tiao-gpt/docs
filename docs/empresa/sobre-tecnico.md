# Threeebs :3 — Sobre Técnico

A Threeebs é um ambiente de desenvolvimento e hospedagem construído para transformar projetos em sistemas que possam evoluir sem depender de uma plataforma fechada.

A arquitetura parte de uma unidade central:

```text
Usuário
   ↓
Cliente
   ↓
Projeto
   ↓
Ambiente
   ├── Sandbox
   └── Produção
```

Cada projeto possui ambientes independentes, endereços próprios, controle de acesso e recursos que podem ser habilitados progressivamente.

A mesma base atende tanto projetos simples e estáticos quanto aplicações que precisam crescer para execução PHP, banco de dados, colaboração em tempo real e outros serviços.

## O Threeebs Editor

O Editor Threeebs utiliza o Monaco como interface de edição, mas a arquitetura não permite que o navegador simplesmente escreva arquivos diretamente no servidor.

As operações passam por uma camada de storage responsável por:

```text
Editor
   ↓
Storage Service
   │
   ├── autorização
   ├── isolamento
   ├── validação de caminhos
   ├── quotas
   ├── concorrência
   ├── metadados
   └── auditoria
        ↓
    filesystem
```

Essa camada centraliza as mutações do Editor e impede que operações concorrentes ultrapassem os limites do projeto.

## HTML, CSS, JavaScript e PHP

Um projeto não precisa escolher entre ser um site HTML ou um projeto PHP.

O mesmo projeto pode evoluir.

```text
Projeto
│
├── index.php
├── sobre.html
│
├── css/
│   └── style.css
│
└── js/
    └── app.js
```

O Editor pode tratar arquivos PHP como código editável, preservando as mesmas regras de quota, isolamento, metadados e auditoria.

Editar PHP e executar PHP são capacidades diferentes.

## Runtime isolado

Quando um ambiente possui execução PHP habilitada, o código não é executado dentro do Host principal do Threeebs.

A arquitetura utiliza runtime isolado por ambiente:

```text
hostname
   ↓
Threeebs Host / Gateway
   ↓
Ambiente
   ↓
tipo de runtime
   │
   ├── static
   │     ↓
   │    Host
   │
   └── PHP
         ↓
   Runtime isolado
```

Cada runtime deve enxergar apenas o seu próprio ambiente.

## Banco de dados por ambiente

Os bancos utilizados pelos projetos são separados dos bancos internos da plataforma.

```text
MYSQL THREEEBS
│
├── identity
├── control
├── work
├── catalog
├── finance
└── audit


PROJECTS DB
│
├── Projeto A / Sandbox
├── Projeto A / Production
├── Projeto B / Sandbox
└── Projeto B / Production
```

Cada ambiente pode receber seu próprio database e usuário, com permissões limitadas somente ao banco correspondente.

A filosofia é simples:

```text
código do cliente
      ↓
acessa recursos do cliente

código do cliente
      ✗
não acessa controle interno Threeebs
```

## Colaboração em tempo real

O Threeebs Editor pode utilizar colaboração em tempo real baseada em:

```text
Monaco
   +
Yjs
   +
y-monaco
   +
WebSocket
```

Cada sala deve ser identificada pelo contexto completo do projeto, ambiente e arquivo.

```text
projeto
+
ambiente
+
arquivo
```

O serviço realtime não deve se tornar um caminho alternativo para ignorar autorização, quota ou auditoria.

## Segurança como arquitetura

Na Threeebs, segurança não deve depender apenas da interface esconder determinado botão.

Ela aparece em diversas camadas:

```text
Identidade
    ↓
Autorização
    ↓
Cliente
    ↓
Projeto
    ↓
Ambiente
    ↓
Serviço
    ↓
Filesystem / Database / Runtime
```

O objetivo é aplicar menor privilégio em cada fronteira.

## Uma base feita para evoluir

A visão técnica da Threeebs não é criar um conjunto de ferramentas independentes.

É permitir que novas capacidades sejam adicionadas ao mesmo projeto.

```text
Projeto
   │
   ├── Editor
   ├── Storage
   ├── Quotas
   ├── Realtime
   ├── Runtime
   ├── Database
   ├── GitHub
   ├── IA / Codex
   └── outros serviços
```

Por isso um projeto pode começar como:

```text
HTML + CSS + JavaScript
```

e evoluir para:

```text
PHP
+
Database
+
Realtime
+
novos serviços
```

sem precisar abandonar sua identidade, código ou estrutura de projeto.

> **A Threeebs constrói uma camada entre a ideia e a infraestrutura: um ambiente onde código, hospedagem, dados e ferramentas podem crescer juntos, mantendo o projeto como propriedade central e a segurança como parte da arquitetura.**

```text
IDEIA
  ↓
CÓDIGO
  ↓
PROJETO
  ↓
AMBIENTE
  ↓
┌─────────────────────────────────────┐
│ Editor                              │
│ Storage + Quotas                    │
│ Realtime                            │
│ Runtime                             │
│ Database                            │
│ Serviços                            │
└─────────────────────────────────────┘
  ↓
SISTEMA PRÓPRIO
  ↓
EVOLUÇÃO
```
