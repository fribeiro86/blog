---
title: "O que é Impugnar um Laudo Pericial? Guia Completo para Advogados"
date: 2026-09-28
draft: false
author: "Fabricio do Nascimento Ribeiro"
description: "Entenda o que é impugnar um laudo pericial, o prazo de 15 dias do Art. 477 do CPC, e como funciona a impugnação de laudos de assinatura digital."
tags: ["impugnação de laudo", "laudo pericial", "assinatura digital", "computação forense", "assistente técnico"]
categories: ["Computação Forense"]
ShowToc: true
TocOpen: false
ShowReadingTime: true
ShowShareButtons: true
---

Impugnar um laudo pericial não é dizer "juiz, não concordo". É analisar tecnicamente, ponto a ponto, as limitações do laudo. É um trabalho minucioso — e, na maioria das vezes, mal feito.

Neste artigo, vou explicar o que é impugnar um laudo pericial, qual é o prazo legal, quando faz sentido impugnar (e quando não faz), e como funciona a impugnação de laudos que envolvem assinaturas digitais.

## O que é impugnar um laudo pericial?

Impugnar é apontar falhas, defeitos e limitações do laudo. Pode ser usado tanto pela parte autora quanto pela parte ré — desde que o resultado seja desfavorável a quem impugna.

**Impugnar não é desqualificar o perito.** Não é dizer "o laudo não presta porque o perito é ruim". É ser honesto e admitir quando o perito declarou algo de forma técnica e robusta — e apontar, com fundamento, apenas onde ele falhou.

### Impugnar vs. contestar

Contestar é rebater uma acusação feita contra alguém. Impugnar é apontar falhas em um documento técnico. A impugnação pode ser usada por qualquer das partes — não é exclusividade do réu.

## O prazo de 15 dias e o Art. 477 do CPC

O **Art. 477 do CPC** é a base legal principal da impugnação.

Após a entrega do laudo, o juiz concede às partes **15 dias** para se manifestarem. Nesse prazo, o advogado pode apresentar sua impugnação e o assistente técnico pode juntar seu parecer.

Depois desse prazo, o perito do juízo tem **mais 15 dias** para esclarecer os pontos controvertidos, conforme o § 2º do Art. 477:

> "O perito do juízo tem o dever de, no prazo de 15 (quinze) dias, esclarecer ponto: I - sobre o qual exista divergência ou dúvida de qualquer das partes, do juiz ou do órgão do Ministério Público; II - divergente apresentado no parecer do assistente técnico da parte."

### O perito é obrigado a responder?

Sim. O perito tem o **dever legal** de responder aos pontos controvertidos. Ele não pode se esquivar com respostas genéricas. Precisa justificar sua metodologia perante o magistrado.

## Quando faz sentido impugnar (e quando não faz)

**Faz sentido impugnar quando:**
- O laudo apresenta falhas técnicas identificáveis
- Há contradições entre a fundamentação e a conclusão
- A [cadeia de custódia digital](/posts/cadeia-de-custodia-digital/). foi comprometida
- O método de análise não segue as normas técnicas

**NÃO faz sentido impugnar quando:**
- O laudo é robusto e bem fundamentado
- Não há falha técnica identificável
- A impugnação seria apenas retórica, sem base científica

A maioria dos laudos na área digital **não é robusta**. Há muitos equívocos — talvez porque essa área é relativamente nova no Brasil. Mas isso não significa que todo laudo deva ser impugnado. O assistente técnico precisa avaliar, com honestidade, se vale a pena.

## Impugnação de laudo de assinatura digital

Quando o laudo trata de **assinatura digital**, a impugnação ganha contornos específicos. É aqui que mora a maior parte das falhas que vejo na prática.

### Validade criptográfica vs. validade probatória

Uma assinatura digital pode ser **criptograficamente válida** e, ao mesmo tempo, **probatoriamente frágil**.

- **Validade criptográfica** é a validade matemática. O certificado está no prazo? A cadeia de certificação está íntegra? O hash confere? O carimbo de tempo é autêntico?
- **Validade probatória** é a validade jurídica. Quem assinou? Quando? Como? O titular do certificado estava presente? A [cadeia de custódia digital](/posts/cadeia-de-custodia-digital/). foi respeitada?

É exatamente aí que mora a brecha. Um laudo pode afirmar "a assinatura é válida" com base apenas na validade criptográfica — e ignorar completamente a validade probatória.

### Os pontos frágeis mais comuns

**1. Ausência de liveness (prova de vida)**

Prova de vida é a verificação de que a pessoa estava **presente** no momento da contratação. Pode ser ativa (a pessoa grava um vídeo em tempo real) ou passiva (o sistema verifica a presença de forma automática). Sem isso, não há como garantir que quem assinou era quem dizia ser.

**2. Ausência de biometria**

A biometria vincula a assinatura a uma característica física da pessoa. Sem ela, a assinatura prova apenas que alguém com acesso ao certificado assinou — não necessariamente o titular.

**3. PDF como relatório gerencial**

Muitos laudos usam PDFs que são "recortes de logs". O problema: o log completo precisa ser apresentado desde o começo da interação entre usuário e servidor até o fim. Um PDF recortado perde contexto, perde metadados e não permite verificar erros, aceites e rejeições.

**4. Ausência de logs brutos**

Logs brutos são os dados registrados pelo servidor enquanto o usuário está conectado. Todas as ações — do servidor e do usuário — são registradas. Eles permitem verificar conexão, horário, sessão, dispositivo. Sozinhos, não provam nada. Mas são um artefato poderoso e direto da fonte.

**5. Impossibilidade de vincular dispositivo e dados telemáticos ao usuário**

Se o laudo não consegue vincular o IP, o dispositivo e os dados telemáticos ao usuário, a prova perde força. Geolocalização por IP, por exemplo, tem precisão aproximada e não é suficiente, isoladamente, para atestar a localização exata.

## O papel do assistente técnico

O assistente técnico é o **braço técnico do advogado**. Ele não substitui o advogado — ele abastece o advogado com dados técnicos para que a impugnação seja elaborada de forma estratégica.

**O que o assistente técnico faz:**
- Audita o laudo ponto a ponto
- Identifica falhas metodológicas
- Verifica a cadeia de custódia
- Aponta contradições entre fundamentação e conclusão
- Elabora quesitos complementares
- Produz o parecer técnico que fundamenta a impugnação

**A diferença entre perito do juízo e assistente técnico:**

| Perito do juízo | Assistente técnico |
|-----------------|-------------------|
| Nomeado pelo juiz | Contratado pela parte |
| Deve ser neutro e imparcial | Defende tecnicamente a parte |
| Analisa a validade criptográfica | Analisa a validade probatória e a metodologia |
| Tem fé pública | Tem valor técnico, mas não fé pública |

O assistente técnico não é obrigado a aceitar o caso. A relação é privada, contratada diretamente pela parte.

## O que acontece depois da impugnação

Depois que a impugnação é protocolada:
1. O perito é **intimado a responder** os pontos controvertidos
2. Ele tem **15 dias** para prestar esclarecimentos
3. Se persistirem dúvidas, o juiz pode marcar **audiência de instrução**
4. O juiz decide

**O juiz não é obrigado a acolher a impugnação.** Ele pode ignorá-la, assim como pode ignorar o laudo do perito. O laudo e o parecer são apenas provas que podem abastecer o convencimento do juiz.

Mas uma impugnação bem-feita pode mudar o curso do processo — e dar a vitória a quem estava perdendo.

## Quando NÃO impugnar

Impugnar sem fundamento técnico é pior do que não impugnar. O advogado que apresenta uma impugnação genérica dá ao juiz um motivo para homologar o laudo integralmente por falta de contraprova consistente.

**Não impugne se:**
- O laudo é robusto
- Não há falha técnica identificável
- A impugnação seria apenas retórica

Antes de impugnar, procure um assistente técnico. Ele vai dizer, com honestidade, se vale a pena.

## Perguntas Frequentes

### O que é impugnar um laudo pericial?

Impugnar um laudo pericial é analisar tecnicamente, ponto a ponto, as limitações do laudo. Não é dizer "não concordo" — é apontar falhas metodológicas, contradições e vulnerabilidades com fundamento técnico.

### Qual é o prazo para impugnar um laudo pericial?

O prazo é de 15 dias contados da juntada do laudo aos autos, conforme o Art. 477, § 1º, do CPC. Nesse prazo, as partes podem apresentar sua manifestação e o assistente técnico pode juntar seu parecer.

### O que acontece se o prazo passar?

Após o prazo, o perito do juízo tem mais 15 dias para responder aos pontos controvertidos. Se o prazo para manifestação das partes passar sem impugnação, a parte pode perder a oportunidade de questionar o laudo naquela fase processual.

### O perito é obrigado a responder à impugnação?

Sim. O Art. 477, § 2º, do CPC estabelece que o perito do juízo tem o dever de esclarecer pontos sobre os quais exista divergência ou dúvida, inclusive os apresentados no parecer do assistente técnico.

### O que é um laudo de assinatura digital?

É um laudo pericial que analisa a validade de uma assinatura eletrônica. Pode envolver verificação de certificado digital, cadeia de certificação, carimbo de tempo, hash e outros elementos técnicos.

### Qual a diferença entre validade criptográfica e validade probatória?

Validade criptográfica é a validade matemática da assinatura (certificado no prazo, cadeia íntegra, hash confere). Validade probatória é a validade jurídica (quem assinou, quando, como, se o titular estava presente). Uma assinatura pode ser criptograficamente válida e, ao mesmo tempo, probatoriamente frágil.

### O que é um assistente técnico e qual o seu papel?

O assistente técnico é o braço técnico do advogado. Ele audita o laudo, identifica falhas, verifica a cadeia de custódia e produz o parecer técnico que fundamenta a impugnação. Ele é contratado pela parte, não é nomeado pelo juiz.

### O juiz é obrigado a acolher a impugnação?

Não. O juiz pode acolher ou ignorar a impugnação. O laudo e o parecer são apenas provas que podem abastecer o convencimento do magistrado. Mas uma impugnação bem-feita pode mudar o curso do processo.

### Quando NÃO faz sentido impugnar um laudo?

Quando o laudo é robusto e bem fundamentado, quando não há falha técnica identificável, ou quando a impugnação seria apenas retórica. Impugnar sem fundamento técnico é pior do que não impugnar.

### Como saber se vale a pena impugnar?

O ideal é contratar um assistente técnico especializado para auditar o laudo. Ele vai avaliar, com honestidade, se há fundamento técnico para a impugnação.


## Conclusão

Impugnar um laudo pericial é um trabalho técnico, minucioso e estratégico. Não é uma petição genérica. É uma contraposição científica que exige conhecimento específico.

Na área de assinaturas digitais, as falhas são frequentes — mas só um olhar forense treinado consegue identificá-las. Se você recebeu um laudo desfavorável e precisa avaliar se há espaço para impugnação, estou à disposição.

---



**Precisa avaliar se um laudo de assinatura digital pode ser impugnado?**

[Solicitar diagnóstico de viabilidade →](https://peritofabricioribeiro.com.br)