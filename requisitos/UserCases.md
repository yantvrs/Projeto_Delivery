
# Casos de uso

- Diagrama de Casos de Uso

<div align="center">
  
![Diagrama de Casos de Uso para o sistema delivery](https://github.com/yantvrs/Projeto_Delivery/blob/main/images/UseCaseDiagram%20-%20Delivery.png)

</div>




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
  - 3a. Se não houver endereço cadastrado, cliente _cria endereço_.
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
  - 4a. Caso negado, Sistema volta para lista de funcionários
