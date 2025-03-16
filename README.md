# Teste para vaga de Analista de Qualidade no Magazord

## Introdução

A Magazord é uma plataforma de e-commerce que oferece soluções integradas para otimizar operações online. Neste teste para vaga de Analista de Qualidade, preparei a documentação necessária para garantir a eficiência das integrações entre o e-commerce e os marketplaces, além da ferramenta de gerenciamento de estoque Bling. Também documentei os procedimentos para verificar que os anúncios sejam automaticamente atualizados e certifiquei que após alterações os campos de cadastro estejam funcionando corretamente.

## Recursos

- **Analista de Teste e Qualidade de Software:** Bruno Soares Ribeiro
- **Prioridade:** Alta
- **Severidade:** Alta
- **Data de Inicio:** 10/03/2025
- **Data Final de Entrega:** 17/03/2025

## Objetivos do Teste

- **1° Cenário:** Garantir que a integração de estoque, anúncios, faturamento, pedidos e preço entre o e-commerce e os marketplaces funcione corretamente.
- **2° Cenário:** Garantir que a integração com a ferramenta de gerenciamento de estoque Bling funcione corretamente no e-commerce.
- **3° Cenário:** Garantir que os anúncios sejam corretamente atualizados para "Pausado (sem estoque)" no Mercado Livre quando o estoque se esgota no e-commerce.
- **4° Cenário:** Garantir que os campos de cadastro de nome completo, e-mail, número de telefone, data de nascimento e endereço estejam funcionando corretamente e validando os dados conforme esperado.

## Critérios de Aceitação

- **1° Cenário:** As atualizações de dados devem ser refletidas corretamente e sem discrepâncias entre o e-commerce e os marketplaces em até 10 minutos.
- **2° Cenário:** As atualizações de estoque devem ser refletidas corretamente e sem discrepâncias entre o e-commerce e o Bling em até 10 minutos.
- **3° Cenário:** Os anúncios devem ser automaticamente atualizados para "Pausado (sem estoque)" no Mercado Livre quando o estoque atinge zero no e-commerce, sem necessidade de intervenção manual.
- **4° Cenário:** Os campos de cadastro devem validar corretamente os dados inseridos, rejeitando entradas inválidas e aceitando apenas dados válidos, conforme as regras de negócio definidas.

## **Riscos e Mitigações**

- **1º Cenário: Integração de Marketplaces**
  - **Risco**: Inconsistência de dados entre sistemas.
  - **Mitigação**: Realizar testes de integração frequentemente e monitoramento de logs.
- **2º Cenário: Integração com Bling**
  - **Risco**: Falhas na atualização de estoque.
  - **Mitigação**: Realizar testes de integração e monitoramento contínuo.
- **3º Cenário: Problema com Anúncios no Mercado Livre**
  - **Risco**: Anúncios incorretamente pausados, resultando em pedidos sem estoque.
  - **Mitigação**: Verificar documentação do Mercado Livre e analisar logs de integração.
- **4º Cenário: Validação de Dados Cadastrais**
  - **Risco**: Dados incorretos ou incompletos.
  - **Mitigação**: Implementar validações rigorosas e criptografia de dados.

## Escopo de Testes

### Testes de Integração

- **CT-001:** Verificação da Sincronização Correta de Quantidades de Produtos no E-commerce
- **CT-002:** Verificação da Sincronização Correta de Quantidades de Produtos no Marketplace
- **CT-003:** Falha na Atualização de Estoque Devido a Problemas de API
- **CT-004:** Testes de Desempenho com Grandes Volumes de Atualizações de Estoque
- **CT-005:** Verificação de Acesso Não Autorizado à API de Estoque
- **CT-006:** Criação de Anúncios com Sucesso
- **CT-007:** Falha na Criação de Anúncios Devido a Dados Incompletos
- **CT-008:** Testes de Desempenho com a Criação de um Grande Número de Anúncios Simultaneamente
- **CT-009:** Verificação de Injeção de Código Malicioso nos Campos de Anúncios
- **CT-010:** Atualização de Anúncios com Sucesso
- **CT-011:** Exclusão de Anúncios com Sucesso
- **CT-012:** Verificação de Permissões de Usuário na Criação de Anúncios
- **CT-013:** Processamento Correto de Pagamentos e Geração de Faturas
- **CT-014:** Falha no Processamento de Pagamentos Devido a Problemas de Gateway de Pagamento
- **CT-015:** Testes de Desempenho com um Grande Volume de Transações Simultâneas
- **CT-016:** Verificação de Segurança na Transmissão de Dados de Pagamento
- **CT-017:** Verificação de Reembolsos
- **CT-018:** Verificação de Pagamentos Parciais
- **CT-019:** Verificação de Diversos Métodos de Pagamento
- **CT-020:** Cancelamento de Pedidos com Sucesso
- **CT-021:** Falha na Atualização de Pedidos Devido a Inconsistências de Dados
- **CT-022:** Testes de Desempenho com um Grande Volume de Pedidos Simultâneos
- **CT-023:** Verificação de Acesso Não Autorizado aos Dados de Pedidos
- **CT-024:** Verificação de Atualização de Status de Pedido
- **CT-025:** Atualização Correta dos Preços dos Produtos nos Marketplaces
- **CT-026:** Falha na Atualização de Preços Devido a Problemas de API
- **CT-027:** Testes de Desempenho com um Grande Volume de Atualizações de Preços
- **CT-028:** Verificação de Manipulação Não Autorizada dos Preços dos Produtos
- **CT-029:** Verificação de Atualização de Preços em Diferentes Moedas
- **CT-030:** Verificação de Descontos e Promoções
- **CT-031:** Verificação de Histórico de Preços

### Testes Validação de Cadastro

- **CT-032:** Nome Completo - Entrada Válida
- **CT-033:** Nome Completo - Campo Vazio
- **CT-034:** Nome Completo - Comprimento Mínimo
- **CT-035:** Nome Completo - Caracteres Especiais
- **CT-036:** Nome Completo - Números.
- **CT-037:** E-mail - Entrada Válida
- **CT-038:** E-mail - Campo Vazio
- **CT-039:** E-mail - Formato Inválido
- **CT-040:** E-mail - Domínios Inválidos
- **CT-041:** E-mail - Espaços em Branco
- **CT-042:** Número de Telefone - Entrada Válida
- **CT-043:** Número de Telefone - Campo Vazio
- **CT-044:** Número de Telefone - Comprimento Mínimo
- **CT-045:** Número de Telefone - Comprimento Máximo
- **CT-046:** Número de Telefone - Caracteres Especiais
- **CT-047:** Número de Telefone - Letras
- **CT-048:** Número de Telefone - Formatos Internacionais
- **CT-049:** Data de Nascimento - Entrada Válida
- **CT-050:** Data de Nascimento - Campo Vazio
- **CT-051:** Data de Nascimento - Formato Inválido
- **CT-052:** Data de Nascimento - Data Futura
- **CT-053:** Data de Nascimento - Letras
- **CT-054:** Rua - Entrada Válida
- **CT-055:** Rua - Campo Vazio
- **CT-056:** Rua - Caracteres Especiais
- **CT-057:** Cidade - Entrada Válida
- **CT-058:** Cidade - Campo Vazio
- **CT-059:** Cidade - Caracteres Especiais
- **CT-060:** Cidade - Números
- **CT-061:** Estado - Entrada Válida
- **CT-062:** Estado - Campo Vazio
- **CT-063:** Estado - Caracteres Especiais
- **CT-064:** Estado - Números
- **CT-065:** CEP - Entrada Válida
- **CT-066:** CEP - Caracteres Especiais
- **CT-067:** CEP - Formato Inválido
- **CT-068:** CEP - Espaços em Branco

## Documentação Completa

**Para acessar a resolução dos quatro cenários, confira o documento:**

- [Plano de Teste](https://github.com/brunosrd/teste-qa-megazord/blob/main/documenta%C3%A7%C3%A3o/PlanoDeTeste.md)

---
