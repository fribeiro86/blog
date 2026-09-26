---
title: "Metadados de documentos digitais: a prova que ninguém olha"
date: 2026-09-26T10:00:00-03:00
draft: false
description: "Metadados revelam quando, como e por quem um documento digital foi criado ou alterado. Entenda por que essa prova é ignorada nos laudos periciais e como usá-la a favor do seu cliente."
tags: ["metadados", "prova digital", "computação forense", "laudo pericial", "impugnação"]
author: "Fabricio do Nascimento Ribeiro"
---

## O que são metadados (e por que o Judiciário ignora)

Todo documento digital carrega duas camadas de informação. A primeira é **visível**: o texto, a assinatura, o conteúdo que qualquer pessoa lê ao abrir o arquivo. A segunda é **invisível** — e é justamente aí que mora a prova mais poderosa de um processo: os **metadados**.

Metadados são dados que descrevem outros dados. Em um PDF, por exemplo, eles registram:

- **Quem** criou o arquivo (nome do autor no sistema operacional)
- **Quando** foi criado e **quando** foi modificado pela última vez
- **Com qual software** foi produzido (versão do Word, Adobe, LibreOffice…)
- **Se houve edição após a assinatura** (alteração de hash)
- **Quantas vezes foi impresso ou convertido**

A praxe forense demonstra que a maioria dos laudos periciais sobre assinatura eletrônica analisa apenas a camada visível — a validade criptográfica do certificado. Os metadados, que podem contradizer completamente essa conclusão, costumam passar despercebidos.

**Isso é uma brecha técnica enorme.**

---

## Por que metadados importam em um processo judicial

Imagine o seguinte cenário: um contrato digital é apresentado como prova, assinado eletronicamente em 10 de março de 2024. O laudo do perito oficial conclui que a assinatura é válida porque o certificado digital está dentro do prazo de validade.

Agora suponha que a análise dos metadados revele que:

- O arquivo foi **criado em 12 de março de 2024** (dois dias após a suposta assinatura)
- Foi **modificado em 15 de março de 2024**, após a coleta da assinatura
- O software usado na conversão final foi diferente do que consta no corpo do documento

Essas contradições, sozinhas, podem invalidar a cronologia dos fatos — mesmo que a assinatura criptográfica esteja "tecnicamente válida".

> **Ponto-chave:** uma assinatura digital válida prova que *alguém* assinou com aquele certificado. Ela **não prova** que o documento assinado é o mesmo que está sendo juntado aos autos. É aí que os metadados entram.

---

## O que examinar nos metadados de um documento digital

Uma auditoria forense séria verifica, no mínimo:

### 1. Cronologia do arquivo
- Data de criação (`CreationDate`)
- Data da última modificação (`ModDate`)
- Divergência entre essas datas e a data da assinatura declarada

### 2. Autoria técnica
- Nome do usuário no sistema operacional que gerou o arquivo
- Software e versão utilizados
- Divergência entre autor declarado e autor técnico

### 3. Integridade estrutural
- Alterações na estrutura interna do PDF após a assinatura
- Inclusão ou remoção de páginas, anexos ou campos
- Comparação entre o hash do documento assinado e o hash do documento apresentado

### 4. Trilhas de auditoria
- Registros de log do sistema de assinatura (quando disponíveis)
- Carimbos de tempo (RFC 3161) e sua coerência com os metadados

### 5. Cadeia de custódia digital
- Como o arquivo foi coletado, armazenado e transferido
- Se houve conversão de formato entre a coleta e a apresentação em juízo

---

## O erro mais comum nos laudos periciais

A maioria dos laudos que analiso comete o mesmo vício metodológico: **confunde validade criptográfica com validade probatória**.

São coisas diferentes.

| Validade criptográfica | Validade probatória |
|---|---|
| O certificado estava dentro do prazo? | O documento apresentado é o mesmo que foi assinado? |
| A assinatura confere com a chave pública? | Houve alteração após a assinatura? |
| O carimbo de tempo é autêntico? | A cadeia de custódia foi preservada? |

Um laudo pode responder "sim" para a coluna da esquerda e "não" para a da direita. Quando isso acontece, há espaço para impugnação técnica fundamentada.

---

## Como usar metadados na impugnação

O Art. 477, § 2º, do CPC garante à parte o direito de formular quesitos e exigir esclarecimentos do perito oficial. Metadados são um dos pontos mais eficazes para **compelir o perito a se manifestar** — porque exigem resposta técnica objetiva, não retórica.

Uma impugnação bem construída pode formular quesitos como:

1. O perito examinou os metadados do arquivo PDF juntado aos autos?
2. A data de modificação do arquivo é compatível com a data da assinatura declarada?
3. Houve alteração estrutural no documento entre a assinatura e a juntada?
4. O hash do documento assinado é idêntico ao hash do documento apresentado?

Se o perito não examinou esses pontos, há omissão metodológica. Se examinou e ignorou, há contradição interna no laudo. **Ambos os cenários favorecem a tese da parte.**

---

## O que fazer quando o prazo aperta

O prazo para impugnação é de 15 dias contados da juntada do laudo (Art. 477, § 1º, CPC). Nesse intervalo, é praticamente impossível que um advogado — sem formação em computação forense — consiga:

- Extrair e interpretar metadados de PDFs, DOCs e imagens
- Comparar hashes e carimbos de tempo
- Identificar conversões de formato que alteram a integridade do arquivo
- Formular quesitos técnicos que o perito não possa responder de forma genérica

É exatamente por isso que a **assistência técnica especializada** existe. Não para "inventar" falhas, mas para **auditar com rigor** o que o laudo oficial deixou de examinar.

---

## Conclusão

Metadados são a prova silenciosa do processo digital. Eles não aparecem na leitura do documento, não são citados em petições genéricas e — na maioria das vezes — não são examinados pelo perito oficial.

Mas quando examinados com rigor técnico, podem:

- Contradizer a cronologia dos fatos
- Invalidar a cadeia de custódia
- Expor omissões metodológicas no laudo
- Sustentar uma impugnação tecnicamente inatacável

Se você atua em processo com prova digital e o laudo pericial foi desfavorável, **os metadados são o primeiro lugar onde se deve olhar**.

---

**Fabricio do Nascimento Ribeiro** é perito judicial em Computação Forense credenciado pelo TJSC, com 14 nomeações oficiais. Atua na análise de laudos periciais sobre assinaturas eletrônicas, contratos digitais e validade de evidências cibernéticas.

👉 [Solicitar diagnóstico de viabilidade para impugnação de laudo pericial](/)