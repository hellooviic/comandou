# Requisitos Não Funcionais

Os requisitos não funcionais definem características de qualidade, segurança, desempenho e restrições técnicas previstas para o Comandou.

## Usabilidade e interface

**RNF01 - Responsividade**  
O sistema deve possuir interface responsiva, adaptando-se a diferentes tamanhos de tela, incluindo computadores, tablets e smartphones.

**RNF02 - Usabilidade**  
A interface deve ser simples e intuitiva, permitindo que clientes e funcionários utilizem as principais funcionalidades com facilidade.

## Segurança

**RNF03 - Isolamento dos dados das empresas**  
O sistema deve garantir que os dados de cada empresa sejam acessados somente por usuários autorizados pertencentes ao respectivo estabelecimento.

**RNF04 - Controle de acesso**  
As funcionalidades internas devem ser disponibilizadas de acordo com o perfil do funcionário autenticado.

**RNF05 - Proteção de credenciais**  
As senhas dos usuários internos devem ser armazenadas de forma segura, utilizando mecanismos de hash.

**RNF06 - Segurança nos pagamentos**  
As operações de pagamento realizadas pela plataforma devem utilizar comunicação segura e integração com serviços de pagamento apropriados.

## Desempenho e confiabilidade

**RNF07 - Desempenho**  
O sistema deve apresentar tempo de resposta adequado durante consultas ao cardápio, realização de pedidos, chamados e operações de pagamento.

**RNF08 - Integridade dos dados**  
O sistema deve preservar a consistência das informações relacionadas a empresas, mesas, sessões, pedidos, pessoas da mesa e pagamentos.

## Compatibilidade

**RNF09 - Compatibilidade com navegadores**  
A aplicação deve funcionar nos principais navegadores modernos utilizados em computadores, tablets e smartphones.

**RNF10 - Aplicação web**  
O Comandou deve ser desenvolvido como uma aplicação web, permitindo seu acesso por navegador sem necessidade de instalação de um aplicativo nativo.

## Tecnologias

**RNF11 - Tecnologias de desenvolvimento**  
O sistema deverá utilizar HTML5, CSS3, JavaScript e Tailwind CSS no front-end, PHP com Laravel no back-end e MySQL para armazenamento dos dados.

**RNF12 - Versionamento**  
O projeto deve utilizar Git para controle de versão e GitHub para armazenamento e organização do repositório.
