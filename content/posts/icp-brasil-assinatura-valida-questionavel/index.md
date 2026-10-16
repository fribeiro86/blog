---
title: "ICP-Brasil: quando a assinatura eletrônica é válida e quando é questionável"
date: 2026-09-26T16:00:00-03:00
draft: false
description: "Nem toda assinatura com certificado ICP-Brasil é prova suficiente em juízo. Entenda a diferença entre validade criptográfica e validade probatória, e como identificar laudos que confundem as duas."
tags: ["ICP-Brasil", "assinatura eletrônica", "laudo pericial", "impugnação", "computação forense", "prova digital"]
author: "Fabricio do Nascimento Ribeiro"
---

## "A assinatura é válida." E agora?

Você recebe o laudo. O perito do juízo escreveu, com todas as letras: **a assinatura eletrônica é válida**. Certificado dentro do prazo, cadeia de certificação íntegra, carimbo de tempo autêntico. Conclusão: o documento é da parte contrária, e o processo segue.

A maioria dos advogados para por aqui. Lê o resultado, fecha o laudo, e tenta reverter em outra frente.

O problema é que **validade criptográfica não é a mesma coisa que validade probatória**. E é exatamente aí que mora a brecha.

Para entender como a cadeia de custódia se conecta a essa brecha, leia o artigo [Cadeia de Custódia Digital: O que é e Por que é Decisiva em Processos Judiciais](/posts/cadeia-de-custodia-digital/).

Neste artigo, vou mostrar — com base em casos reais que atendo — **quando uma assinatura ICP-Brasil é realmente prova suficiente em juízo, e quando ela é apenas um dos elementos que precisam ser confrontados**.

![Validação de certificado digital ICP-Brasil em documento assinado eletronicamente](/images/icp-validacao.jfif)
---

## O que o ICP-Brasil garante (e o que não garante)

A Infraestrutura de Chaves Públicas Brasileira (ICP-Brasil) é o sistema oficial de certificação digital do país. Quando um documento é assinado com um certificado ICP-Brasil, o sistema garante três coisas:

1. **Autenticidade** — a assinatura foi feita com a chave privada correspondente ao certificado
2. **Integridade** — o documento não foi alterado após a assinatura
3. **Não repúdio** — o titular do certificado não pode negar que assinou (em tese)

Isso é o que a **criptografia** garante. E é isso que o laudo pericial costuma verificar.

Mas repara no que **não está nessa lista**:

- ❌ Se **quem** assinou era realmente o titular do certificado (ou alguém usando o certificado dele)
- ❌ Se **o contexto** da assinatura foi legítimo (login, senha, dispositivo, biometria)
- ❌ Se **o documento assinado** é o mesmo que está sendo juntado aos autos
- ❌ Se **a cadeia de custódia** foi preservada entre a coleta e a perícia

É aqui que a coisa desanda.

---

## O caso que me fez escrever este artigo

Há alguns anos, uma advogada me contratou para impugnar um laudo que ela considerava **perdido**.

Quando perguntei o que ela tinha achado do laudo, a resposta foi sincera: *"na verdade, nem li. Fui pro final e vi o resultado."*

Cara, surreal. Mas é a realidade. A maioria dos advogados não tem formação técnica para ler um laudo de assinatura eletrônica linha por linha. Vão no resultado.

O laudo em questão **parecia robusto**. O perito detalhou as limitações técnicas, tintin por tintin. Explicou o que era hash, o que era carimbo de tempo, o que era certificado digital. Um trabalho que, na superfície, dava segurança ao juízo.

No final, ele considerou o **conjunto probatório como satisfeito**. Conclusão: a assinatura era da autora.

Mas esmiuçando o laudo, a história era outra.

---

## O que o perito deixou passar

Examinando o documento com calma, identifiquei **três omissões críticas**:

### 1. O banco não apresentou prova de vida (liveness)

Em contratos digitais, a prova de vida (também chamada de *liveness detection*) é o mecanismo que confirma que **a pessoa real** estava do outro lado da tela no momento da assinatura. Sem isso, um certificado digital pode ter sido usado por terceiro — ou até por alguém que obteve a senha do titular.

O banco **não juntou** essa prova. O perito **não exigiu**.

### 2. O dispositivo não foi associado à autora

Em contratos eletrônicos bancários, é padrão registrar **de qual dispositivo** (celular, computador, tablet) partiu a assinatura. Esse dado permite verificar se houve quebra de padrão (ex: assinatura feita de um IP em outro estado, em horário incompatível com o histórico do cliente).

O laudo **não analisou** esse ponto.

### 3. O perito não explicou o que eram as "portas lógicas"

O laudo mencionava "portas lógicas" no processo de autenticação, mas **não explicou o que eram** nem como se aplicavam ao caso concreto. Termo técnico sem contextualização não é fundamentação — é verniz.

---

## O resultado

Com base nesses pontos, elaborei um **parecer técnico** demonstrando que o laudo oficial havia confundido **validade criptográfica** com **validade probatória**. O perito respondeu "sim" para as perguntas da criptografia, mas deixou de responder "sim" para as perguntas da prova.

**Viramos o jogo.** O processo, que a advogada considerava perdido, teve a conclusão revertida.

E o detalhe: **eu cobrei bem baratinho na época.** Não porque o trabalho valia pouco, mas porque ainda estava construindo minha carteira de casos. Hoje, o valor é outro.

---

## A diferença entre validade criptográfica e validade probatória

Guarda essa tabela. Ela resume o artigo inteiro.

| **Validade criptográfica** | **Validade probatória** |
|---|---|
| O certificado estava dentro do prazo? | O documento apresentado é o mesmo que foi assinado? |
| A assinatura confere com a chave pública? | Houve alteração após a assinatura? |
| O carimbo de tempo é autêntico? | A cadeia de custódia foi preservada? |
| O certificado é ICP-Brasil? | O contexto da assinatura foi verificado (liveness, dispositivo, IP)? |
| A cadeia de certificação está íntegra? | O perito analisou metadados e logs? |

**Um laudo pode responder "sim" para a coluna da esquerda e "não" para a coluna da direita.** Quando isso acontece, há omissão metodológica — e omissão metodológica é base sólida para impugnação.

---

## O que o perito tem obrigação de verificar

Um laudo pericial sobre assinatura eletrônica só está completo se verificar, no mínimo:

- [ ] **Autenticidade criptográfica** — certificado, chave pública, cadeia de certificação
- [ ] **Integridade do documento** — hash do arquivo assinado vs. hash do arquivo juntado
- [ ] **Carimbo de tempo (RFC 3161)** — quando o documento existia
- [ ] **Contexto de assinatura** — liveness, biometria, dispositivo, IP, geolocalização
- [ ] **Metadados** — data de criação, modificação, software, autor técnico
- [ ] **Cadeia de custódia** — como o documento foi coletado, armazenado e apresentado
- [ ] **Logs de auditoria** — registros do sistema de assinatura, quando disponíveis

Se o laudo verifica **apenas os três primeiros**, ele está incompleto.

---

## O erro mais comum que vejo em laudos

Vou ser direto: a maioria dos laudos que analiso comete o mesmo vício.

**Eles confundem "assinatura válida" com "prova suficiente".**

Validade criptográfica é **condição necessária**, mas não **condição suficiente** para que a assinatura seja aceita como prova em juízo.

É como dizer que um contrato tem firma reconhecida em cartório, e por isso é automaticamente válido — ignorando que a firma pode ter sido obtida sob coação, que o contrato pode ter sido alterado depois, ou que a pessoa que assinou não tinha capacidade civil no momento.

**A criptografia prova o "como". Não prova o "quem" nem o "contexto".**

---

## O que fazer quando o laudo é desfavorável

Se você recebeu um laudo que conclui pela validade da assinatura, e a sua tese depende de questionar isso, o caminho é:

1. **Triagem técnica do laudo** — em 24-48h, identificar se há omissões metodológicas viáveis
2. **Diagnóstico de viabilidade** — parecer objetivo sobre as chances reais de reversão
3. **Análise forense aprofundada** — exame dos documentos, metadados, logs e contexto de assinatura
4. **Formulação de quesitos complementares** — perguntas técnicas que o perito é **obrigado a responder** (Art. 477, § 2º, CPC)
5. **Protocolo da impugnação** — dentro do prazo de 15 dias, com fundamentação técnica robusta

O prazo do Art. 477 é exíguo. **Não dá pra improvisar.**

---

## Uma observação honesta sobre prazos

Eu não aceito fazer parecer um dia antes de terminar o prazo.

Já fiz na correria. Não ficou bom. Aprendi que **um parecer técnico de qualidade exige 2 a 3 dias de análise séria** — tempo pra examinar metadados, comparar hashes, ler logs, cruzar contexto e escrever com rigor.

Se o prazo é curto, o caminho é começar pelo **diagnóstico de viabilidade** (24h), que já dá base pra decidir se vale investir no parecer completo.

---

## Conclusão

Uma assinatura ICP-Brasil é **condição necessária**, mas não **suficiente** para que um documento seja aceito como prova em juízo. O laudo pericial que ignora contexto de assinatura, cadeia de custódia, metadados e logs está **incompleto** — e pode ser impugnado.

Se você atua em processo com prova digital e o laudo foi desfavorável, **o momento de agir é agora**. O prazo de 15 dias do Art. 477 do CPC não espera.

---

**Fabricio do Nascimento Ribeiro** é perito judicial em Computação Forense credenciado pelo TJSC, com 14 nomeações oficiais. Atua na análise de laudos periciais sobre assinaturas eletrônicas, contratos digitais e validade de evidências cibernéticas.

👉 [Solicitar diagnóstico de viabilidade para impugnação de laudo pericial](https://peritofabricioribeiro.com.br)👉