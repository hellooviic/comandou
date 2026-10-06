# Requisitos Funcionais

Os requisitos funcionais descrevem as principais funcionalidades previstas para o Comandou.

## Gestão da plataforma

**RF01 - Gerenciar empresas**  
O sistema deve permitir o cadastro e gerenciamento dos estabelecimentos que utilizam a plataforma.

**RF02 - Autenticar funcionários**  
O sistema deve permitir que usuários internos realizem login para acessar as funcionalidades correspondentes ao seu perfil.

**RF03 - Gerenciar funcionários**  
O administrador deve poder cadastrar, editar e alterar o status dos funcionários do estabelecimento.

**RF04 - Controlar perfis de acesso**  
O sistema deve diferenciar os acessos de administrador, atendente, garçom e cozinha.

## Cardápio e mesas

**RF05 - Gerenciar categorias**  
O administrador deve poder cadastrar, editar e alterar o status das categorias do cardápio.

**RF06 - Gerenciar produtos**  
O administrador deve poder cadastrar e editar produtos, incluindo nome, descrição, preço, imagem, categoria e disponibilidade.

**RF07 - Gerenciar mesas**  
O estabelecimento deve poder cadastrar e gerenciar suas mesas.

**RF08 - Gerenciar sessões da mesa**  
O sistema deve permitir iniciar e encerrar uma sessão de atendimento vinculada a uma mesa.

## Experiência do cliente

**RF09 - Acessar a mesa**  
O cliente deve poder acessar a sessão da mesa pelo dispositivo disponibilizado pelo estabelecimento ou pelo próprio celular.

**RF10 - Identificar pessoas da mesa**  
O sistema deve permitir cadastrar nomes ou apelidos temporários das pessoas presentes na mesa, sem necessidade de criação de conta.

**RF11 - Consultar cardápio**  
O cliente deve poder visualizar categorias, produtos, descrições, preços e disponibilidade.

**RF12 - Realizar pedido**  
O cliente deve poder adicionar produtos ao pedido, informando quantidade e observações quando necessário.

**RF13 - Associar consumo à pessoa**  
O sistema deve permitir associar os itens pedidos à pessoa responsável pelo consumo.

**RF14 - Gerenciar pedido antes do envio**  
O cliente deve poder alterar quantidades ou remover itens enquanto o pedido ainda não tiver sido enviado para a cozinha.

## Pedidos e atendimento

**RF15 - Enviar pedido para a cozinha**  
O sistema deve encaminhar os pedidos confirmados para a área da cozinha.

**RF16 - Atualizar situação do pedido**  
A equipe deve poder atualizar o pedido de "Enviado para a cozinha" para "Entregue".

**RF17 - Solicitar atendimento**  
O cliente deve poder realizar chamados para solicitar atendimento na mesa.

**RF18 - Gerenciar chamados**  
A equipe deve poder visualizar e atualizar a situação dos chamados realizados pelas mesas.

## Pagamentos

**RF19 - Calcular a conta da mesa**  
O sistema deve calcular o valor total consumido durante a sessão da mesa.

**RF20 - Pagar a conta integralmente**  
O sistema deve permitir que o valor total da conta seja realizado em um único pagamento.

**RF21 - Dividir igualmente a conta**  
O sistema deve calcular a divisão igual do valor da conta entre as pessoas da mesa.

**RF22 - Pagar por consumo individual**  
O sistema deve permitir que cada pessoa pague os itens associados ao seu próprio consumo.

**RF23 - Disponibilizar formas de pagamento**  
O sistema deve permitir pagamentos por Pix, cartão ou dinheiro.

**RF24 - Processar pagamento via Pix**  
O sistema deve permitir o pagamento via Pix pela própria plataforma e registrar sua confirmação automaticamente após a aprovação pelo serviço de pagamento.

**RF25 - Registrar pagamentos presenciais**  
Funcionários autorizados devem poder registrar pagamentos realizados presencialmente por cartão ou dinheiro.

**RF26 - Controlar saldo restante**  
O sistema deve atualizar o valor restante da conta conforme os pagamentos forem realizados.

**RF27 - Encerrar a sessão da mesa**  
O sistema deve permitir o encerramento da sessão somente após a quitação total da conta.
