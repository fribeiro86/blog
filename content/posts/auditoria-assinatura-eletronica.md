---
title: "Como Funciona a Auditoria de Assinaturas Eletrônicas"
date: 2026-09-26T17:25:00-03:00
draft: false
description: "Entenda os critérios técnicos para validar assinaturas eletrônicas e detectar fraudes em documentos digitais analisando metadados e registros de rede."
tags: ["Assinatura Eletrônica", "Metadados", "Computação Forense", "CGNAT"]
categories: ["Artigos"]
---

A validade de um documento digital vai muito além do aspecto visual de uma assinatura. Na perícia judicial, a auditoria de assinaturas eletrônicas exige uma análise profunda das camadas ocultas do arquivo para garantir a integridade da prova.

### Onde as Fraudes se Escondem

Muitas falsificações ocorrem na manipulação direta do PDF. Para identificar se um documento foi adulterado após a assinatura, o exame pericial concentra-se na extração de metadados e na verificação do histórico de edições estruturais do arquivo.

![Análise de metadados e hashes em um documento PDF](/images/analise-metadados.jpg)
*Inspeção técnica revelando a cadeia de custódia e registros de IP/CGNAT do signatário. (Lembre-se de colocar sua imagem real na pasta static/images/)*

### Critérios de Validação Técnica

Para que um Parecer Técnico ateste a integridade da assinatura de forma irrefutável, avaliamos três pilares principais:

1. **Validação Criptográfica:** Verificação da chave pública e da cadeia de confiança do certificado utilizado no momento da assinatura.
2. **Teste de Liveness (Prova de Vida):** Em assinaturas que utilizam biometria facial, checamos a conformidade com normas técnicas, como a ISO/IEC 30107-3, para descartar o uso de fotos estáticas ou manipulações em vídeo.
3. **Rastreabilidade de Rede:** Análise detalhada dos logs de conexão, incluindo portas e IPs sob CGNAT, cruzando a localização temporal e geográfica do assinante.

A adulteração documental sempre deixa rastros digitais. A aplicação da metodologia forense correta garante a segurança jurídica necessária para impugnar ou validar a evidência no processo.
