# Threeebs :3 — Hospedagem e Continuidade

> Documento comercial — primeira versão  
> Este arquivo descreve como funciona a hospedagem dos projetos na Threeebs, o que acontece após o fim de um contrato de desenvolvimento e quais serviços adicionais podem ser contratados para continuidade operacional.

---

# 1. Objetivo

A hospedagem mantém o projeto disponível na infraestrutura da Threeebs.

Ela deve ser entendida como uma camada própria, separada de desenvolvimento e de manutenção.

```text
Desenvolvimento
≠
Hospedagem
≠
Manutenção
```

Essas três frentes podem se relacionar, mas não representam o mesmo serviço.

---

# 2. Hospedagem durante o projeto

Durante um contrato de desenvolvimento, a hospedagem padrão faz parte do pacote contratado.

```text
Contrato de projeto
      ↓
Desenvolvimento
      +
Hospedagem Threeebs
      +
Publicação
```

O cliente não precisa contratar um servidor separado para iniciar.

A infraestrutura padrão é gerenciada pela Threeebs.

---

# 3. Continuidade após o contrato

Quando o contrato de desenvolvimento termina, o cliente pode optar por continuar apenas com a hospedagem.

```text
Fim do contrato
      ↓
Cliente escolhe
   /        |        \
renovar   hospedar   encerrar
projeto    somente
```

A continuidade de hospedagem pode ser contratada nos ciclos:

```text
mensal
trimestral
semestral
anual
```

Os valores e possíveis incentivos por período podem ser definidos futuramente.

---

# 4. O que a hospedagem inclui

A hospedagem cobre a permanência e operação do projeto dentro da infraestrutura da Threeebs.

Ela pode incluir, dentro do escopo contratado:

- publicação do projeto;
- disponibilização em servidor Threeebs;
- operação básica da infraestrutura;
- continuidade do ambiente;
- gestão técnica do ambiente de hospedagem;
- manutenção do endereço publicado;
- suporte relacionado à disponibilidade da infraestrutura, dentro dos limites definidos pela Threeebs.

---

# 5. O que a hospedagem não inclui

Hospedagem não significa evolução contínua do projeto.

Ela não inclui automaticamente:

- novas funcionalidades;
- novas páginas;
- alterações de layout;
- integrações;
- automações;
- manutenção ativa;
- relatórios periódicos;
- acompanhamento estratégico;
- mudanças de escopo;
- rotina formal de backup.

Esses itens podem ser contratados separadamente.

---

# 6. Infraestrutura padrão

Por padrão, o projeto utiliza a infraestrutura da Threeebs.

```text
Cliente
  ↓
Projeto
  ↓
Infraestrutura Threeebs
```

Na maior parte dos casos, essa estrutura pode ser compartilhada entre diferentes projetos com isolamento e controles definidos pela plataforma.

---

# 7. Infraestrutura dedicada

Quando houver necessidade específica, pode ser utilizada infraestrutura dedicada.

Isso pode incluir:

- servidor próprio;
- ambiente dedicado;
- banco de dados dedicado;
- recursos específicos;
- configuração especial.

```text
Projeto padrão
      ↓
Nova necessidade
      ↓
Análise técnica
      ↓
Infraestrutura dedicada
```

A infraestrutura dedicada não faz parte automaticamente da hospedagem padrão e pode exigir orçamento adicional.

---

# 8. Backup como serviço opcional

A hospedagem padrão não inclui uma rotina formal de backup contratada.

O backup é tratado como um serviço adicional.

```text
Hospedagem
   ↓
Backup opcional
```

O cliente pode contratar um plano de backup de acordo com a necessidade do projeto.

A periodicidade pode variar, por exemplo:

```text
semanal
mensal
ou outra frequência acordada
```

A definição depende do tipo de projeto, volume de dados, criticidade e necessidade do cliente.

---

# 9. Recomendação de backup

A Threeebs considera backup uma boa prática e pode recomendar sua contratação de forma ativa.

A contratação continua sendo opcional.

```text
Cliente sem backup
      ↓
Threeebs recomenda
      ↓
Cliente decide
```

A comunicação deve explicar a importância do serviço sem transformar a recomendação em obrigação comercial.

---

# 10. Lembretes de backup

Quando o cliente ainda não possui um plano de backup, a Threeebs pode realizar lembretes periódicos.

Modelo inicial:

```text
início do projeto
      ↓
primeira recomendação
      ↓
novo lembrete posteriormente
      ↓
reavaliação periódica
```

Na fase inicial, esses lembretes podem ser realizados manualmente.

No futuro, podem ser automatizados dentro da própria plataforma.

Exemplo de evolução:

```text
Hoje
→ contato manual

Futuro
→ notificação automática Threeebs
```

Quando o cliente contratar o backup, as notificações de oferta deixam de ser necessárias enquanto o serviço estiver ativo.

---

# 11. Manutenção não é hospedagem

O projeto pode permanecer no ar sem possuir um plano de manutenção.

```text
Projeto hospedado
      ↓
Continua funcionando
```

Um plano de manutenção representa acompanhamento ativo e pode incluir:

- verificações periódicas;
- inspeção técnica;
- validação de funcionamento;
- análise preventiva;
- relatórios;
- correções previstas no plano.

A manutenção deve ser contratada separadamente.

---

# 12. Encerramento da hospedagem

Se o cliente não renovar a hospedagem, o projeto pode ser retirado da infraestrutura ativa da Threeebs.

Antes da remoção definitiva, existe uma janela inicial de retenção de:

```text
60 dias
```

Durante esse período, o projeto pode permanecer disponível para:

- reativação;
- recuperação;
- organização de saída;
- migração;
- exportação.

---

# 13. Código após encerramento

O código-fonte segue as regras de propriedade definidas no contrato correspondente.

Quando houver direito de acesso ou propriedade do cliente, o código pode permanecer preservado em repositório GitHub.

```text
Hospedagem encerrada
      ↓
Código preservado
      ↓
GitHub
```

A existência do código no repositório não significa que o ambiente continuará ativo.

---

# 14. Banco de dados após encerramento

O banco de dados deve ser tratado separadamente da infraestrutura ativa.

Após o encerramento da hospedagem, a Threeebs pode realizar uma exportação do banco de dados.

```text
Banco ativo
   ↓
Hospedagem encerrada
   ↓
Exportação
   ↓
Backup separado
```

Esse backup pode ser armazenado por até:

```text
1 ano
```

Esse mecanismo existe como retenção de encerramento e não substitui um plano de backup recorrente.

---

# 15. Retenção de encerramento não é backup

É importante separar os dois conceitos.

```text
BACKUP RECORRENTE
→ proteção contínua durante operação

RETENÇÃO DE ENCERRAMENTO
→ preservação temporária após saída
```

O fato de a Threeebs manter um banco exportado após o encerramento não garante recuperação de versões anteriores do projeto durante sua operação.

Por isso, projetos que exigem maior proteção de dados devem considerar a contratação de backup recorrente.

---

# 16. Reativação

Durante o período de retenção, o cliente pode solicitar reativação.

A reativação pode envolver:

- restauração do ambiente;
- reconfiguração;
- atualização de domínio;
- restauração de banco;
- nova contratação de hospedagem.

Dependendo do trabalho necessário, pode existir custo de reativação.

---

# 17. Migração

Quando o cliente desejar sair da infraestrutura da Threeebs, a migração pode ser realizada conforme as regras do modelo contratado.

Ela pode envolver:

- exportação de arquivos;
- entrega ou transferência de código;
- exportação do banco;
- configuração em novo servidor;
- ajuste de domínio;
- documentação técnica;
- validação pós-migração.

A migração pode ser cobrada como serviço separado.

---

# 18. Ciclo de continuidade

```text
Projeto em desenvolvimento
        ↓
Hospedagem incluída
        ↓
Fim do contrato
        ↓
Cliente decide
   /        |        \
renovar   manter     encerrar
projeto   hospedagem
            ↓
        hospedagem
        recorrente
            ↓
      mensal / trimestral
      semestral / anual
```

---

# 19. Evolução futura

A forma de hospedagem poderá evoluir com a maturidade da Threeebs.

No futuro, podem existir modelos como:

- cobrança por uso;
- planos por capacidade;
- armazenamento adicional;
- banco de dados por consumo;
- infraestrutura dedicada automatizada;
- relatórios de consumo;
- alertas de capacidade;
- escalabilidade automática.

Essas possibilidades não fazem parte obrigatória do modelo inicial.

---

# 20. Princípio central

> **Hospedagem mantém o projeto disponível. Manutenção acompanha o projeto. Backup protege o projeto. Desenvolvimento transforma o projeto.**

A Threeebs deve manter essas responsabilidades separadas para que o cliente saiba exatamente o que está contratando.

```text
clareza
+
continuidade
+
escolha
+
responsabilidade
```
