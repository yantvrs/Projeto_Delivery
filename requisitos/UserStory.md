# Histórias de Usuário

## Cliente:

- Como cliente, desejo me cadastrar na plataforma.
  - Deve haver um formulário de registro com campos obrigatórios, como nome, e-mail e senha.
  - O sistema deve validar se o e-mail fornecido é único.
  - Após o registro bem-sucedido, o cliente deve ser automaticamente redirecionado para a página de login.

- Como cliente, desejo fazer login na minha conta para fazer pedidos.
  - Deve haver um formulário de login com campos obrigatórios, como e-mail e senha.
  - O sistema deve permitir o acesso apenas a clientes registrados e com credenciais válidas.
  - Após o login bem-sucedido, o cliente deve ser redirecionado para a página de navegação do cardápio.
  
- Como cliente, desejo navegar pelo cardápio, selecionar itens e adicioná-los ao meu pedido.
  - O cliente deve ser capaz de visualizar o cardápio completo com descrições e preços.
  - Deve haver a opção de adicionar itens ao carrinho de compras.
  - O cliente deve poder ajustar a quantidade de itens no carrinho.

- Como cliente, desejo escolher a forma de pagamento, o endereço da entrega e finalizar meu pedido.
  - O cliente deve ser guiado através do processo de finalização do pedido, incluindo a seleção do endereço de entrega e opção de pagamento.
  - Deve ser possível revisar o pedido antes de confirmá-lo.
  - Após a confirmação, o pedido deve ser processado e uma confirmação de pedido deve ser exibida.
  
- Como cliente, desejo receber atualizações sobre o status do meu pedido.
  - O cliente deve receber notificações por e-mail ou no aplicativo sobre o progresso do pedido, incluindo confirmação, preparação, entrega e conclusão.  

## Gerente:

- Como gerente, desejo gerenciar (adicionar/editar/remover) opções ao cardápio do restaurante.
  - Deve haver uma interface de gerenciamento de cardápio onde o gerente pode alterar itens com nome, descrição e preço.
  - Os novos itens devem ser exibidos no cardápio para os clientes após a adição.

- Como gerente, desejo receber notificações sobre novos pedidos e ter a capacidade de aceitar ou recusar pedidos.
  - O gerente deve receber notificações em tempo real sobre novos pedidos.
  - Deve haver uma opção para o gerente aceitar ou recusar pedidos.

- Como gerente, desejo designar entregadores para realizar as entregas de pedidos.
  - Deve haver uma interface para atribuir entregadores a pedidos pendentes.
  - O status do pedido deve ser atualizado para "Em rota de entrega" após a atribuição do entregador. 

- Como gerente, desejo criar novos pedidos manualmente, se necessário.
  - O gerente deve ter a capacidade de criar pedidos manualmente, especificando os itens, endereço de entrega e informações do cliente.

## Cozinha:

- Como membro da equipe de cozinha, desejo confirmar o recebimento de pedidos para começar a preparação, ou recusá-los por algum motivo.
  - A equipe de cozinha deve receber notificações de pedidos pendentes.
  - Deve ser possível confirmar ou recusar pedidos pendentes. 

- Como membro da equipe de cozinha, desejo marcar pedidos como concluídos após a preparação.
  - Deve haver uma opção para a equipe de cozinha marcar pedidos como concluídos após a preparação. 

## Entregador:

- Como entregador, desejo receber notificações sobre os pedidos que devo entregar.
  - O entregador deve receber notificações em tempo real sobre os pedidos atribuídos a eles.
 
- Como entregador, desejo marcar os pedidos como entregues após a entrega bem-sucedida.
  - O entregador deve ter a opção de marcar pedidos como entregues após a entrega ser concluída com sucesso.

## Administrador:

- Como administrador, desejo cadastrar os perfis de funcionários (gerente, cozinha e entregador).
  - Deve haver uma interface de administração para cadastrar novos funcionários com informações relevantes.
  
- Como administrador, desejo acessar dados gerais e estatísticas sobre os pedidos e o desempenho do restaurante.
  - O administrador deve ter acesso a um painel com informações estatísticas sobre os pedidos, incluindo números de pedidos, tempo médio de preparação e de entrega, métricas financeiras, entre outros dados relevantes. 

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
