<div align="center">

<img src="./assets/hero.svg" width="100%" alt="Rafael Massena — software local-first para escrita e português brasileiro" />

### Software local-first para escrita e português brasileiro.

`Vanilla JavaScript` · `PWA` · `engines linguísticas` · `interfaces offline`

[Escrevaral](https://escrevaral.com) · [arquitetura](https://github.com/rfmss/escrevaral/blob/main/ARCHITECTURE.md) · [experimento atual](https://github.com/rfmss/escrevaral/pull/155) · [rafa.pro.br](https://rafa.pro.br)

</div>

## 01 // Sistema principal

### [Escrevaral](https://github.com/rfmss/escrevaral)

Criei o Escrevaral para escrever, preservar e analisar manuscritos no navegador sem transformar o texto em tráfego de uma plataforma. A versão pública **Argila 1.0.0** usa HTML, CSS e JavaScript sem framework e permanece utilizável sem internet depois da instalação.

| Fronteira | Implementação verificável |
| :--- | :--- |
| **Execução** | aplicação estática no navegador, sem servidor de aplicação ou conta obrigatória |
| **Preservação** | estado local, exportação, cópia de segurança e contratos explícitos para migração e conflito |
| **Linguagem** | engines e dados linguísticos versionados, processados no dispositivo |
| **Distribuição** | service worker na raiz, cache versionado e auditoria de publicação offline |
| **Qualidade** | gate de release candidate mais workflows especializados de dados, navegação, privacidade e acessibilidade |

[usar o produto ↗](https://escrevaral.com) · [ler a arquitetura ↗](https://github.com/rfmss/escrevaral/blob/main/ARCHITECTURE.md) · [ver os gates de lançamento ↗](https://github.com/rfmss/escrevaral/blob/main/docs/release/LAUNCH_CHECKLIST.md)

### Em validação: Mass Notes Next

A próxima fundação está isolada numa branch experimental: editor Tiptap/ProseMirror, IndexedDB, autosave, revisões, recuperação, conflitos explícitos e engines locais lendo o snapshot vivo. O trabalho possui gates cross-browser e **não substitui a versão pública enquanto a evidência não autorizar a promoção**.

[acompanhar o PR técnico #155 ↗](https://github.com/rfmss/escrevaral/pull/155)

## 02 // Sistemas selecionados

| Sistema | Problema tratado | Decisões que podem ser inspecionadas |
| :--- | :--- | :--- |
| **[Dirlizanu](https://github.com/rfmss/dirlizanu)** | campanha e laboratório de quebra-cabeças 4 × 4 e 5 × 5 | geração por movimentos legais; auditoria de paridade, unicidade e progressão; adaptação ao `visualViewport`; áudio sintetizado localmente |
| **[Pomodoro](https://github.com/rfmss/pomodoro)** | cronômetro que não perde o tempo quando a tela bloqueia | relógio baseado em horário absoluto; engine separada do DOM; sessão persistente; auditores do timer e do ciclo; PWA offline |
| **[Boletos Mil](https://github.com/rfmss/boletosmil)** | organização doméstica sem integração bancária ou conta remota | regras de domínio puras; scanner de privacidade; build estático reproduzível; publicação restrita a `dist/`; exportação e restauração em JSON |
| **[RafaMass Blueprint](https://github.com/rfmss/rfmss.github.io)** | identidade visual reutilizável sem transformar produtos diferentes no mesmo layout | tokens e componentes isolados por `[data-rm-blueprint]`; nenhuma fonte, imagem, framework ou JavaScript obrigatório; documentação de composição e acessibilidade |

## 03 // Registro de engenharia

| Artefato | O que demonstra |
| :--- | :--- |
| [Arquitetura do Escrevaral](https://github.com/rfmss/escrevaral/blob/main/ARCHITECTURE.md) | fronteiras de produto, persistência, modelo offline, contratos de interface e dívida estrutural declarada |
| [Mass Notes Next — PR #155](https://github.com/rfmss/escrevaral/pull/155) | experimento governado por gates, limites linguísticos explícitos e promoção suspensa até validação |
| [Auditor de níveis do Dirlizanu](https://github.com/rfmss/dirlizanu/blob/main/scripts/audit-levels.js) | matrizes solucionáveis, ausência de duplicatas e progressão mensurável |
| [Auditores do Pomodoro](https://github.com/rfmss/pomodoro/tree/main/scripts) | precisão do relógio e invariantes do ciclo fora da interface |
| [Auditoria de privacidade do Boletos Mil](https://github.com/rfmss/boletosmil/blob/main/docs/PRIVACY_AUDIT.md) | separação entre produto público e origem privada, varredura de dados e limites do armazenamento local |
| [Assinatura visual RafaMass](https://github.com/rfmss/rfmss.github.io/blob/main/docs/ASSINATURA-VISUAL.md) | sistema de tokens, hierarquia, responsividade, movimento e anti-padrões |

## 04 // Contato

**Rafael Massena** — escritor e desenvolvedor. A experiência com texto orienta os problemas que escolho resolver; os repositórios registram como cada solução foi construída e validada.

[rafa.pro.br](https://rafa.pro.br) · [rafamass@proton.me](mailto:rafamass@proton.me) · [@rafa.pro.br no Bluesky](https://bsky.app/profile/rafa.pro.br) · [@xrafamass no X](https://x.com/xrafamass)

<sub>`Rafa Mass` é a assinatura pública. `rfmss` é a matrícula técnica.</sub>
