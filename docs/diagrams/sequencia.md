# Diagramas de Sequência

Os diagramas de sequência apresentam, de forma resumida, a ordem das interações entre os principais participantes do Comandou.

## Realização de pedido

```mermaid
sequenceDiagram
    actor Cliente
    participant Sistema
    participant Banco

    Cliente->>Sistema: Acessa o cardápio
    Sistema->>Banco: Consulta produtos disponíveis
    Banco-->>Sistema: Retorna produtos
    Sistema-->>Cliente: Exibe cardápio

    Cliente->>Sistema: Adiciona produtos ao pedido
    Cliente->>Sistema: Confirma envio do pedido
    Sistema->>Banco: Registra pedido e itens
    Banco-->>Sistema: Confirma registro
    Sistema-->>Cliente: Informa pedido enviado
```

## Envio e atualização do pedido na cozinha

```mermaid
sequenceDiagram
    actor Cliente
    participant Sistema
    actor Cozinha
    participant Banco

    Cliente->>Sistema: Confirma pedido
    Sistema->>Banco: Salva pedido com status "Enviado para a cozinha"
    Sistema-->>Cozinha: Disponibiliza novo pedido

    Cozinha->>Sistema: Visualiza pedido
    Cozinha->>Sistema: Marca pedido como entregue
    Sistema->>Banco: Atualiza status para "Entregue"
    Banco-->>Sistema: Confirma atualização
```

## Solicitação de atendimento

```mermaid
sequenceDiagram
    actor Cliente
    participant Sistema
    actor Equipe
    participant Banco

    Cliente->>Sistema: Solicita atendimento
    Sistema->>Banco: Registra chamado
    Sistema-->>Equipe: Disponibiliza chamado

    Equipe->>Sistema: Visualiza chamado
    Equipe->>Sistema: Marca chamado como atendido
    Sistema->>Banco: Atualiza status do chamado
```

## Pagamento via Pix

```mermaid
sequenceDiagram
    actor Cliente
    participant Sistema
    participant Pagamento
    participant Banco

    Cliente->>Sistema: Escolhe forma de divisão
    Sistema-->>Cliente: Exibe valor correspondente

    Cliente->>Sistema: Seleciona Pix
    Sistema->>Pagamento: Solicita geração do pagamento
    Pagamento-->>Sistema: Retorna dados do Pix
    Sistema-->>Cliente: Exibe QR Code e código Pix

    Cliente->>Pagamento: Realiza pagamento
    Pagamento-->>Sistema: Confirma pagamento

    Sistema->>Banco: Registra pagamento confirmado
    Sistema->>Banco: Atualiza saldo da mesa
    Sistema-->>Cliente: Informa pagamento confirmado
```

## Pagamento presencial

```mermaid
sequenceDiagram
    actor Cliente
    participant Sistema
    actor Equipe
    participant Banco

    Cliente->>Sistema: Seleciona cartão ou dinheiro
    Sistema-->>Cliente: Informa pagamento presencial

    Cliente->>Equipe: Realiza pagamento
    Equipe->>Sistema: Registra pagamento realizado
    Sistema->>Banco: Salva pagamento
    Sistema->>Banco: Atualiza saldo da mesa
    Sistema-->>Equipe: Confirma registro
```
