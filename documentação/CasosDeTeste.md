# **Casos de Teste Desafio Megazord**

## Cenário 1°: Integração de Marketplaces

### CT-001 Verificação da Sincronização Correta de Quantidades de Produtos no E-commerce

- **Descrição:** Verificar se a quantidade de produtos é atualizada corretamente no sistema de e-commerce.
- **Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.
- **Prioridade:** Alta
- **Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos e selecionar um produto específico.
2. Atualizar a quantidade de estoque do produto no e-commerce.
3. Salvar as alterações e verificar se a atualização foi bem-sucedida no e-commerce.
4. Verificar a quantidade de estoque do produto no e-commerce para garantir que a atualização foi aplicada corretamente.

- **Resultado esperado:**
  - A quantidade de estoque no e-commerce deve refletir a atualização realizada.

### CT-002: Verificação da Sincronização Correta de Quantidades de Produtos no Marketplace

**Descrição:** Verificar se a quantidade de produtos no marketplace é atualizada corretamente após a alteração no e-commerce.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos no e-commerce e selecionar um produto específico.
2. Atualizar a quantidade de estoque do produto no e-commerce.
3. Salvar as alterações e verificar se a atualização foi bem-sucedida no e-commerce.
4. Navegar até o marketplace e verificar a quantidade de estoque do produto para garantir que a atualização foi sincronizada corretamente.

**Resultado esperado:** A quantidade de estoque no marketplace deve refletir a atualização realizada no e-commerce.

### CT-003: Falha na Atualização de Estoque Devido a Problemas de API

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com falhas na atualização de estoque devido a problemas de API.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos e selecionar um produto específico.
2. Usar Postman para enviar uma resposta de erro 500 ao tentar atualizar o estoque.
3. Tentar atualizar a quantidade de estoque do produto no e-commerce.
4. Salvar as alterações e verificar se uma mensagem de erro é exibida.
5. Verificar a quantidade de estoque do produto no e-commerce para garantir que a atualização não foi aplicada devido ao problema de API.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando o problema de API. A quantidade de estoque no e-commerce não deve ser alterada.

### CT-004: Testes de Desempenho com Grandes Volumes de Atualizações de Estoque

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com grandes volumes de atualizações de estoque.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos e selecionar um conjunto de produtos.
2. Configurar JMeter para enviar múltiplas requisições de atualização de estoque simultaneamente.
3. Executar o teste de carga e monitorar o desempenho do sistema.
4. Verificar se todas as atualizações de estoque foram aplicadas corretamente.
5. Registrar o tempo de resposta e qualquer erro ocorrido durante o teste.

**Resultado esperado:** O sistema deve ser capaz de lidar com grandes volumes de atualizações de estoque sem falhas. O tempo de resposta deve ser aceitável e todas as atualizações devem ser aplicadas corretamente.

### CT-005: Verificação de Acesso Não Autorizado à API de Estoque

**Descrição:** Verificar se o sistema de e-commerce impede o acesso não autorizado à API de estoque.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Credenciais não autorizadas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos e selecionar um produto específico.
2. Usar Postman para enviar uma requisição à API de estoque com credenciais não autorizadas.
3. Tentar acessar ou atualizar a quantidade de estoque do produto usando essas credenciais.
4. Verificar a resposta do sistema e qualquer mensagem de erro exibida.
5. Registrar o comportamento do sistema e garantir que o acesso não autorizado seja bloqueado.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando que o acesso não é autorizado. A API de estoque deve bloquear qualquer tentativa de acesso ou atualização com credenciais não autorizadas.

### CT-006: Criação de Anúncios com Sucesso

**Descrição:** Verificar se o sistema de e-commerce permite a criação de anúncios com sucesso nos marketplaces.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para o anúncio.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Selecionar a opção para criar um novo anúncio.
3. Preencher todos os campos obrigatórios com dados válidos (nome do produto, descrição, preço, imagem).
4. Salvar o anúncio e verificar se a criação foi bem-sucedida.
5. Acessar o marketplace e verificar se o anúncio foi publicado corretamente.

**Resultado esperado:** O anúncio deve ser criado com sucesso no sistema de e-commerce. O anúncio deve ser publicado corretamente no marketplace.

### CT-007: Falha na Criação de Anúncios Devido a Dados Incompletos

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com falhas na criação de anúncios devido a dados incompletos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados incompletos para o anúncio (falta de nome do produto).

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Selecionar a opção para criar um novo anúncio.
3. Preencher os campos obrigatórios com dados incompletos (deixar o campo de nome do produto vazio).
4. Tentar salvar o anúncio.
5. Verificar a mensagem de erro exibida pelo sistema.
6. Registrar o comportamento do sistema e qualquer mensagem de erro.

**Resultado esperado:**  O sistema deve exibir uma mensagem de erro clara indicando que os dados do anúncio estão incompletos. O anúncio não deve ser criado no sistema de e-commerce.

### CT-008: Testes de Desempenho com a Criação de um Grande Número de Anúncios Simultaneamente

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com a criação de um grande número de anúncios simultaneamente.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para múltiplos anúncios.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Usar uma ferramenta de teste de carga, como JMeter, para simular a criação de um grande número de anúncios simultaneamente.
3. Executar o teste de carga e monitorar o desempenho do sistema.
4. Verificar se todos os anúncios foram criados corretamente.
5. Registrar o tempo de resposta e qualquer erro ocorrido durante o teste.

**Resultado esperado:** O sistema deve ser capaz de lidar com a criação de um grande número de anúncios simultaneamente sem falhas. O tempo de resposta deve ser aceitável e todos os anúncios devem ser criados corretamente.

### CT-009: Verificação de Injeção de Código Malicioso nos Campos de Anúncios

**Descrição:** Verificar se o sistema de e-commerce impede a injeção de código malicioso nos campos de anúncios.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados contendo scripts maliciosos nos campos de anúncios.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Selecionar a opção para criar um novo anúncio.
3. Preencher os campo de descrição com script malicioso.
4. Tentar salvar o anúncio.
5. Verificar a resposta do sistema e qualquer mensagem de erro exibida.
6. Registrar o comportamento do sistema e garantir que o código malicioso não seja executado.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando que os dados do anúncio contêm conteúdo inválido. O código malicioso não deve ser executado e deve ser bloqueado pelo sistema.

### CT-010: Atualização de Anúncios com Sucesso

**Descrição:** Verificar se o sistema de e-commerce permite a atualização de anúncios com sucesso nos marketplaces.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Anúncios existentes com dados válidos para atualização.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Selecionar um anúncio existente para atualização.
3. Atualizar os campos necessários (por exemplo, preço, descrição).
4. Salvar as alterações e verificar se a atualização foi bem-sucedida.
5. Acessar o marketplace e verificar se o anúncio foi atualizado corretamente.

**Resultado esperado:** O anúncio deve ser atualizado com sucesso no sistema de e-commerce. O anúncio deve ser atualizado corretamente no marketplace.

### CT-011: Exclusão de Anúncios com Sucesso

**Descrição:** Verificar se o sistema de e-commerce permite a exclusão de anúncios com sucesso nos marketplaces.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Anúncios existentes para exclusão.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios.
2. Selecionar um anúncio existente para exclusão.
3. Confirmar a exclusão do anúncio.
4. Verificar se a exclusão foi bem-sucedida no sistema de e-commerce.
5. Acessar o marketplace e verificar se o anúncio foi removido corretamente.

**Resultado esperado:**  O anúncio deve ser excluído com sucesso no sistema de e-commerce. O anúncio deve ser removido corretamente no marketplace.

### CT-012: Verificação de Permissões de Usuário na Criação de Anúncios

**Descrição:** Verificar se o sistema de e-commerce respeita as permissões de usuário na criação de anúncios.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas e permissões adequadas.

**Massa de dados:** Usuários com diferentes níveis de permissão.

**Prioridade:** Média

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de anúncios com um usuário com permissões limitadas.
2. Tentar criar um novo anúncio.
3. Verificar se o sistema impede a criação de anúncios por usuários sem permissão.
4. Repetir o teste com um usuário com permissões adequadas.

**Resultado esperado:** O sistema deve impedir a criação de anúncios por usuários sem permissão. O sistema deve permitir a criação de anúncios por usuários com permissões adequadas.

### CT-013: Processamento Correto de Pagamentos e Geração de Faturas

**Descrição:** Verificar se o sistema de e-commerce processa pagamentos corretamente e gera faturas de forma adequada.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para transações.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para processamento.
3. Inserir as informações de pagamento válidas.
4. Processar o pagamento.
5. Verificar se o pagamento foi processado com sucesso.
6. Gerar a fatura para o pedido.
7. Verificar se a fatura foi gerada corretamente e contém todas as informações necessárias.

**Resultado esperado:** O pagamento deve ser processado com sucesso. A fatura deve ser gerada corretamente e conter todas as informações necessárias.

### CT-014: Falha no Processamento de Pagamentos Devido a Problemas de Gateway de Pagamento

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com falhas no processamento de pagamentos devido a problemas de gateway de pagamento.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para transações.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para processamento.
3. Inserir as informações de pagamento válidas.
4. Usar Postman para simular uma resposta de erro (502 Bad Gateway) do gateway de pagamento.
5. Tentar processar o pagamento.
6. Verificar a mensagem de erro exibida pelo sistema.
7. Registrar o comportamento do sistema e qualquer mensagem de erro.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando o problema de gateway de pagamento. O pagamento não deve ser processado.

### CT-015: Testes de Desempenho com um Grande Volume de Transações Simultâneas

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com um grande volume de transações simultâneas.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para múltiplas transações.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um conjunto de pedidos para processamento.
3. Configurar JMeter para enviar múltiplas requisições de processamento de pagamento simultaneamente.
4. Executar o teste de carga e monitorar o desempenho do sistema.
5. Verificar se todos os pagamentos foram processados corretamente.
6. Registrar o tempo de resposta e qualquer erro ocorrido durante o teste.

**Resultado esperado:** O sistema deve ser capaz de lidar com um grande volume de transações simultâneas sem falhas. O tempo de resposta deve ser aceitável e todos os pagamentos devem ser processados corretamente.

### CT-016: Verificação de Segurança na Transmissão de Dados de Pagamento

**Descrição:** Verificar se o sistema de e-commerce garante a segurança na transmissão de dados de pagamento.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para transações.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para processamento.
3. Inserir as informações de pagamento válidas.
4. Usar OWASP ZAP para monitorar a transmissão de dados de pagamento.
5. Processar o pagamento.
6. Usando HTTPS, verificar se os dados de pagamento são transmitidos de forma segura.
7. Registrar qualquer vulnerabilidade ou problema de segurança identificado.

**Resultado esperado:** Os dados de pagamento devem ser transmitidos de forma segura, utilizando protocolos de segurança como HTTPS. Não deve haver vulnerabilidades ou problemas de segurança na transmissão de dados de pagamento.

### CT-017: Verificação de Reembolsos

**Descrição:** Verificar se o sistema de e-commerce processa reembolsos corretamente.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos válidos que necessitam de reembolso.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para reembolso.
3. Processar o reembolso.
4. Verificar se o reembolso foi processado com sucesso.
5. Verificar se a fatura foi atualizada corretamente para refletir o reembolso.

**Resultado esperado:** O reembolso deve ser processado com sucesso.A fatura deve ser atualizada corretamente para refletir o reembolso.

### CT-018: Verificação de Pagamentos Parciais

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com pagamentos parciais.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos válidos que permitem pagamentos parciais.

**Prioridade:** Média

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para pagamento parcial.
3. Inserir as informações de pagamento parcial válidas.
4. Processar o pagamento parcial.
5. Verificar se o pagamento parcial foi processado com sucesso.
6. Verificar se a fatura foi gerada corretamente para refletir o pagamento parcial.

**Resultado esperado:** O pagamento parcial deve ser processado com sucesso. A fatura deve ser gerada corretamente para refletir o pagamento parcial.

### CT-019: Verificação de Diversos Métodos de Pagamento

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com diversos métodos de pagamento (cartão de crédito, PayPal, PIX e cartão débito).

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos válidos com diferentes métodos de pagamento.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para processamento.
3. Inserir as informações de pagamento válidas para diferentes métodos de pagamento.
4. Processar o pagamento.
5. Verificar se o pagamento foi processado com sucesso para cada método de pagamento.
6. Gerar a fatura para o pedido.
7. Verificar se a fatura foi gerada corretamente e contém todas as informações necessárias.

**Resultado esperado:** O pagamento deve ser processado com sucesso para cada método de pagamento. A fatura deve ser gerada corretamente e conter todas as informações necessárias.

### CT-020: Cancelamento de Pedidos com Sucesso

**Descrição:** Verificar se o sistema de e-commerce permite o cancelamento de pedidos corretamente.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos existentes com dados válidos.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para cancelamento.
3. Confirmar o cancelamento do pedido.
4. Verificar se o pedido foi cancelado com sucesso.
5. Verificar se o pedido aparece como cancelado na lista de pedidos.

**Resultado esperado:** O pedido deve ser cancelado com sucesso e aparecer como cancelado na lista de pedidos.

### CT-021: Falha na Atualização de Pedidos Devido a Inconsistências de Dados

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com falhas na atualização de pedidos devido a inconsistências de dados.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos existentes com dados inconsistentes.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para atualização.
3. Tentar atualizar quantidade de produtos maior do que o disponível em estoque.
4. Salvar as alterações e verificar se uma mensagem de erro é exibida.
5. Verificar se o pedido não foi atualizado devido às inconsistências de dados.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando as inconsistências de dados. O pedido não deve ser atualizado.

### CT-022: Testes de Desempenho com um Grande Volume de Pedidos Simultâneos

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com um grande volume de pedidos simultâneos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Dados completos e válidos para múltiplos pedidos.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Usar JMeter para simular a criação de um grande volume de pedidos simultâneos.
3. Executar o teste de carga e monitorar o desempenho do sistema.
4. Verificar se todos os pedidos foram processados corretamente.
5. Registrar o tempo de resposta e qualquer erro ocorrido durante o teste.

**Resultado esperado:** O sistema deve ser capaz de lidar com um grande volume de pedidos simultâneos sem falhas. O tempo de resposta deve ser aceitável e todos os pedidos devem ser processados corretamente.

### CT-023: Verificação de Acesso Não Autorizado aos Dados de Pedidos

**Descrição:** Verificar se o sistema de e-commerce impede o acesso não autorizado aos dados de pedidos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Credenciais inválidas ou não autorizadas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Usar uma ferramenta como Postman para enviar uma requisição aos dados de pedidos com credenciais não autorizadas.
3. Tentar acessar ou atualizar os dados de pedidos usando essas credenciais.
4. Verificar a resposta do sistema e qualquer mensagem de erro exibida.
5. Registrar o comportamento do sistema e garantir que o acesso não autorizado seja bloqueado.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando que o acesso não é autorizado. O acesso aos dados de pedidos deve ser bloqueado para credenciais não autorizadas.

### CT-024: Verificação de Atualização de Status de Pedido

**Descrição:** Verificar se o sistema de e-commerce permite a atualização do status de pedidos corretamente.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Pedidos existentes com dados válidos.

**Prioridade:** Alta

**asso a passo para execução:**

1. Navegar até a seção de gerenciamento de pedidos.
2. Selecionar um pedido específico para atualização.
3. Atualizar o status do pedido (por exemplo, de "Processando" para "Enviado").
4. Salvar as alterações e verificar se a atualização foi bem-sucedida.
5. Verificar se o status do pedido foi atualizado corretamente na lista de pedidos.

**Resultado esperado:** O status do pedido deve ser atualizado com sucesso e refletido corretamente na lista de pedidos.

### CT-025: Atualização Correta dos Preços dos Produtos nos Marketplaces

**Descrição:** Verificar se o sistema de e-commerce atualiza corretamente os preços dos produtos nos marketplaces.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com preços válidos e atualizados.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Selecionar um produto específico para atualização de preço.
3. Atualizar o preço do produto no sistema de e-commerce.
4. Salvar as alterações e verificar se a atualização foi bem-sucedida no e-commerce.
5. Acessar o marketplace e verificar se o preço do produto foi atualizado corretamente.

**Resultado esperado:** O preço do produto deve ser atualizado corretamente no sistema de e-commerce e refletido no marketplace.

### CT-026: Falha na Atualização de Preços Devido a Problemas de API

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com falhas na atualização de preços devido a problemas de API.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com preços válidos.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Selecionar um produto específico para atualização de preço.
3. Usar Postman para simular uma resposta de erro 500 ao tentar atualizar o preço.
4.Tentar atualizar o preço do produto no sistema de e-commerce.
5.Salvar as alterações e verificar se uma mensagem de erro é exibida.
6.Verificar se o preço do produto no e-commerce não foi alterado devido ao problema de API.
**Resultado esperado:**

- O sistema deve exibir uma mensagem de erro clara indicando o problema de API.
- O preço do produto no e-commerce não deve ser alterado.

### CT-027: Testes de Desempenho com um Grande Volume de Atualizações de Preços

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com um grande volume de atualizações de preços.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com preços válidos para múltiplas atualizações.

**Prioridade:** Alta

1. Passo a passo para execução:
2. Navegar até a seção de gerenciamento de produtos.
3. Selecionar um conjunto de produtos para atualização de preços.
4. Configurar JMeter para enviar múltiplas requisições de atualização de preços simultaneamente.
5. Executar o teste de carga e monitorar o desempenho do sistema.
6. Verificar se todas as atualizações de preços foram aplicadas corretamente.
7. Registrar o tempo de resposta e qualquer erro ocorrido durante o teste.

**Resultado esperado:** O sistema deve ser capaz de lidar com um grande volume de atualizações de preços sem falhas. O tempo de resposta deve ser aceitável e todas as atualizações devem ser aplicadas corretamente.

### CT-028: Verificação de Manipulação Não Autorizada dos Preços dos Produtos

**Descrição:** Verificar se o sistema de e-commerce impede a manipulação não autorizada dos preços dos produtos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Credenciais não autorizadas.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Usar Postman para enviar uma requisição de atualização de preços com credenciais não autorizadas.
3. Tentar atualizar o preço de um produto usando essas credenciais.
4. Verificar a resposta do sistema e qualquer mensagem de erro exibida.
5. Registrar o comportamento do sistema e garantir que a manipulação não autorizada seja bloqueada.

**Resultado esperado:** O sistema deve exibir uma mensagem de erro clara indicando que o acesso não é autorizado. A atualização de preços deve ser bloqueada para credenciais não autorizadas.

### CT-029: Verificação de Atualização de Preços em Diferentes Moedas

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com a atualização de preços em diferentes moedas.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com preços válidos em diferentes moedas.

**Prioridade:** Média

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Selecionar um produto específico para atualização de preço.
3. Atualizar o preço do produto em diferentes moedas no sistema de e-commerce.
4. Salvar as alterações e verificar se a atualização foi bem-sucedida no e-commerce.
5. Acessar o marketplace e verificar se o preço do produto foi atualizado corretamente em diferentes moedas.

**Resultado esperado:** O preço do produto deve ser atualizado corretamente no sistema de e-commerce e refletido no marketplace em diferentes moedas.

### CT-030: Verificação de Descontos e Promoções

**Descrição:** Verificar se o sistema de e-commerce lida corretamente com a aplicação de descontos e promoções nos preços dos produtos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com preços válidos e descontos aplicáveis.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Selecionar um produto específico para aplicação de desconto ou promoção.
3. Aplicar o desconto ou promoção ao preço do produto no sistema de e-commerce.
4. Salvar as alterações e verificar se a atualização foi bem-sucedida no e-commerce.
5. Acessar o marketplace e verificar se o preço do produto com desconto ou promoção foi atualizado corretamente.

**Resultado esperado:** O preço do produto com desconto ou promoção deve ser atualizado corretamente no sistema de e-commerce e refletido no marketplace.

### CT-031: Verificação de Histórico de Preços

**Descrição:** Verificar se o sistema de e-commerce mantém um histórico de alterações de preços dos produtos.

**Pré-condições:** A integração entre o e-commerce e o marketplace deve estar configurada e ativa. O usuário deve estar logado no sistema de e-commerce com credenciais válidas.

**Massa de dados:** Produtos com histórico de alterações de preços.

**Prioridade:** Média

**Passo a passo para execução:**

1. Navegar até a seção de gerenciamento de produtos.
2. Selecionar um produto específico para visualização do histórico de preços.
3. Verificar se o histórico de alterações de preços é exibido corretamente.
4. Verificar se todas as alterações de preços estão registradas no histórico.

**Resultado esperado:** O histórico de alterações de preços deve ser exibido corretamente. Todas as alterações de preços devem estar registradas no histórico.

---

## Cenário 4°: Validação de Dados Cadastrais

### CT-032: Nome Completo - Entrada Válida

**Descrição:** Verificar a inserção correta de nomes completos válidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Bruno Soares Ribeiro" no campo Nome Completo.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o nome completo e salva o registro corretamente.

### CT-033: Nome Completo - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio no nome completo.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Nome Completo vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-034: Nome Completo - Comprimento Mínimo

**Descrição:** Verificar a inserção de nomes com comprimento mínimo.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "A" no campo Nome Completo.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o nome é muito curto.

### CT-035: Nome Completo - Caracteres Especiais

**Descrição:** Verificar a inserção de nomes com caracteres especiais não permitidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Bruno So@res Ribeiro" no campo Nome Completo.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não permitidos foram inseridos.

### CT-036: Nome Completo - Números

**Descrição:** Verificar a inserção de nomes com números.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Bruno123" no campo Nome Completo.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que números não são permitidos.

### CT-037: E-mail - Entrada Válida

**Descrição:** Verificar a inserção correta de e-mails válidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir 'brunosr099@outlook.com' no campo e-mail.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o e-mail e salva o registro corretamente.

### CT-038: E-mail - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio no e-mail.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo e-mail vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-039: E-mail - Formato Inválido

**Descrição:** Verificar a inserção de e-mails com formato inválido.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "bruno@" no campo e-mail.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o formato do e-mail é inválido.

### CT-040: E-mail - Domínios Inválidos

**Descrição:** Verificar a inserção de e-mails com domínios inválidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "bruno@dominio" no campo e-mail.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o domínio do e-mail é inválido.

### CT-041: E-mail - Espaços em Branco

**Descrição:** Verificar a inserção de e-mails com espaços em branco.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir 'bruno@ dominio. com' no campo E-mail.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que espaços em branco não são permitidos.

### CT-042: Número de Telefone - Entrada Válida

**Descrição:** Verificar a inserção correta de números de telefone válidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "+55 55 99937-3610" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o número de telefone e salva o registro corretamente.

### CT-043: Número de Telefone - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio no número de telefone.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Número de Telefone vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-044: Número de Telefone - Comprimento Mínimo

**Descrição:** Verificar a inserção de números de telefone com comprimento mínimo.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "123" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o número de telefone é muito curto.

### CT-045: Número de Telefone - Comprimento Máximo

**Descrição:** Verificar a inserção de números de telefone com comprimento máximo.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "+55 55 99937-361000" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o número de telefone é muito longo.

### CT-046: Número de Telefone - Caracteres Especiais

**Descrição:** Verificar a inserção de números de telefone com caracteres especiais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "+55 55 99937 3610!" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não são permitidos.

### CT-047: Número de Telefone - Letras

**Descrição:** Verificar a inserção de números de telefone com letras.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "+55 55 99937-ABCD" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que letras não são permitidas.

### CT-048: Número de Telefone - Formatos Internacionais

**Descrição:** Verificar a inserção de números de telefone em formatos internacionais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "+1 123-456-7890" no campo Número de Telefone.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o número de telefone e salva o registro corretamente.

### CT-049: Data de Nascimento - Entrada Válida

**Descrição:** Verificar a inserção correta de datas de nascimento válidas.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "19/01/1999" no campo Data de Nascimento.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita a data de nascimento e salva o registro corretamente.

### CT-050: Data de Nascimento - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio na data de nascimento.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Data de Nascimento vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-051: Data de Nascimento - Formato Inválido

**Descrição:** Verificar a inserção de datas de nascimento com formato inválido.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "2000-01-01" no campo Data de Nascimento.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o formato da data é inválido.

### CT-052: Data de Nascimento - Data Futura

**Descrição:** Verificar a inserção de datas de nascimento no futuro.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "01/01/2030" no campo Data de Nascimento.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que a data de nascimento não pode ser no futuro.

### CT-053: Data de Nascimento - Letras

**Descrição:** Verificar a inserção de datas de nascimento com letras.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "01/jan/2000" no campo Data de Nascimento.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que letras não são permitidas.

### CT-054: Rua - Entrada Válida

**Descrição:** Verificar a inserção correta de ruas válidas.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Estr. da Madeira, 1875" no campo Rua.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita a rua e salva o registro corretamente.

### CT-055: Rua - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio na rua.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Rua vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-056: Rua - Caracteres Especiais

**Descrição:** Verificar a inserção de ruas com caracteres especiais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Estr. da Madeira!@#" no campo Rua.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não são permitidos.

### CT-057: Cidade - Entrada Válida

**Descrição:** Verificar a inserção correta de cidades válidas.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Rio do Sul" no campo Cidade.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita a cidade e salva o registro corretamente.

### CT-058: Cidade - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio na cidade.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Cidade vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-059: Cidade - Caracteres Especiais

**Descrição:** Verificar a inserção de cidades com caracteres especiais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Rio do Sul!@#" no campo Cidade.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não são permitidos.

### CT-060: Cidade - Números

**Descrição:** Verificar a inserção de cidades com números.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "Rio do Sul123" no campo Cidade.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que números não são permitidos.

### CT-061: Estado - Entrada Válida

**Descrição:** Verificar a inserção correta de estados válidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "SC" no campo Estado.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o estado e salva o registro corretamente.

### CT-062: Estado - Campo Vazio

**Descrição:** Verificar a inserção de campo vazio no estado.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Deixar o campo Estado vazio.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o campo é obrigatório.

### CT-063: Estado - Caracteres Especiais

**Descrição:** Verificar a inserção de estados com caracteres especiais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "SC!@#" no campo Estado.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não são permitidos.

### CT-064: Estado - Números

**Descrição:** Verificar a inserção de estados com números.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "SC123" no campo Estado.
3. Submeter o formulário.

**esultado esperado:** O sistema exibe uma mensagem de erro indicando que números não são permitidos.

### CT-065: CEP - Entrada Válida

**Descrição:** Verificar a inserção correta de CEPs válidos.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "89165-063" no campo CEP.
3. Submeter o formulário.

**Resultado esperado:** O sistema aceita o CEP e salva o registro corretamente.

### CT-066: CEP - Caracteres Especiais

**Descrição:** Verificar a inserção de CEPs com caracteres especiais.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "89165-063!" no campo CEP.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que caracteres especiais não são permitidos.

### CT-067: CEP - Formato Inválido

**Descrição:** Verificar a inserção de CEPs com formato inválido.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Alta

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir "89-165063" no campo CEP.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que o formato do CEP é inválido.

### CT-068: CEP - Espaços em Branco

**Descrição:** Verificar a inserção de CEPs com espaços em branco.

**Pré-condições:** Sistema de gerenciamento de usuários ativo.

**Prioridade:** Média

**Passo a passo para execução:**

1. Acessar a página de cadastro.
2. Inserir ' 891650 63' no campo CEP.
3. Submeter o formulário.

**Resultado esperado:** O sistema exibe uma mensagem de erro indicando que espaços em branco não são permitidos.

## Observações Importantes

**Nota:** Os testes descritos neste documento ainda não foram executados. Portanto, os resultados atuais não foram documentados.

---