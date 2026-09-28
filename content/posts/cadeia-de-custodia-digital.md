---
title: "Cadeia de Custódia Digital: O que é e Por que é Decisiva em Processos Judiciais"
date: 2026-09-27
draft: false
author: "Fabricio do Nascimento Ribeiro"
description: "Entenda o que é cadeia de custódia digital, como a ISO/IEC 27037 e o Art. 158-A do CPP a regulam, e por que falhas na preservação de evidências digitais podem anular provas em processos judiciais."
tags: ["cadeia de custódia", "prova digital", "computação forense", "ICP-Brasil", "assistência técnica"]
categories: ["Computação Forense"]
ShowToc: true
TocOpen: false
ShowReadingTime: true
ShowShareButtons: true
---

A cadeia de custódia digital é o conjunto de procedimentos que garante que uma evidência digital — um arquivo, um log, uma assinatura eletrônica — permaneça **exatamente igual** desde o momento em que foi coletada até o momento em que é analisada em juízo.

Parece simples. Mas não é.

A evidência digital é frágil por natureza. Um arquivo pode ser deletado, alterado ou modificado em segundos. Um log pode ser editado. Uma assinatura eletrônica pode ser questionada quanto à sua origem. E quando isso acontece sem o devido registro, a prova perde valor.

Neste artigo, vou explicar o que é a cadeia de custódia digital, como ela é regulada no Brasil, quais são as falhas mais comuns que comprometem provas digitais e o que advogados precisam saber para questioná-la tecnicamente.

## O que é Cadeia de Custódia Digital?

De acordo com a **ISO/IEC 27037** — norma internacional que estabelece diretrizes para identificação, coleta, aquisição e preservação de evidências digitais —, a cadeia de custódia é o procedimento que garante a integridade da prova digital desde a sua origem.

A norma é clara ao afirmar que a evidência digital é relevante quando se destina a provar ou refutar um elemento de um caso específico. E o princípio fundamental é: **garantir que a evidência digital seja o que pretende ser**.

No Brasil, a definição legal está no **Art. 158-A do Código de Processo Penal (CPP)**, incluído pela Lei 13.964/2019 (Pacote Anticrime). O artigo define a cadeia de custódia como:

> "O conjunto de procedimentos utilizados para rastrear, manter e documentar a história cronológica da evidência, desde o momento de sua coleta até o seu descarte."

A lei é genérica — vale para qualquer tipo de prova, não apenas digital. Mas é o arcabouço legal que sustenta a necessidade de documentação rigorosa.

### A diferença entre cadeia de custódia física e digital

Na cadeia de custódia física (documentos em papel, objetos, amostras), a evidência é material. Ela pode ser apreendida, lacrada, guardada em local seguro. A alteração exige ação física.

Na cadeia de custódia digital, a evidência é **imaterial e volátil**. Um arquivo pode ser copiado, alterado ou deletado sem deixar vestígios aparentes. Por isso, a preservação da integridade digital exige **métodos técnicos específicos**, como o hash — sobre o qual falarei mais adiante.

## As 4 Fases da Cadeia de Custódia Digital

A ISO/IEC 27037 define quatro fases principais para o tratamento de evidências digitais. Na prática, elas funcionam assim:

### 1. Identificação

É o momento de reconhecer quais evidências são relevantes para o caso. Nem tudo que está no dispositivo interessa. O responsável pela coleta precisa saber o que procurar, onde procurar e por quê.

### 2. Coleta

Aqui, a evidência é isolada e armazenada de forma controlada. Depende do que está sendo coletado: um celular, um HD, um arquivo em nuvem, um log de servidor. Cada tipo de evidência exige um procedimento diferente.

### 3. Aquisição

A evidência é copiada para um ambiente controlado, onde será analisada. O ideal é que essa cópia seja feita em um ambiente **offline**, sem acesso à internet, para evitar contaminação ou alteração externa.

### 4. Preservação

A evidência é mantida em local seguro, com acesso restrito e documentado. Qualquer acesso precisa ser registrado. A preservação garante que a prova permaneça íntegra até o momento da análise.

## O Papel do Hash na Integridade da Prova

Se eu pudesse resumir a cadeia de custódia digital em uma única palavra, seria: **hash**.

O hash é uma função matemática que gera um código único para cada arquivo. É como se fosse a **certidão de nascimento digital** do documento. Qualquer alteração — um ponto, uma vírgula, um bit — faz com que o hash mude completamente.

Na prática, funciona assim:

1. A evidência é coletada e o hash é gerado.
2. Esse hash é registrado e documentado.
3. Antes da análise, o hash é recalculado.
4. Se o hash bater, a prova é íntegra.
5. Se o hash não bater, a prova foi alterada — e a cadeia de custódia está comprometida.

### Um exemplo prático

No meu trabalho com auditoria de assinaturas eletrônicas, eu faço a coleta através de um portal controlado. Cada arquivo recebe um hash no momento do upload. Eu registro o IP do advogado, o número da OAB, o nome completo, e pergunto de onde os documentos foram extraídos. Essa documentação é a base da cadeia de custódia.

Depois, mantenho os arquivos em pasta privada com acesso restrito. Faço uma cópia para uma máquina virtual sem acesso à internet e só então inicio a análise. Ao final, emito o laudo e descarto tudo com um protocolo de wipe — que gera um registro de que os setores do HD onde a prova estava foram devidamente apagados.

## Falhas Comuns na Cadeia de Custódia Digital

Na prática forense, vejo erros que comprometem a validade da prova digital com frequência. Os mais comuns são:

### 1. Recebimento de prova por email

Peritos que aceitam documentos por email, sem questionar a origem, sem documentar o método de coleta, sem gerar hash no momento do recebimento. Essa prova, na minha opinião, deveria ser anulada. Não há como garantir que o arquivo que chegou por email é o mesmo que saiu da fonte original.

### 2. Falta de documentação da origem

Não se pergunta de onde veio a prova. Não se documenta quem enviou, quando, como, por qual meio. Sem essa informação, não há como rastrear a cadeia.

### 3. Ausência de hash

Se o hash não foi gerado no momento da coleta e recalculado antes da análise, não há como provar que a evidência é íntegra.

### 4. Falta de "prova de vida"

Em casos que envolvem celulares, por exemplo, não se consegue vincular o aparelho ao seu dono. O IP não é vinculado à pessoa. A geolocalização pode ser implantada. Sem esses vínculos, a prova perde força.

### 5. Logs incompletos

Se os logs de acesso à prova não estão completos, não há como saber quem acessou, quando e por quê.

## Consequências da Quebra da Cadeia de Custódia

Quando a cadeia de custódia é comprometida, a prova digital pode ser:

- **Anulada** — o juiz pode determinar que a prova não seja considerada na decisão.
- **Desentranhada dos autos** — a prova é removida do processo.
- **Desconsiderada** — o juiz pode simplesmente ignorá-la por falta de confiabilidade.

O impacto no resultado do processo pode ser decisivo. Uma prova que poderia condenar ou absolver pode perder completamente o valor se a cadeia de custódia não for respeitada.

## O Papel do Perito e do Assistente Técnico

**O perito judicial** tem a função de preservar a prova. Ele é o responsável por garantir que a evidência coletada permaneça íntegra durante todo o processo de análise. Isso inclui documentar a origem, gerar hash, manter o ambiente controlado e registrar todos os acessos.

**O assistente técnico** fiscaliza as atividades do perito. Ele verifica se o perito documentou a origem da prova, se gerou hash, se recalculou o hash antes da análise, se manteve a prova em ambiente íntegro. Se o perito falhou em algum desses pontos, o assistente técnico tem base para questionar a validade da prova.

Na minha atuação como perito credenciado pelo TJSC, já vi casos em que a falha na cadeia de custódia foi evidente — mas passou despercebida porque ninguém questionou. A maioria dos advogados não sabe o que é cadeia de custódia. Não pergunta. Não fiscaliza. E o perito, muitas vezes, também não documenta.

## Recomendações Práticas para Advogados

Se você é advogado e precisa questionar a cadeia de custódia de uma prova digital, aqui está o que fazer:

### 1. Verifique a documentação da coleta

Pergunte: quem coletou? Quando? Onde? Como? Com qual ferramenta? Se não houver resposta documentada, a cadeia já está comprometida.

### 2. Exija o hash

O hash do arquivo original deve estar documentado. E o hash do arquivo analisado deve ser recalculado e comparado. Se não bater, a prova foi alterada.

### 3. Peça os logs de acesso

Quem acessou a prova? Quando? Por quê? Se não houver registro, não há como garantir a integridade.

### 4. Questione a origem

De onde veio a prova? Como chegou ao processo? Se o perito aceitou a prova por email, sem documentar a origem, isso é uma falha grave.

### 5. Levante a questão no momento da impugnação

O momento mais estratégico para questionar a cadeia de custódia é na impugnação do laudo pericial. É quando você pode apontar as falhas e pedir que a prova seja desconsiderada.

## Conclusão

A cadeia de custódia digital não é um detalhe técnico. É o que garante que uma prova digital tenha valor em juízo.

Quando ela é respeitada, a prova é confiável. Quando é quebrada, a prova perde valor — e o processo pode ser decidido com base em evidências frágeis.

Se você é advogado e atua em casos que envolvem provas digitais, dominar esse conceito é essencial. E se precisar de suporte técnico para auditar a cadeia de custódia de uma prova digital, estou à disposição.

---

**Precisa verificar se a cadeia de custódia de uma prova digital no seu processo está íntegra?**

[Solicitar diagnóstico de viabilidade →](https://peritofabricioribeiro.com.br)