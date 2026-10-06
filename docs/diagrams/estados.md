# Diagrama de Estados

Os diagramas abaixo representam as principais mudanças de estado previstas no Comandou.

## Estado do pedido

```mermaid
%%{init: {
  "theme": "base",
  "flowchart": {
    "htmlLabels": true,
    "padding": 28,
    "nodeSpacing": 55,
    "rankSpacing": 65,
    "useMaxWidth": false
  },
  "themeVariables": {
    "background": "#ffffff",
    "primaryColor": "#ffffff",
    "primaryTextColor": "#000000",
    "primaryBorderColor": "#000000",
    "lineColor": "#333333",
    "fontSize": "17px"
  }
}}%%

flowchart LR

subgraph DIAGRAMA[" "]
direction LR

    INICIO([Início])
    ENVIADO["Enviado para<br/>a cozinha"]
    ENTREGUE["Entregue"]
    FIM([Fim])

    INICIO --> ENVIADO
    ENVIADO --> ENTREGUE
    ENTREGUE --> FIM

end

classDef estado fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;
classDef iniciofim fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;

class ENVIADO,ENTREGUE estado;
class INICIO,FIM iniciofim;

style DIAGRAMA fill:#ffffff,stroke:#ffffff,color:#000000

linkStyle default stroke:#333333,stroke-width:2px;
```

## Estado do pagamento

```mermaid
%%{init: {
  "theme": "base",
  "flowchart": {
    "htmlLabels": true,
    "padding": 28,
    "nodeSpacing": 55,
    "rankSpacing": 65,
    "useMaxWidth": false
  },
  "themeVariables": {
    "background": "#ffffff",
    "primaryColor": "#ffffff",
    "primaryTextColor": "#000000",
    "primaryBorderColor": "#000000",
    "lineColor": "#333333",
    "fontSize": "17px"
  }
}}%%

flowchart LR

subgraph DIAGRAMA[" "]
direction LR

    INICIO([Início])
    PENDENTE["Pendente"]
    CONFIRMADO["Confirmado"]
    CANCELADO["Cancelado"]
    FIM([Fim])

    INICIO --> PENDENTE
    PENDENTE --> CONFIRMADO
    PENDENTE --> CANCELADO
    CONFIRMADO --> FIM
    CANCELADO --> FIM

end

classDef estado fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;
classDef iniciofim fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;

class PENDENTE,CONFIRMADO,CANCELADO estado;
class INICIO,FIM iniciofim;

style DIAGRAMA fill:#ffffff,stroke:#ffffff,color:#000000

linkStyle default stroke:#333333,stroke-width:2px;
```

## Estado da sessão da mesa

```mermaid
%%{init: {
  "theme": "base",
  "flowchart": {
    "htmlLabels": true,
    "padding": 32,
    "nodeSpacing": 60,
    "rankSpacing": 70,
    "useMaxWidth": false
  },
  "themeVariables": {
    "background": "#ffffff",
    "primaryColor": "#ffffff",
    "primaryTextColor": "#000000",
    "primaryBorderColor": "#000000",
    "lineColor": "#333333",
    "fontSize": "17px"
  }
}}%%

flowchart LR

subgraph DIAGRAMA[" "]
direction LR

    INICIO([Início])
    ABERTA["Aberta"]
    AGUARDANDO["Aguardando<br/>quitação<br/>da conta"]
    ENCERRADA["Encerrada"]
    FIM([Fim])

    INICIO --> ABERTA
    ABERTA --> AGUARDANDO
    AGUARDANDO --> ENCERRADA
    ENCERRADA --> FIM

end

classDef estado fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;
classDef iniciofim fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;

class ABERTA,AGUARDANDO,ENCERRADA estado;
class INICIO,FIM iniciofim;

style DIAGRAMA fill:#ffffff,stroke:#ffffff,color:#000000

linkStyle default stroke:#333333,stroke-width:2px;
```

## Estado do chamado

```mermaid
%%{init: {
  "theme": "base",
  "flowchart": {
    "htmlLabels": true,
    "padding": 28,
    "nodeSpacing": 55,
    "rankSpacing": 65,
    "useMaxWidth": false
  },
  "themeVariables": {
    "background": "#ffffff",
    "primaryColor": "#ffffff",
    "primaryTextColor": "#000000",
    "primaryBorderColor": "#000000",
    "lineColor": "#333333",
    "fontSize": "17px"
  }
}}%%

flowchart LR

subgraph DIAGRAMA[" "]
direction LR

    INICIO([Início])
    ABERTO["Aberto"]
    EMATENDIMENTO["Em atendimento"]
    ATENDIDO["Atendido"]
    FIM([Fim])

    INICIO --> ABERTO
    ABERTO --> EMATENDIMENTO
    EMATENDIMENTO --> ATENDIDO
    ATENDIDO --> FIM

end

classDef estado fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;
classDef iniciofim fill:#ffffff,stroke:#000000,color:#000000,stroke-width:1.5px,font-size:17px;

class ABERTO,EMATENDIMENTO,ATENDIDO estado;
class INICIO,FIM iniciofim;

style DIAGRAMA fill:#ffffff,stroke:#ffffff,color:#000000

linkStyle default stroke:#333333,stroke-width:2px;
```
