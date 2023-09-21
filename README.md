**Sistema de Delivery 🍔🚚**

   Projeto desenvolvido por Yan Tavares, Pedro Rêgo, Jordan Marques e Cristian Soares como parte da disciplina de Projeto de Engenharia de Software ofertada pela Universidade Federal do Rio Grande do Norte.

**Descrição do Projeto 📋**

   O Sistema de Delivery é uma plataforma que permite aos clientes realizar pedidos de comida de restaurantes locais. Além disso, fornece funcionalidades para gerentes, cozinheiros, entregadores e administradores, tornando a gestão do restaurante mais eficiente.

**Funcionalidades do Sistema 🚀**

**Ator 1: Cliente 👤**

      **Realizar cadastro**
      *Fluxo Normal:*
        - Cliente informa Nome
        - Cliente informa CPF
        - Cliente informa Número de contato
        - Cliente informa E-mail
        - Cliente informa Senha
        - Sistema cria o usuário
      - Extensões:
        - 2a. Se o CPF for inválido, solicitar novamente.
        - 5a. Se a senha for inferior a 6 caracteres, solicitar novamente.

      3.1.2. **Realizar login**
      - Fluxo Normal:
        - Cliente informa email
        - Cliente informa senha
        - Sistema realiza login
      - Extensões:
        - 1a. Se o e-mail for inválido, solicitar novamente.
        - 2a. Se a senha for inválida, solicitar novamente.

      3.1.3. **Realizar pedido**
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

      3.1.4. **Criar endereço**
      - Fluxo Normal:
        - Cliente informa CEP
        - Sistema valida o CEP
        - Sistema preenche informações com base no CEP preenchido
        - Cliente informa Número
        - Cliente informa Complemento (ex.: Bloco/Apto)
      - Extensões:
        - 2a. Se o CEP não for atendido, solicitar novamente
        - 3a. Se as informações não forem preenchidas, cliente informa manualmente

      3.1.5. **Acompanhar pedido**
      - Fluxo Normal:
        - Sistema exibe lista de pedidos
        - Cliente seleciona o pedido que deseja acompanhar
        - Sistema exibe informações detalhadas sobre o pedido

   3.2. **Ator 2: Gerente 👨‍💼**

      3.2.1. **Adicionar itens ao cardápio**
      - Fluxo Normal:
        - Gerente informa Nome do item
        - Gerente informa Descrição
        - Gerente informa Categoria
        - Gerente informa Preço
        - Gerente adiciona Foto
        - Sistema cria item

      3.2.2. **Alterar itens do cardápio**
      - Fluxo Normal:
        - Sistema exibe lista de itens
        - Gerente seleciona item que deseja alterar
        - Sistema exibe campos com atuais informações do item
        - Gerente edita os campos desejados
        - Sistema exibe confirmação
        - Gerente confirma alteração
        - Sistema atualiza o cardápio

      3.2.3. **Remover itens do cardápio**
      - Fluxo Normal:
        - Sistema exibe lista de itens do cardápio
        - Gerente seleciona os itens que deseja remover
        - Sistema exibe confirmação
        - Gerente confirma
        - Sistema atualiza o cardápio

      3.2.4. **Aceitar ou Recusar pedidos**
      - Fluxo Normal:
        - Sistema exibe lista de pedidos realizados
        - Gerente acessa detalhes do pedido
        - Gerente confirma ou não o pedido
      - Extensões:
        - 3a. Caso confirmado, Sistema envia pedido para cozinha
        - 3b. Caso negado, Gerente informa motivo, Sistema cancela e informa o cliente

      3.2.5. **Direcionar pedidos para entrega**
      - Fluxo Normal:
        - Sistema exibe para o gerente os pedidos finalizados pela cozinha
        - Gerente direciona pedido para entregador disponível
        - Sistema atualiza status do pedido para disponível para entrega

      3.2.6. **Alterar funcionamento da loja**
      - Fluxo Normal:
        - Gerente torna indisponível a efetuação de pedidos, ainda que dentro do horário de funcionamento, por motivos internos.

   3.3. **Ator 3: Cozinha 👨‍🍳**

      3.3.1. **Confirmar recebimento**
      - Fluxo Normal:
        - Sistema mostra pedidos a serem feitos
        - Cozinha confirma o recebimento do pedido
      - Extensões:
        - 2a. Caso cozinha não confirme, pedido volta para gerente

      3.3.2.
