# Comandou

Plataforma web para gerenciamento de pedidos e atendimento em estabelecimentos.

**Domínio:** comandou.com.br

## Visão geral

O Comandou tem como objetivo integrar, em um único sistema, a experiência do cliente e a operação interna do estabelecimento.

Pelo tablet disponibilizado no local ou pelo próprio celular, o cliente poderá acessar a mesa, identificar as pessoas presentes, consultar o cardápio, realizar pedidos, solicitar atendimento e efetuar o pagamento.

Na área interna, funcionários poderão acompanhar pedidos, chamados e pagamentos, enquanto administradores terão acesso ao gerenciamento do estabelecimento.

Um dos diferenciais do Comandou está na organização individual do consumo dentro de uma mesma mesa. Cada pessoa é identificada temporariamente durante o atendimento, permitindo que os pedidos sejam associados a quem realizou o consumo. No momento do pagamento, a conta poderá ser paga integralmente por uma pessoa, dividida igualmente entre os participantes ou separada de acordo com o consumo individual de cada um. O sistema também permitirá pagamentos via Pix diretamente pela plataforma, com confirmação automática.

## Domínio e subdomínios

O sistema será disponibilizado por meio do domínio principal:

`comandou.com.br`

Cada estabelecimento poderá possuir seu próprio subdomínio dentro da plataforma, permitindo identificar e separar o acesso de cada empresa.

Exemplo:

`confeitaria.comandou.com.br`

Dessa forma, os estabelecimentos utilizarão a mesma plataforma e infraestrutura, mantendo seus dados e configurações vinculados individualmente dentro do Comandou.

## Funcionamento

O fluxo principal do sistema contempla:

1. Acesso à mesa;
2. Identificação das pessoas;
3. Consulta ao cardápio;
4. Realização do pedido;
5. Envio para a cozinha;
6. Atendimento de solicitações;
7. Divisão da conta;
8. Pagamento;
9. Encerramento da mesa.

O cliente não precisará criar uma conta para utilizar o sistema.

## Módulos

O projeto será dividido entre:

- Área do cliente;
- Gestão de pedidos;
- Cozinha;
- Atendimento;
- Pagamentos;
- Administração do estabelecimento.

## Protótipo

A interface e o fluxo principal do cliente foram desenvolvidos no Figma.

[Acessar protótipo no Figma](https://www.figma.com/design/JqXHUthiYVKXV4G9iT3Ngy/Untitled?node-id=0-1&t=MGgNXuyp3hqaSGFe-1)

## Tecnologias

### Front-end

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=plastic&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=plastic&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=plastic&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=plastic&logo=tailwindcss&logoColor=white)

### Back-end

![PHP](https://img.shields.io/badge/PHP-777BB4?style=plastic&logo=php&logoColor=white)
![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=plastic&logo=laravel&logoColor=white)

### Banco de dados

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=plastic&logo=mysql&logoColor=white)

### Desenvolvimento e prototipação

![Git](https://img.shields.io/badge/Git-F05032?style=plastic&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=plastic&logo=github&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=plastic&logo=figma&logoColor=white)

## Documentação do projeto

A documentação técnica do Comandou está organizada na pasta `docs`.

- [Estrutura do banco de dados](docs/database/estrutura-banco-dados.md)
- [Requisitos Funcionais](docs/requirements/requisitos-funcionais.md)
- [Requisitos Não Funcionais](docs/requirements/requisitos-nao-funcionais.md)
- [Diagrama de Casos de Uso](docs/diagrams/casos-de-uso.md)
- [Diagrama de Classes](docs/diagrams/classes.md)
- [Diagramas de Sequência](docs/diagrams/sequencia.md)
- [Fluxograma do sistema](docs/diagrams/fluxograma.md)
- [Diagrama de Estados](docs/diagrams/estados.md)
- [Diagrama de Componentes](docs/diagrams/componentes.md)
- [Roadmap do MVP](docs/roadmap/roadmap-mvp.md)

## Repositório

O repositório do projeto é mantido no GitHub, utilizando Git para o versionamento durante o desenvolvimento.

## Autora

**Nafitaly Vitória**

Análise e Desenvolvimento de Sistemas - FATEC Araraquara.

## Status

Em fase de planejamento e prototipação.
