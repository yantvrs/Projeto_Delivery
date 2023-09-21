# Sistema de Delivery 🍔🚚

Projeto desenvolvido por Yan Tavares, Pedro Rêgo, Jordan Marques e Cristian Soares como parte da disciplina de Projeto de Engenharia de Software ofertada pela Universidade Federal do Rio Grande do Norte.

## Ator 1: Cliente

### Realizar cadastro
- Fluxo Normal:
  1. Cliente informa Nome
  2. Cliente informa CPF
  3. Cliente informa Número de contato
  4. Cliente informa E-mail
  5. Cliente informa Senha
  6. Sistema cria o usuário
- Extensões:
   2a. Se o CPF for inválido, solicitar novamente.
   5a. Se a senha for inferior a 6 caracteres, solicitar novamente.

### Realizar login
- Fluxo Normal:
  - Cliente informa email
  - Cliente informa senha
  - Sistema realiza login
- Extensões:
  - 1a. Se o e-mail for inválido, solicitar novamente.
  - 2a. Se a senha for inválida, solicitar novamente.

### Realizar pedido
- Fluxo Normal:
  - Cliente explora o cardápio
  - Cliente adiciona itens ao carrinho
  - Cliente seleciona endereço
  - Cliente informa forma de pagamento (Dinheiro/Cartão)
  - Cliente verifica o pedido
  - Cliente confirma pedido
- Extensões:
  - 3a. Se não houver endereço cadastrado, cliente cria endereço.
  - 4a. Se forma de pagamento for dinheiro, cliente informa troco
  - 5a. Se desejar, cliente pode remover algum item

### Criar endereço
- Fluxo Normal:
  - Cliente informa CEP
  - Sistema valida o CEP
  - Sistema preenche informações com base no CEP preenchido
  - Cliente informa Número
  - Cliente informa Complemento (ex.: Bloco/Apto)
- Extensões:
  - 2a. Se o CEP não for atendido, solicitar novamente
  - 3a. Se as informações não forem preenchidas, cliente informa manualmente

### Acompanhar pedido
- Fluxo Normal:
  - Sistema exibe lista de pedidos
  - Cliente seleciona o pedido que deseja acompanhar
  - Sistema exibe informações detalhadas sobre o pedido

## Ator 2: Gerente

### Adicionar itens ao cardápio
- Fluxo Normal:
  - Gerente informa Nome do item
  - Gerente informa Descrição
  - Gerente informa Categoria
  - Gerente informa Preço
  - Gerente adiciona Foto
  - Sistema cria item

### Alterar itens do cardápio
- Fluxo Normal:
  - Sistema exibe lista de itens
  - Gerente seleciona item que deseja alterar
  - Sistema exibe campos com atuais informações do item
  - Gerente edita os campos desejados
  - Sistema exibe confirmação
  - Gerente confirma alteração
  - Sistema atualiza o cardápio

### Remover itens do cardápio
- Fluxo Normal:
  - Sistema exibe lista de itens do cardápio
  - Gerente seleciona os itens que deseja remover
  - Sistema exibe confirmação
  - Gerente confirma
  - Sistema atualiza o cardápio

### Aceitar ou Recusar pedidos
- Fluxo Normal:
  - Sistema exibe lista de pedidos realizados
  - Gerente acessa detalhes do pedido
  - Gerente confirma ou não o pedido
- Extensões:
  - 3a. Caso confirmado, Sistema envia pedido para cozinha
  - 3b. Caso negado, Gerente informa motivo, Sistema cancela e informa o cliente

### Direcionar pedidos para entrega
- Fluxo Normal:
  - Sistema exibe para o gerente os pedidos finalizados pela cozinha
  - Gerente direciona pedido para entregador disponível
  - Sistema atualiza status do pedido para disponível para entrega

### Alterar funcionamento da loja
- Fluxo Normal:
  - Gerente torna indisponível a efetuação de pedidos, ainda que dentro do horário de funcionamento, por motivos internos.

## Ator 3: Cozinha

### Confirmar recebimento
- Fluxo Normal:
  - Sistema mostra pedidos a serem feitos
  - Cozinha confirma o recebimento do pedido
- Extensões:
  - 2a. Caso cozinha não confirme, pedido volta para gerente

### Marcar como concluído
- Fluxo Normal:
  - Sistema exibe pedidos em andamento
  - Cozinha confirma a conclusão

## Ator 4: Entregador

### Efetuar entrega
- Fluxo Normal:
  - Sistema envia notificação ao entregador de pedido disponível para entrega
  - Entregador coleta pedido e altera status do pedido para Em Entrega
  - Ao finalizar entrega, marcar como Entregue

## Ator 5: Administrador

### Cadastrar funcionário
- Fluxo Normal:
  - Administrador informa Nome do funcionário
  - Administrador informa CPF do funcionário
  - Administrador informa Email do funcionário
  - Administrador informa Perfil do funcionário
  - Administrador informa Contato do funcionário
- Extensões:
  - 2a. Se CPF for inválido, solicitar novamente

### Editar funcionário
- Fluxo Normal:
  - Sistema exibe lista de funcionários
  - Sistema exibe campos com informações editáveis do funcionário
  - Administrador edita campos desejados
  - Sistema exibe confirmação
  - Administrador confirma
  - Sistema atualiza informações do funcionário
- Extensões:
  - 5a. Caso negado, Sistema volta para tela de campos

### Remover funcionário
- Fluxo Normal:
  - Sistema exibe lista de funcionários
  - Administrador seleciona funcionários que serão removidos
  - Sistema exibe confirmação
  - Administrador confirma a remoção
- Extensões:
  - 5a. Caso negado, Sistema volta para lista de funcionários

## Ator 6: Sistema

### Exibe informações
- Fluxo Normal:
  - Sistema verifica perfis de usuários e delimita permissões com base no perfil
  - Sistema exibe quantidade de entregas efetuadas, em andamento e disponíveis
  - Sistema notifica todos os usuários sobre status dos pedidos.
  - Sistema exibe lucro diário ou em determinado período
  - Sistema exibe quantidade de funcionários por perfil
  - Sistema exibe quantidade de entregas por entregador
  - Sistema exibe média dos valores dos pedidos
  - Sistema exibe tempo médio de entregas
  - Sistema exibe tempo médio da preparação dos pedidos pela cozinha
  - Sistema exibe quantidade de usuários cadastrados/utilizando

## Licença 📄

Este projeto é licenciado sob a [MIT License](LICENSE.md).

## Agradecimentos 👏

Agradecemos a todos que contribuíram para o desenvolvimento deste sistema! 🙌

## Perfis dos Desenvolvedores no GitHub

- [Perfil do GitHub de Yan Tavares](https://github.com/yan-tavares)
- [Perfil do GitHub de Pedro Rêgo](https://github.com/pedrorego)
- [Perfil do GitHub de Jordan Marques](https://github.com/jordan-marques)
- [Perfil do GitHub de Cristian Soares](https://github.com/cristian-soares)
