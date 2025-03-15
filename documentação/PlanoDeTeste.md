# Plano de Teste Desafio Megazord

## 1º Cenário: Plano de testes para validar a integração com o marketplace

### 1.Documentação e Materiais de Apoio

**Identificação da documentação:**

- Documentação oficial dos marketplaces.
- Especificações técnicas da integração.
- Requisitos do projeto.
- Histórico de bugs e relatórios de testes anteriores.
- Documentação de arquitetura do sistema.
- Relatórios de teste de segurança e desempenho.

**Análise da documentação:**

- Detalhes sobre endpoints da API, autenticação, e mapeamento de dados específicos de cada marketplace.
- Diagramas de fluxo, mapeamento de dados, lógica de negócios e protocolos de comunicação.
- Expectativas do cliente, critérios de aceitação e metas de desempenho.
- Fluxos de trabalho críticos e cenários de teste previamente definidos.
- Areas problemáticas e erros corrigidos.
- Pontos de interação e compatibilidade com a infraestrutura existente.

**Mapeamento dos requisitos:**

- Crio casos de teste específicos para cada requisito funcional e não funcional, garantindo que todos os aspectos da integração sejam validados.
- Utilizo uma matriz de rastreabilidade para garantir que todos os requisitos do projeto estejam cobertos pelos casos de teste.

**Utilização de ferramentas:**

- Para rastreamento de requisitos, criação de casos de teste, gerenciamento de tarefas e colaborar com a equipe: Jira + Xray e Trello.
- Para análise de conteúdo textual, extração de informações significativas e identificação de padrões: MyMap.AI.

### 2.Abrangência dos Testes

**Funcionalidades de Integração:**

- **Estoque:** Verifico a sincronização de quantidade de produtos.
- **Anúncios:** Crio, atualizo e excluo anúncios.
- **Faturamento:** Processo pagamentos e gero faturas.
- **Pedidos:** Recebo, atualizo e cancelo pedidos.
- **Preço:** Atualizo preços dos produtos.

#### Casos de Uso

**Estoque:**

- **Cenários de Sucesso:** Verifico a sincronização correta de quantidades de produtos.
- **Cenários de Falha:** Testo falhas na atualização de estoque devido a problemas de rede ou API.
- **Cenários de Carga:** Realizo testes de desempenho com grandes volumes de atualizações de estoque.
- **Cenários de Segurança:** Verifico acesso não autorizado à API de estoque.

**Anúncios:**

- **Cenários de Sucesso:** Crio, atualizo e excluo anúncios com sucesso.
- **Cenários de Falha:** Testo falhas na criação de anúncios devido a dados incompletos ou inválidos.
- **Cenários de Carga:** Realizo testes de desempenho com a criação de um grande número de anúncios simultaneamente.
- **Cenários de Segurança:** Verifico injeção de código malicioso nos campos de anúncios.

**Faturamento:**

- **Cenários de Sucesso:** Processo pagamentos corretamente e gero faturas.
- **Cenários de Falha:** Testo falhas no processamento de pagamentos devido a problemas de gateway de pagamento.
- **Cenários de Carga:** Realizo testes de desempenho com um grande volume de transações simultâneas.
- **Cenários de Segurança:** Verifico segurança na transmissão de dados de pagamento.
  
**Pedidos:**

- **Cenários de Sucesso:** Recebo, atualizo e cancelo pedidos com sucesso.
- **Cenários de Falha:** Testo falhas na atualização de pedidos devido a inconsistências de dados.
- **Cenários de Carga:** Realizo testes de desempenho com um grande volume de pedidos simultâneos.
- **Cenários de Segurança:** Verifico acesso não autorizado aos dados de pedidos.

**Preço:**

- **Cenários de Sucesso:** Atualizo preços dos produtos nos marketplaces corretamente.
- **Cenários de Falha:** Testo falhas na atualização de preços devido a problemas de rede ou API.
- **Cenários de Carga:** Realizo testes de desempenho com um grande volume de atualizações de preços.
- **Cenários de Segurança:** Verifico manipulação não autorizada dos preços dos produtos.

**Priorização dos Testes:**

- **Criticidade da Funcionalidade:** Funcionalidades essenciais para o funcionamento do e-commerce e integração com os marketplaces.
- **Impacto no Negócio:** Funcionalidades que têm maior impacto nas operações e receitas do e-commerce.
- **Riscos Potenciais:** Funcionalidades que apresentam maior risco de falhas ou vulnerabilidades.
- **Histórico de Bugs:** Funcionalidades que tiveram problemas em testes anteriores e necessitam de atenção especia.
- **Complexidade Técnica:** Funcionalidades que envolvem lógica de negócios complexa ou múltiplos pontos de integração.
- **Frequência de Uso:** Funcionalidades que são usadas com mais frequência pelos usuários finais.
  
### 3.Execução dos Testes

**Ambiente de Teste:**

- Ambiente de homologação que replica o ambiente de produção, mas sem impactar os usuários finais, permitindo testar todas as funcionalidades da integração de forma segura e controlada.

**Dados de Teste:**

- **Dados de Produtos:** Utilizo dados fictícios de produtos, incluindo informações como nome, descrição, preço e quantidade em estoque.
- **Dados de Estoque:** Gero dados de estoque com diferentes quantidades e localizações para validar a atualização e sincronização de estoque.
- **Dados de Pedidos:** Gero pedidos de teste com diferentes estados (pendente, processado, cancelado) para validar o fluxo de pedidos.
- **Dados de Usuários:** Crio contas de usuário de teste com diferentes perfis e permissões para verificar o acesso e a segurança.
- **Dados de Faturamento:** Simulo transações financeiras para testar o processamento de pagamentos e a geração de faturas.
  
**Ferramentas de Automação:**

- **Ferramentas de Teste Funcional:** Utilizo Cypress para automatizar testes de interface de usuário e garantir que as funcionalidades estejam operando corretamente.
- **Ferramentas de Teste de API:** Utilizo Postman para criar e executar testes automatizados das APIs de integração, verificando a correta comunicação entre o e-commerce e os marketplaces.
- **Ferramentas de Teste de Performance:** Utilizo JMeter para realizar testes de carga e desempenho, garantindo que a integração suporte altos volumes de transações.
- **Ferramentas de Teste de Segurança:** Utilizo OWASP ZAP para identificar e corrigir vulnerabilidades de segurança nas APIs e interfaces de usuário.
  
**Registro de Resultados:**

- **Ferramenta de Gerenciamento de Testes:** Utilizo Jira + Xray para registrar os resultados dos testes, acompanhar o progresso e gerar relatórios detalhados.
- **Ferramenta de Relatórios:** Utilizo Mocha com Mochawesome para gerar relatórios detalhados e visualmente intuitivos dos testes automatizados.
- **Integração CI/CD:** Utilizo GitHub Actions para automatizar a execução dos testes em pipelines, e Cypress Cloud para executar testes em paralelo e obter relatórios centralizados.
  
---
  
## 2º Cenário: Plano de testes para validar a integração com Bling
  
### 1. Documentação e Materiais de Apoio

**Identificação da Documentação:**

- Documentação Oficial da Bling.
- Especificações Técnicas da Integração.
- Requisitos do Projeto.
- Histórico de bugs e relatórios de testes anteriores.

**Análise da documentação:**

- Incluo guias de API, manuais de usuário e qualquer documentação técnica fornecida pela Bling.
- Documentos que detalham como a integração foi implementada, incluindo diagramas de arquitetura, fluxos de dados e especificações de endpoints.
- Documentos que descrevem os requisitos funcionais e não funcionais da integração, incluindo casos de uso, critérios de aceitação e expectativas de desempenho.
- Adiciono uma análise detalhada dos bugs anteriores para identificar padrões e áreas que podem precisar de atenção especial durante os testes.

**Mapeamento dos requisitos:**

- Crio casos de teste específicos para cada requisito funcional e não funcional, garantindo que todos os aspectos da integração sejam validados.
- Utilizo uma matriz de rastreabilidade para garantir que todos os requisitos do projeto estejam cobertos pelos casos de teste.

**Utilização de ferramentas:**

- Para rastreamento de requisitos, criação de casos de teste, gerenciamento de tarefas e colaborar com a equipe: Jira + Xray e Trello.
- Para análise de conteúdo textual, extração de informações significativas e identificação de padrões: MyMap.

### 2. Abrangência dos Testes

**Funcionalidades de Integração:**

- **Sincronização de Produtos:** Testo a criação, atualização e exclusão de produtos para garantir que todas as operações sejam refletidas corretamente.
- **Atualização de Estoque:** Garanto que as quantidades de estoque sejam atualizadas corretamente no Bling e refletidas no e-commerce. Incluir cenários de estoque negativo e excesso de estoque para verificar a resposta do sistema.
- **Processamento de Pedidos:** Valido que os pedidos são processados corretamente e que as informações são transmitidas de forma precisa entre os sistemas. Validar pedidos com diferentes métodos de pagamento e status (pendente, cancelado, concluído).
- **Geração de Relatórios:** Testo a geração de relatórios de estoque, vendas e pedidos para garantir que os dados sejam precisos e completos. Verificar precisão dos relatórios em diferentes períodos (diário, semanal, mensal) e categorias de produtos.
- **Criação e Atualização de Anúncios:** Verifico se os anúncios de produtos são criados e atualizados corretamente no Bling e refletidos no e-commerce. Testar integração com diferentes plataformas de anúncios.
- **Segurança e Permissões:** Asseguro que apenas usuários autorizados possam acessar e modificar dados sensíveis. Realizar testes de acesso com diferentes níveis de permissão.
- **Desempenho:** Avalio a performance da integração sob diferentes condições de carga, incluindo grandes volumes de dados e transações simultâneas.

**Priorização dos testes:**

- **Criticidade da Funcionalidade:** Avalio a importância da funcionalidade para o funcionamento geral do sistema.
- **Impacto no Negócio:** Considero o impacto que a funcionalidade tem no negócio, incluindo receita e operações.
- **Riscos Potenciais:** Identifico os riscos associados à funcionalidade e a probabilidade de falhas.
- **Frequência de Uso:** Priorizo funcionalidades que são usadas com mais frequência pelos usuários.
- **Complexidade da Implementação:** Levo em conta a complexidade técnica da funcionalidade e a probabilidade de erros durante a implementação.

### 3. Execução dos Testes

**Ambiente de Teste:**

- Ambiente de homologação que replica o ambiente de produção, mas sem impactar os usuários finais, permitindo testar todas as funcionalidades da integração de forma segura e controlada.

**Dados de teste:**

- **Dados de Produtos:** Crio um conjunto de dados de produtos com diferentes categorias, preços, descrições e atributos para testar a sincronização e atualização de produtos.
- **Dados de Estoque:** Gero dados de estoque com diferentes quantidades e localizações para validar a atualização e sincronização de estoque.
- **Dados de Pedidos:** Crio dados de pedidos com diferentes status (pendente, processado, cancelado) para testar o processamento e a transmissão de informações entre os sistemas.
- **Dados de Usuários:** Crio contas de usuário de teste com diferentes perfis e permissões para verificar o acesso e a segurança.
- **Dados de Faturamento:** Simulo transações financeiras para testar o processamento de pagamentos e a geração de faturas.
  
**Ferramentas de Automação:**

- **Ferramentas de Teste Funcional:** Utilizo Cypress para automatizar testes de interface de usuário e garantir que as funcionalidades de integração com o Bling estejam operando corretamente.
- **Ferramentas de Teste de API:** Utilizo Postman para criar e executar testes automatizados das APIs de integração, verificando a correta comunicação entre o e-commerce e o Bling.
- **Ferramentas de Teste de Performance:** Utilizo JMeter para realizar testes de carga e desempenho, garantindo que a integração com o Bling suporte altos volumes de transações.
- **Ferramentas de Teste de Segurança:** Utilizo OWASP ZAP para identificar e corrigir vulnerabilidades de segurança nas APIs e interfaces de usuário relacionadas à integração com o Bling.
  
**Registro de Resultados:**

- **Ferramenta de Gerenciamento de Testes:** Utilizo Jira + Xray para registrar os resultados dos testes, acompanhar o progresso e gerar relatórios detalhados.
- **Ferramenta de Relatórios:** Utilizo Mocha com Mochawesome para gerar relatórios detalhados e visualmente intuitivos dos testes automatizados.
- **Integração CI/CD:** Utilizo GitHub Actions para automatizar a execução dos testes em pipelines, e Cypress Cloud para executar testes em paralelo e obter relatórios centralizados.
  
---
  
## 3º Cenário: Anúncios pausados incorretamente, resultando em pedidos sem estoque

### Passos para Análise, Identificação e Resolução do Problema

#### Análise

**Revisar a Documentação:**

- Consulto as regras e condições para que um anúncio seja marcado como "Pausado (sem estoque)" versus "Pausado".
- Verifico se há atualizações recentes na documentação que possam ter alterado o comportamento esperado.

**Verificar os Logs de Integração:**

- Analiso os logs para identificar falhas na comunicação ou na atualização de estoque.
- Verifico se há registros de envio de estoque igual a zero quando o estoque se esgota no Magazord.
- Confirmo se os logs estão completos e se todas as transações foram registradas corretamente.

**Comparar o Comportamento:**

- Comparo anúncios pausados manualmente com aqueles pausados automaticamente.
- Identifico se há diferenças nos logs e nas condições de atualização de estoque.
- Verifico se há padrões específicos que possam indicar a causa do problema.

#### Identificação

**Realizar Testes de Cenários:**

- Realizo testes manuais de atualização de estoque para verificar se o problema pode ser reproduzido.
- Envio atualizações de estoque para zero e observo se o anúncio é marcado como "Pausado (sem estoque)".
- Documento os resultados dos testes para análise posterior.

**Consultar a API:**

- Utilizo a API para consultar o status dos anúncios e verifico inconsistências entre o status retornado pela API e o status exibido na plataforma.
- Configuro alertas para falhas de comunicação e verifico a integridade dos dados enviados e recebidos.
- Confirmo se a API está funcionando corretamente e se há algum problema de latência ou timeout.

**Analisar as Configurações:**

- Verifico as configurações de integração no ERP Magazord e no painel do Mercado Livre para garantir que estejam configuradas corretamente para enviar atualizações de estoque.
- Verifico se há regras específicas configuradas que devem ser acionadas quando o estoque se esgota.
- Confirmo se as configurações estão alinhadas com as práticas recomendadas pela documentação.

#### Resolução

**Falha na Comunicação da API:**

- Implemento monitoramento contínuo da comunicação entre o ERP Magazord e o Mercado Livre para detectar e corrigir falhas rapidamente.
- Configuro alertas para falhas de comunicação e verifico a integridade dos dados enviados e recebidos.

**Configuração Incorreta:**

- Revisito e ajusto as configurações de integração no ERP Magazord e no painel do Mercado Livre.
- Asseguro que as configurações estejam corretas para enviar atualizações de estoque para zero quando o estoque se esgota.

**Bug no Sistema:**

- Reporto o bug para a equipe de desenvolvimento e forneço detalhes específicos para reprodução.
- A equipe de desenvolvimento corrige o bug e realizo novamente os testes para garantir que o problema foi resolvido.

**Diferença de Regras de Negócio:**

- Alinho as regras de negócio no ERP Magazord com as regras do Mercado Livre.
- Atualizo as regras de negócio no ERP para garantir que os anúncios sejam pausados corretamente quando o estoque se esgota.

**Problemas de Sincronização:**

- Implemento verificações de sincronização periódicas entre o ERP Magazord e o Mercado Livre.
- Utilizo ferramentas de sincronização para garantir que os dados de estoque estejam sempre atualizados em ambas as plataformas.

**Interferência Manual:**

- Restringo o acesso manual aos anúncios e implemento controles de auditoria.
- Asseguro que apenas usuários autorizados possam pausar anúncios e que todas as ações sejam registradas para auditoria.
  
### Possíveis Hipóteses do Erro

**Falha na Comunicação da API:**

- A comunicação entre o ERP Magazord e o Mercado Livre pode falhar, resultando em atualizações de estoque não enviadas corretamente.

**Configuração Incorreta:**

- As configurações de integração podem estar incorretas, impedindo o envio de atualizações de estoque para zero quando o estoque se esgota.

**Bug no Sistema:**

- Pode haver um bug no ERP Magazord ou na API do Mercado Livre que impede a atualização correta do status do anúncio.

**Diferença de Regras de Negócio:**

- As regras de negócio no ERP Magazord podem não estar alinhadas com as regras do Mercado Livre para atualização de status de anúncios.

**Problemas de Sincronização:**

- Pode haver problemas de sincronização entre o ERP Magazord e o Mercado Livre, causando atrasos ou falhas na atualização de estoque.

**Interferência Manual:**

- Alguém pode ter pausado manualmente os anúncios sem atualizar o estoque, resultando em inconsistências.

---

## 4º Cenário: Validar campos de cadastro alterados

### Casos de Uso

#### Nome Completo

- **Cenários de Sucesso:** Verifico a inserção correta de nomes completos válidos.
- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de nomes com comprimento mínimo.
  - Testo falhas na inserção de nomes com caracteres especiais.
  - Testo falhas na inserção de nomes com números.

#### E-mail

- **Cenários de Sucesso:** Verifico a inserção correta de e-mails válidos.
- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de e-mails com formato inválido.
  - Testo falhas na inserção de e-mails com domínios inválidos.
  - Testo falhas na inserção de e-mails com espaços em branco.

#### Número de Telefone

- **Cenários de Sucesso:** Verifico a inserção correta de números de telefone válidos.
- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de números de telefone com comprimento mínimo.
  - Testo falhas na inserção de números de telefone com comprimento máximo.
  - Testo falhas na inserção de números de telefone com caracteres especiais.
  - Testo falhas na inserção de números de telefone com letras.
  - Testo falhas na inserção de números de telefone em formatos internacionais.

#### Data de Nascimento

- **Cenários de Sucesso:** Verifico a inserção correta de datas de nascimento válidas.
- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de datas de nascimento com formato inválido.
  - Testo falhas na inserção de datas de nascimento no futuro.
  - Testo falhas na inserção de datas de nascimento com letras.

#### Rua

- **Cenários de Sucesso:** Verifico a inserção correta de ruas válidas.
- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de ruas com caracteres especiais.

#### Cidade

- **Cenários de Sucesso:** Verifico a inserção correta de cidades válidas.

- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de cidades com caracteres especiais.
  - Testo falhas na inserção de cidades com números.

#### Estado

- **Cenários de Sucesso:** Verifico a inserção correta de estados válidos.

- **Cenários de Falha:**
  - Testo falhas na inserção de campo vazio.
  - Testo falhas na inserção de estados com caracteres especiais.
  - Testo falhas na inserção de estados com números.

#### CEP

- **Cenários de Sucesso:** Verifico a inserção correta de CEPs válidos.

- **Cenários de Falha:**
  - Testo falhas na inserção de CEPs com caracteres especiais.
  - Testo falhas na inserção de CEPs com formato inválido.
  - Testo falhas na inserção de CEPs com espaços em branco.

---
