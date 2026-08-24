# Projeto-pessoal-Testes-Funcionais-do-Carrinho-de-Compras-Sauce-Demo-
Projeto de testes manuais funcionais do módulo de carrinho de compras, desenvolvido para portfólio de QA.

## 🎯 Objetivo

O objetivo deste projeto é avaliar o funcionamento do módulo de carrinho de compras da aplicação, verificando se as principais funcionalidades relacionadas à adição, remoção e alteração de produtos funcionam conforme o comportamento esperado.
Também foram realizados testes para validar a atualização de quantidades, valores individuais e valor total do carrinho, além da identificação e documentação de possíveis defeitos encontrados durante a execução dos testes.

## 🔍 Escopo

### Funcionalidades testadas

Durante a execução dos testes, foram avaliadas as seguintes funcionalidades do módulo de carrinho:
- Acesso ao carrinho vazio;
- Adição de produtos ao carrinho;
- Adição de múltiplos produtos;
- Adição de múltiplas unidades do mesmo produto;
- Remoção de um produto;
- Remoção de todos os produtos;
- Alteração da quantidade de produtos;
- Validação da quantidade zero;
- Atualização dos valores dos produtos;
- Validação do valor total do carrinho;
- Comportamento do carrinho após alterações nos produtos e quantidades.

### Funcionalidades fora do escopo

Não foram realizados testes relacionados a:
- Pagamento;
- Checkout;
- Integração com meios de pagamento;
- Segurança;
- Performance;
- APIs;
- Banco de dados;
- Responsividade em dispositivos móveis;
- Compatibilidade com outros navegadores.

  ## 🖥️ Ambiente de Testes

| Item | Informação |
|---|---|
| Aplicação | Sauce Demo |
| Módulo testado | Carrinho de compras |
| Sistema operacional | Windows 11 |
| Navegador | Google Chrome |
| Tipo de teste | Teste manual |
| Idioma observado | Inglês/Portugues |
| Moeda observada | GBP (£) |

## 🧪 Estratégia de Testes

Para a validação do módulo de carrinho de compras, foram executados testes manuais utilizando diferentes abordagens, buscando verificar tanto comportamentos esperados quanto possíveis falhas da aplicação.

As estratégias utilizadas foram:

### ✅ Testes positivos
Validação de funcionalidades que devem funcionar corretamente.

Exemplos:
- Adicionar produtos ao carrinho;
- Remover produtos;
- Remover todos os produtos;
- Validar o cálculo do valor total.

### ❌ Testes negativos
Validação de comportamentos que devem ser impedidos pelo sistema.

Exemplos:
- Tentar adicionar quantidade igual a zero.

### 🔄 Testes de atualização
Validação do comportamento do carrinho após alterações nos produtos e quantidades.

Exemplos:
- Alterar quantidade de 1 → 2;
- Alterar quantidade de 2 → 1;
- Adicionar múltiplas unidades do mesmo produto.

### 💰 Testes de cálculo e valores
Validação dos valores individuais e do valor total do carrinho.

Exemplos:
- Soma dos produtos;
- Atualização dos subtotais;
- Atualização do valor total do carrinho.

## 📊 Resultados dos Testes

Foram executados 10 casos de teste durante a validação do módulo de carrinho de compras.
| Métrica | Resultado |
|---|---:|
| Casos de teste executados | 10 |
| Casos aprovados (PASS) | 4 |
| Casos reprovados (FAIL) | 6 |
| Bugs identificados | 2 |
| Taxa de aprovação | 40% |
| Taxa de falha | 60% |

### Resumo

Dos 10 casos executados, 4 apresentaram comportamento conforme o esperado e 6 apresentaram falhas.
As principais falhas identificadas estão relacionadas ao carregamento do carrinho e à atualização dos valores após alterações na quantidade de produtos.

## 🐞 Bugs Encontrados
Durante a execução dos testes, foram identificados dois defeitos principais no módulo de carrinho de compras.

| ID | Descrição | Severidade | Prioridade | Status |
|---|---|---|---|---|
| BUG-02 | Valor total não é atualizado após alteração da quantidade | Média | Alta | Aberto |
| BUG-03 | Carrinho não abre após adicionar produto sem atualizar a página | Média | Alta | Aberto |

### BUG-02 — Atualização do valor do carrinho
Após alterar a quantidade de um produto, a quantidade exibida é atualizada, porém o valor do carrinho não é recalculado automaticamente. É necessário atualizar a página utilizando F5 ou pressionar Enter para que o valor seja atualizado.

**Casos relacionados:** CT-006, CT-007, CT-009 e CT-010.

### BUG-03 — Carregamento do carrinho
Após adicionar um produto ao carrinho, o carrinho não é carregado automaticamente ao clicar no ícone correspondente. É necessário atualizar manualmente a página utilizando F5 para que o carrinho seja carregado.

**Casos relacionados:** CT-003 e CT-009.

## 🔗 Matriz de Rastreabilidade
A matriz abaixo relaciona os casos de teste executados aos defeitos identificados durante a execução.

| Caso de Teste | Resultado | Bug relacionado |
|---|---|---|
| CT-001 | PASS | N/A |
| CT-002 | PASS | N/A |
| CT-003 | FAIL | BUG-03 |
| CT-004 | PASS | N/A |
| CT-005 | PASS | N/A |
| CT-006 | FAIL | BUG-02 |
| CT-007 | FAIL | BUG-02 |
| CT-008 | PASS | N/A |
| CT-009 | FAIL | BUG-02 / BUG-03 |
| CT-010 | FAIL | BUG-02 |

## 📂 Documentação

- 📋 [Casos de Teste](./casos-de-teste/casos-de-teste-carrinho.xlsx)
- 🐞 [Bug Reports](./bug-reports/BUG%20REPORT%20SAUCE%20DEMO.xlsx)
- 📸 [Evidências de Testes](./evidencias/)

```markdown
## 📁 Estrutura do Projeto

```text
├── README.md
├── casos-de-teste/
│   ├── README.md
│   └── casos-de-teste-carrinho.xlsx
├── bug-reports/
│   ├── README.md
│   └── BUG REPORT SAUCE DEMO.xlsx
└── evidencias/
    ├── README.md
    └── arquivos PNG das evidências

## 📝 Conclusão
A execução dos testes funcionais permitiu validar diferentes comportamentos do módulo de carrinho de compras, incluindo adição e remoção de produtos, alteração de quantidades e validação dos valores apresentados.

Foram executados 10 casos de teste, sendo:

- 5 casos aprovados;
- 5 casos reprovados;
- 2 defeitos identificados e documentados.

Os principais problemas encontrados estão relacionados ao carregamento do carrinho e à atualização dos valores após alterações na quantidade de produtos.

Os defeitos foram documentados nos Bug Reports, juntamente com seus respectivos passos para reprodução, comportamento esperado, comportamento obtido e evidências.

O projeto também possui uma matriz de rastreabilidade relacionando os casos de teste aos defeitos encontrados.
