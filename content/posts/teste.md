---
title: "A Importância do Hash SHA-256 na Perícia Digital"
date: 2026-09-26T16:11:00-03:00
draft: false
tags: ["Computação Forense", "Evidências Digitais", "Cadeia de Custódia"]
categories: ["Artigos"]
---

Na perícia judicial, a integridade da evidência é o pilar que sustenta qualquer avaliação técnica. É aqui que entra a importância do **Hash SHA-256**.

### O que é o Hash?
De forma simplificada, o algoritmo de hash atua como uma "impressão digital" de um arquivo. Ao submeter um documento, captura de tela ou log a um cálculo de hash, é gerada uma string alfanumérica única. Qualquer alteração, por menor que seja (como mudar um único pixel em uma imagem ou espaço em um texto), mudará completamente o código final.

### Aplicação Prática na Cadeia de Custódia
Seguindo as diretrizes da **ABNT NBR ISO/IEC 27037** para identificação e coleta de evidências, o cálculo do hash logo no momento da preservação garante que o material analisado no laboratório é exatamente o mesmo que foi coletado na origem. 

Em casos de auditoria de assinaturas eletrônicas e análise de metadados, apresentar os hashes correspondentes no Parecer Técnico é fundamental para afastar, tecnicamente, qualquer alegação de adulteração da prova material.