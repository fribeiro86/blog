---
title: "IP e Porta Lógica na Assinatura Eletrônica: Guia do Perito Judicial"
description: "Entenda por que o IP sozinho não prova autoria em assinatura eletrônica, o papel da porta lógica em ambiente CGNAT e o que diz o Art. 15-A do Decreto nº 12.975/2026."
date: 2026-05-21
draft: false
slug: "ip-e-porta-logica-na-assinatura-eletronica"
tags:
  - assinatura eletrônica
  - perícia digital
  - porta lógica
  - CGNAT
  - cadeia de custódia
  - Decreto 12.975/2026
categories:
  - Perícia Digital
author: "Fabricio do Nascimento Ribeiro"
keywords:
  - porta lógica
  - IP na perícia
  - assinatura eletrônica
  - CGNAT
  - cadeia de custódia digital
  - Decreto 12.975/2026
  - Art. 15-A
  - perito judicial
  - prova digital
  - REsp 1.777.769
image: "/images/ip-porta-logica-assinatura-eletronica.jpg"
---

Se você atua em processo que envolve **assinatura eletrônica digital**, provavelmente já se deparou com um log contendo um endereço IP. E, muito provavelmente, alguém tratou esse IP como se fosse prova de autoria.

**Não é.**

O IP identifica, na maioria dos casos, apenas a provedora de conexão dona daquele endereço. Ele não identifica a pessoa, não identifica o dispositivo e não identifica quem assinou.

Já a **porta lógica** — dado frequentemente ignorado — é o elemento que permite individualizar a conexão. É ela que possibilita à provedora localizar, em sua tabela NAT, qual usuário estava usando aquele IP naquele exato dia e horário.

<!--more-->

Neste guia, vou explicar:

- O que o IP realmente identifica (e o que ele não identifica);
- O que é a porta lógica e por que ela é indispensável em ambiente CGNAT;
- O que diz o Decreto nº 12.975/2026, Art. 15-A, sobre guarda de porta lógica;
- Quais falhas comprometem a prova digital;
- O que advogados devem exigir e o que peritos devem documentar.

## O que é IP na perícia de assinatura eletrônica

O **IP (Internet Protocol)** é o endereço lógico que identifica um ponto de conexão na internet. Em um log de assinatura eletrônica, o IP de origem indica por onde a conexão entrou na rede.

O problema é que, no Brasil, a maior parte das conexões residenciais e móveis opera atrás de **CGNAT (Carrier-Grade NAT)**. Isso significa que dezenas, centenas ou milhares de usuários compartilham o mesmo IP público simultaneamente.

**Consequência prática:** o IP, sozinho, não individualiza ninguém. Ele aponta para a provedora. Nada mais.

É por isso que laudos que afirmam *"o IP X assinou o documento"* partem de premissa tecnicamente equivocada.

## O que é porta lógica e por que ela é decisiva

A **porta lógica de origem** é o dado que, dentro da tabela NAT da provedora, permite saber qual usuário estava usando aquele IP naquele momento.

Quando um banco ou aplicação registra uma assinatura eletrônica, ele normalmente captura:

- IP de origem;
- Porta lógica de origem;
- Timestamp (data e hora);
- Protocolo.

Essa combinação — **IP + porta + horário** — é o que permite à provedora fazer a correlação inversa: *"neste horário, esta porta estava atribuída a este usuário"*.

Sem a porta lógica, em ambiente CGNAT, a provedora não consegue individualizar. Ela sabe qual IP foi usado, mas não sabe qual dos inúmeros usuários atrás daquele IP era o responsável pela conexão.

A porta lógica é o elemento que transforma um IP compartilhado em uma conexão individualizável.

## Decreto nº 12.975/2026, Art. 15-A: a obrigação de guardar a porta lógica

O **Decreto nº 12.975, de 20 de maio de 2026**, alterou o Decreto nº 8.771/2016 e incluiu o **Art. 15-A**, que trata especificamente da guarda de registros de conexão.

O texto estabelece que a obrigação de guarda de registros de IP — tanto para provedores de conexão quanto para provedores de aplicação — abrange a **porta lógica de origem**, sempre que esse dado for necessário para identificar de forma única o terminal de origem ou o próximo elo da rede.

Dois pontos merecem atenção:

1. **A guarda é prévia.** O parágrafo primeiro do Art. 15-A deixa claro que a obrigação é autônoma de cada provedor e independe de requisição judicial. O dado tem que estar lá antes de o juiz pedir. Não pode ser gerado depois.
2. **A norma consolida entendimento do STJ.** Desde 2019, no **REsp 1.777.769/SP**, e depois nos **REsp 1.784.156** e **REsp 2.170.872**, o Superior Tribunal de Justiça reconheceu que, enquanto não houver migração completa para IPv6, a porta lógica é indispensável para a identificação do usuário.

## O que a porta lógica prova — e o que ela não prova

Aqui está o ponto que separa o **laudo técnico rigoroso** do **laudo frágil**.

A porta lógica permite chegar até a conexão. Permite que a provedora localize o usuário titular daquele acesso. Permite responder: *"neste horário, esta conexão estava atribuída a esta pessoa"*.

Mas ela **não prova que foi essa pessoa quem assinou**. A conexão pode ter sido usada por:

- Um familiar;
- Um visitante;
- Alguém conectado ao mesmo Wi-Fi;
- Um dispositivo comprometido por malware.

Em outras palavras: **a porta lógica leva você até a casa. Não necessariamente até a pessoa que estava no computador naquele momento.**

Por isso, IP e porta lógica não são elementos decisivos. São elementos **incendiários**. Acendem o rastro, orientam a investigação, mas precisam ser correlacionados com outros artefatos:

- Logs de aplicação;
- Certificado digital;
- Autenticação em dois fatores;
- Geolocalização;
- Registros de dispositivo.

## Falhas comuns na análise de IP e porta lógica

### 1. Tratar IP como identidade
O IP identifica a provedora. Não a pessoa. Laudos que afirmam *"o IP X assinou o documento"* partem de premissa tecnicamente equivocada.

### 2. Ignorar a porta lógica
Em ambiente CGNAT, sem porta lógica, a individualização é impossível. Um log que só traz IP, sem porta, tem valor probatório drasticamente reduzido.

### 3. Não documentar a origem do dado
De onde veio esse IP? Quem capturou? Em que momento? Com qual ferramenta? Sem essa documentação, a cadeia de custódia digital já nasce comprometida.

### 4. Não verificar o fuso horário
A correlação entre porta lógica e usuário depende de precisão temporal. Um erro de fuso pode deslocar completamente a atribuição.

### 5. Confundir "conexão individualizada" com "autoria comprovada"
São coisas diferentes. A primeira é um passo técnico. A segunda exige um conjunto probatório bem mais amplo.

## Consequências da má gestão desses dados

Quando IP e porta lógica são mal documentados, mal interpretados ou simplesmente ignorados, a prova digital perde força. O juiz pode:

- Desconsiderar o laudo por falta de fundamento técnico;
- Desentranhar a prova dos autos;
- Absolver por insuficiência probatória.

O impacto pode ser decisivo. Uma prova que poderia esclarecer um contrato contestado, uma fraude bancária ou uma assinatura negada pode se tornar inútil se a porta lógica não foi preservada ou se o IP foi tratado como prova cabal de autoria.

## O papel do perito e do assistente técnico

O **perito** precisa documentar com rigor:

- Qual IP;
- Qual porta lógica;
- Qual horário;
- Qual fuso;
- Qual método de captura.

E precisa deixar claro, no laudo, a diferença entre **individualizar a conexão** e **atribuir autoria**.

O **assistente técnico** deve verificar:

- Se a porta lógica foi registrada no momento da coleta;
- Se o timestamp está em fuso consistente;
- Se a correlação IP + porta + horário foi feita com base em documentação da provedora;
- Se o laudo confunde conexão com pessoa.

Se o perito tratou IP como identidade, o assistente tem base para impugnar. Se a porta lógica não foi documentada, a individualização é frágil. Se o fuso horário não foi observado, a correlação pode estar deslocada.

## Recomendações práticas para advogados

1. **Peça a porta lógica.** Se o log trouxer apenas IP, questione. Em ambiente CGNAT, sem porta, não há individualização possível.
2. **Verifique o timestamp e o fuso.** A porta lógica só faz sentido se o horário estiver correto. Peça o registro completo, com fuso.
3. **Confirme a origem do dado.** Quem capturou? Quando? Com qual ferramenta? O dado foi gerado no momento da conexão ou reconstruído depois?
4. **Use o Art. 15-A do Decreto 12.975/2026 como fundamento.** Se a provedora alegar que não guardou a porta lógica, isso contraria obrigação normativa expressa. A guarda é prévia e independente de requisição judicial.
5. **Exija que o laudo diferencie conexão de autoria.** Se o perito afirmou que "o IP X assinou", isso é erro técnico. Aponte.
6. **Levante a questão na impugnação.** O momento estratégico para questionar a cadeia de custódia e a interpretação de IP/porta é na impugnação do laudo pericial.

## Perguntas frequentes (FAQ)

### O que é porta lógica na assinatura eletrônica?
É o dado que, dentro da tabela NAT da provedora, permite identificar qual usuário estava usando determinado IP naquele momento. Sem ela, em ambiente CGNAT, não há individualização da conexão.

### O IP sozinho prova quem assinou um documento?
Não. O IP identifica, na maioria dos casos, apenas a provedora de conexão. Ele não identifica a pessoa, o dispositivo ou o autor da assinatura.

### O que diz o Decreto nº 12.975/2026 sobre porta lógica?
O Art. 15-A inclui a porta lógica de origem na obrigação de guarda de registros de IP, tanto para provedores de conexão quanto de aplicação. A guarda é prévia e independe de requisição judicial.

### Qual a diferença entre cadeia de custódia física e digital?
Na física, a evidência é material e a alteração exige ação física. Na digital, a evidência é imaterial e volátil — um arquivo pode ser alterado ou deletado sem deixar vestígios aparentes. Por isso exige métodos técnicos como o hash.

### O que é hash e por que ele é importante?
O hash é uma função matemática que gera um código único para cada arquivo. Qualquer alteração faz o hash mudar completamente. Se o hash recalculado bate com o original, a prova é íntegra. Se não bate, a prova foi alterada.

## Conclusão

**IP e porta lógica não são prova de autoria. São elementos de localização.**

O IP aponta para a provedora. A porta lógica individualiza a conexão dentro daquela provedora. Juntos, permitem chegar até o usuário titular da conexão.

Mas chegar até o usuário não é o mesmo que provar que ele assinou. **A porta lógica leva você até a casa. Quem estava lá dentro, naquele momento, usando aquele dispositivo — isso exige outros artefatos, outras correlações, outras provas.**

O Decreto nº 12.975/2026, ao incluir o Art. 15-A, reforçou a importância da porta lógica como elemento de individualização. Mas também reforçou a necessidade de rigor: a guarda é prévia, a correlação depende de precisão temporal, e a interpretação exige cautela.

Para o **perito**, a mensagem é clara: documente IP, porta, horário e fuso. E nunca trate indício como certeza.

Para o **advogado**, a mensagem é igualmente clara: se o log não tem porta lógica, pergunte por quê. Se o laudo confunde conexão com autoria, impugne. Porque no processo, o que vale não é o dado bruto — é o que se consegue demonstrar com ele.

---

**Precisa verificar a cadeia de custódia de uma assinatura eletrônica?**

Se o seu processo envolve assinatura eletrônica digital e você precisa auditar a cadeia de custódia, a guarda de IP e porta lógica, ou a validade técnica de um laudo pericial, posso ajudar.

👉 **[Solicitar diagnóstico de viabilidade](http://peritofabricioribeiro.com.br/)**