# Estrutura Inicial do Banco de Dados

Este documento apresenta a estrutura inicial do banco de dados do Comandou.

A modelagem poderá sofrer alterações durante o desenvolvimento do sistema.

## empresas

Armazena os estabelecimentos cadastrados na plataforma.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| nome | VARCHAR(150) | |
| cnpj | VARCHAR(18) | |
| slug | VARCHAR(100) | |
| email | VARCHAR(150) | |
| telefone | VARCHAR(20) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## usuarios

Armazena os usuários internos de cada estabelecimento, como administradores, atendentes, garçons e equipe da cozinha.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| empresa_id | BIGINT | FK → empresas.id |
| nome | VARCHAR(150) | |
| email | VARCHAR(150) | |
| senha | VARCHAR(255) | |
| perfil | VARCHAR(30) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## mesas

Armazena as mesas pertencentes a cada estabelecimento.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| empresa_id | BIGINT | FK → empresas.id |
| numero | VARCHAR(20) | |
| codigo_acesso | VARCHAR(100) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## sessoes_mesa

Representa cada atendimento realizado em uma mesa.

Uma nova sessão é criada quando uma mesa inicia um atendimento e encerrada após a finalização da conta.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| mesa_id | BIGINT | FK → mesas.id |
| status | VARCHAR(20) | |
| aberta_em | TIMESTAMP | |
| encerrada_em | TIMESTAMP | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## pessoas_mesa

Armazena temporariamente as pessoas participantes de uma sessão.

Essas pessoas não possuem conta ou login na plataforma.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| sessao_mesa_id | BIGINT | FK → sessoes_mesa.id |
| nome | VARCHAR(100) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## categorias

Armazena as categorias utilizadas para organizar os produtos do cardápio.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| empresa_id | BIGINT | FK → empresas.id |
| nome | VARCHAR(100) | |
| descricao | VARCHAR(255) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## produtos

Armazena os produtos cadastrados por cada estabelecimento.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| empresa_id | BIGINT | FK → empresas.id |
| categoria_id | BIGINT | FK → categorias.id |
| nome | VARCHAR(150) | |
| descricao | TEXT | |
| preco | DECIMAL(10,2) | |
| imagem | VARCHAR(255) | |
| disponivel | BOOLEAN | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## pedidos

Armazena os pedidos realizados durante uma sessão da mesa.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| sessao_mesa_id | BIGINT | FK → sessoes_mesa.id |
| status | VARCHAR(30) | |
| enviado_em | TIMESTAMP | |
| entregue_em | TIMESTAMP | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## itens_pedido

Armazena os produtos pertencentes a cada pedido.

O item poderá ser associado a uma pessoa específica da mesa ou identificado como compartilhado.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| pedido_id | BIGINT | FK → pedidos.id |
| produto_id | BIGINT | FK → produtos.id |
| pessoa_mesa_id | BIGINT | FK → pessoas_mesa.id |
| tipo_consumo | VARCHAR(20) | |
| quantidade | INT | |
| preco_unitario | DECIMAL(10,2) | |
| observacao | VARCHAR(255) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## chamados

Registra solicitações de atendimento realizadas pela mesa.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| sessao_mesa_id | BIGINT | FK → sessoes_mesa.id |
| pessoa_mesa_id | BIGINT | FK → pessoas_mesa.id |
| usuario_atendente_id | BIGINT | FK → usuarios.id |
| tipo | VARCHAR(50) | |
| status | VARCHAR(20) | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## pagamentos

Registra os pagamentos realizados durante a sessão da mesa.

A estrutura permite pagamento único, pagamento por consumo individual ou divisão igual entre os participantes.

| Campo | Tipo | Chave |
|---|---|---|
| id | BIGINT | PK |
| sessao_mesa_id | BIGINT | FK → sessoes_mesa.id |
| pessoa_mesa_id | BIGINT | FK → pessoas_mesa.id |
| tipo_divisao | VARCHAR(30) | |
| forma_pagamento | VARCHAR(20) | |
| valor | DECIMAL(10,2) | |
| status | VARCHAR(20) | |
| referencia_externa | VARCHAR(255) | |
| pago_em | TIMESTAMP | |
| created_at | TIMESTAMP | |
| updated_at | TIMESTAMP | |

## Observações

- O sistema será multiempresa, mantendo os dados de cada estabelecimento separados.
- Clientes não precisarão criar uma conta para utilizar o sistema.
- As pessoas da mesa existirão somente durante a sessão de atendimento.
- Os itens poderão ser individuais ou compartilhados.
- Os pedidos enviados à cozinha seguirão o fluxo de `Enviado para a cozinha` até `Entregue`.
- A conta poderá ser paga de forma única, dividida igualmente ou separada pelo consumo de cada pessoa.
- Pagamentos via Pix poderão ser confirmados automaticamente por meio de integração com um serviço de pagamento.
