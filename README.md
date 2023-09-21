# Sistema de Delivery 🍔🚚

## Visão Geral do Projeto

O projeto "Sistema de Delivery" é um sistema de software desenvolvido como parte da disciplina de Projeto de Engenharia de Software, oferecida pela Universidade Federal do Rio Grande do Norte. O objetivo principal deste projeto é criar uma plataforma de delivery de alimentos que permite aos clientes realizar pedidos de restaurantes locais e acompanhar o status de seus pedidos em tempo real. Além disso, o sistema oferece ferramentas de gerenciamento para os restaurantes.

# Casos de uso
- Diagrama de Casos de Uso
![Diagrama de Casos de Uso para o sistema delivery](https://github.com/yantvrs/Projeto_Delivery/blob/main/images/Diagrama%20de%20casos%20de%20uso_page-0001.jpg)


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
  - 2a. Se o CPF for inválido, solicitar novamente.
  - 5a. Se a senha for inferior a 6 caracteres, solicitar novamente.

### Realizar login
- Fluxo Normal:
1. Cliente informa email
2. Cliente informa senha
3. Sistema realiza login
- Extensões:
  - 1a. Se o e-mail for inválido, solicitar novamente.
  - 2a. Se a senha for inválida, solicitar novamente.

### Realizar pedido
- Fluxo Normal:
1. Cliente explora o cardápio
2. Cliente adiciona itens ao carrinho
3. Cliente seleciona endereço
4. Cliente informa forma de pagamento (Dinheiro/Cartão)
5. Cliente verifica o pedido
6. Cliente confirma pedido
- Extensões:
  - 3a. Se não houver endereço cadastrado, cliente cria endereço.
  - 4a. Se forma de pagamento for dinheiro, cliente informa troco
  - 5a. Se desejar, cliente pode remover algum item

### Criar endereço
- Fluxo Normal:
1. Cliente informa CEP
2. Sistema valida o CEP
3. Sistema preenche informações com base no CEP preenchido
4. Cliente informa Número
5. Cliente informa Complemento (ex.: Bloco/Apto)
- Extensões:
  - 2a. Se o CEP não for atendido, solicitar novamente
  - 3a. Se as informações não forem preenchidas, cliente informa manualmente

### Acompanhar pedido
- Fluxo Normal:
1. Sistema exibe lista de pedidos
2. Cliente seleciona o pedido que deseja acompanhar
3. Sistema exibe informações detalhadas sobre o pedido

## Ator 2: Gerente

### Adicionar itens ao cardápio
- Fluxo Normal:
1. Gerente informa Nome do item
2. Gerente informa Descrição
3. Gerente informa Categoria
4. Gerente informa Preço
5. Gerente adiciona Foto
6. Sistema cria item

### Alterar itens do cardápio
- Fluxo Normal:
1. Sistema exibe lista de itens
2. Gerente seleciona item que deseja alterar
3. Sistema exibe campos com atuais informações do item
4. Gerente edita os campos desejados
5. Sistema exibe confirmação
6. Gerente confirma alteração
7. Sistema atualiza o cardápio

### Remover itens do cardápio
- Fluxo Normal:
1. Sistema exibe lista de itens do cardápio
2. Gerente seleciona os itens que deseja remover
3. Sistema exibe confirmação
4. Gerente confirma
5. Sistema atualiza o cardápio

### Aceitar ou Recusar pedidos
- Fluxo Normal:
1. Sistema exibe lista de pedidos realizados
2. Gerente acessa detalhes do pedido
3. Gerente confirma ou não o pedido
- Extensões:
  - 3a. Caso confirmado, Sistema envia pedido para cozinha
  - 3b. Caso negado, Gerente informa motivo, Sistema cancela e informa o cliente

### Direcionar pedidos para entrega
- Fluxo Normal:
1. Sistema exibe para o gerente os pedidos finalizados pela cozinha
2. Gerente direciona pedido para entregador disponível
3. Sistema atualiza status do pedido para disponível para entrega

### Alterar funcionamento da loja
- Fluxo Normal:
1. Gerente torna indisponível a efetuação de pedidos, ainda que dentro do horário de funcionamento, por motivos internos.

## Ator 3: Cozinha

### Confirmar recebimento
- Fluxo Normal:
1. Sistema mostra pedidos a serem feitos
2. Cozinha confirma o recebimento do pedido
- Extensões:
  - 2a. Caso cozinha não confirme, pedido volta para gerente

### Marcar como concluído
- Fluxo Normal:
1. Sistema exibe pedidos em andamento
2. Cozinha confirma a conclusão

## Ator 4: Entregador

### Efetuar entrega
- Fluxo Normal:
1. Sistema envia notificação ao entregador de pedido disponível para entrega
2. Entregador coleta pedido e altera status do pedido para Em Entrega
3. Ao finalizar entrega, marcar como Entregue

## Ator 5: Administrador

### Cadastrar funcionário
- Fluxo Normal:
1. Administrador informa Nome do funcionário
2. Administrador informa CPF do funcionário
3. Administrador informa Email do funcionário
4. Administrador informa Perfil do funcionário
5. Administrador informa Contato do funcionário
- Extensões:
  - 2a. Se CPF for inválido, solicitar novamente

### Editar funcionário
- Fluxo Normal:
1. Sistema exibe lista de funcionários
2. Sistema exibe campos com informações editáveis do funcionário
3. Administrador edita campos desejados
4. Sistema exibe confirmação
5. Administrador confirma
6. Sistema atualiza informações do funcionário
- Extensões:
  - 5a. Caso negado, Sistema volta para tela de campos

### Remover funcionário
- Fluxo Normal:
1. Sistema exibe lista de funcionários
2. Administrador seleciona funcionários que serão removidos
3. Sistema exibe confirmação
4. Administrador confirma a remoção
- Extensões:
  - 5a. Caso negado, Sistema volta para lista de funcionários

## Ator 6: Sistema

### Exibe informações
- Fluxo Normal:
1. Sistema verifica perfis de usuários e delimita permissões com base no perfil
2. Sistema exibe quantidade de entregas efetuadas, em andamento e disponíveis
3. Sistema notifica todos os usuários sobre status dos pedidos.
4. Sistema exibe lucro diário ou em determinado período
5. Sistema exibe quantidade de funcionários por perfil
6. Sistema exibe quantidade de entregas por entregador
7. Sistema exibe média dos valores dos pedidos
8. Sistema exibe tempo médio de entregas
9. Sistema exibe tempo médio da preparação dos pedidos pela cozinha
10. Sistema exibe quantidade de usuários cadastrados/utilizando

# Histórias de Usuário

## Cliente:

- Como cliente, desejo me cadastrar na plataforma.
- Como cliente, desejo fazer login na minha conta para fazer pedidos.
- Como cliente, desejo navegar pelo cardápio, selecionar itens e adicioná-los ao meu pedido.
- Como cliente, desejo escolher a forma de pagamento, o endereço da entrega e finalizar meu pedido.
- Como cliente, desejo receber atualizações sobre o status do meu pedido.

## Gerente:

- Como gerente, desejo adicionar novas opções ao cardápio do restaurante.
- Como gerente, desejo receber notificações sobre novos pedidos e ter a capacidade de aceitar ou recusar pedidos.
- Como gerente, desejo designar entregadores para realizar as entregas de pedidos.
- Como gerente, desejo criar novos pedidos manualmente, se necessário.

## Cozinha:

- Como membro da equipe de cozinha, desejo confirmar o recebimento de pedidos para começar a preparação, ou recusá-los por algum motivo.
- Como membro da equipe de cozinha, desejo marcar pedidos como concluídos após a preparação.

## Entregador:

- Como entregador, desejo receber notificações sobre os pedidos que devo entregar.
- Como entregador, desejo marcar os pedidos como entregues após a entrega bem-sucedida.

## Administrador:

- Como administrador, desejo cadastrar os perfis de funcionários (gerente, cozinha e entregador).
- Como administrador, desejo acessar dados gerais e estatísticas sobre os pedidos e o desempenho do restaurante.

# Requisitos Funcionais

## Sistema de Autenticação:

- Cadastro de clientes e perfis de funcionários.
- Login para todos os perfis e diferenciação dos acessos de cada perfil.
- Acesso e gerenciamento de dados pessoais de cada usuário.

## Cardápio:

- Gerenciamento de itens de menu pelo gerente.
- Navegação e seleção de itens de menu pelos clientes.

## Pedidos:

- Clientes podem criar pedidos.
- O Gerente pode aceitar ou recusar pedidos.
- A cozinha pode confirmar, recusar e concluir pedidos.
- Entregadores recebem, efetuam e concluem entregas.

## Gestão de Funcionários e Dados:

- O administrador pode gerenciar perfis de gerente, cozinha e entregador.

## Notificações:

- Notificações em tempo real para clientes sobre o status do pedido.
- Notificações para o gerente sobre novos pedidos.
- Notificações para os funcionários da cozinha sobre novos pedidos.
- Notificações para entregadores sobre pedidos a serem entregues.


## Agradecimentos 👏

Agradecemos a todos que contribuíram para o desenvolvimento deste sistema! 🙌

## Perfis dos Desenvolvedores no GitHub

- [Cristian Soares](https://github.com/criric)
- [Jordan Marques](https://github.com/jordanmaramos)
- [Pedro Rêgo](https://github.com/pedrorvn)
- [Yan Tavares](https://github.com/yantvrs)
