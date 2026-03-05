
<div align="center">

<img src="assets/img/icon.png" alt="Social Media ID Cheatsheet" width="220" style="margin-bottom: 20px;"/>

# 🕵️ RavAgents

> Coleção de agentes investigativos para LLMs — prompts estruturados para fact-checking, OSINT e combate à desinformação  
> Compatível com: ChatGPT · Gemini · Grok · Claude · Copilot e afins

---

## 📌 O que é este projeto?

**RavAgents** é uma coleção de prompts que transformam qualquer LLM em agentes investigativos especializados. Cada agente possui metodologia própria, hierarquia de fontes definida, padrões de detecção estruturados e saída padronizada em relatório TXT + diagrama Mermaid.

Os agentes não executam código — eles são instruções precisas que guiam modelos de linguagem a conduzir investigações replicáveis, céticas e baseadas exclusivamente em fontes verificáveis.

Feito para pesquisadores, jornalistas, profissionais de segurança da informação, usuários técnicos e a comunidade open source em geral.

[![➜ ​ ​TOON](https://img.shields.io/badge/➜%20%20toon-gray.svg)](https://toonformat.dev/) 

</div>

---

## 📁 Estrutura do repositório

```
📁 ravagents/
├── 📄 README.md                        ← você está aqui
├── 📜 LICENSE
└── 🗂️ agents/
    ├── 🔵 winprobe-agent/              ← fake news Windows/Microsoft
    │   ├── 📄 README.md
    │   ├── 📝 prompt.txt
    │   └── 🧩 prompt.toon
    ├── 🟣 invosint/              ← investigação de perfis públicos BR
    │   ├── 📄 README.md
    │   ├── 📝 prompt.txt
    │   └── 🧩 prompt.toon
    └── ⚫ [entre outros agentes...]/
```

Cada pasta de agente contém:

| Arquivo       | Descrição                                                                          |
| ------------- | ---------------------------------------------------------------------------------- |
| `README.md`   | Documentação completa do agente, funcionalidades e como usar                       |
| `prompt.txt`  | Prompt em formato texto convencional — cole em qualquer LLM                        |
| `prompt.toon` | Prompt em formato TOON (Token-Oriented Object Notation) — estruturado e versionado |

---

## 🤖 Agentes disponíveis

<details>
<summary>🔵 <strong><a href="agents/winprobe-agent/">winprobe-agent</a></strong> <code>v1.0.0</code> — fake news Windows/Microsoft</summary>

<br>

Agente especializado em investigar desinformação técnica sobre Windows e produtos Microsoft. Verifica se notícias, artigos ou posts sobre bugs, falhas, vulnerabilidades ou comportamentos anômalos do Windows são verídicos, sensacionalistas, meia-verdade ou fake news completa.

**Destaques:**
- Consulta obrigatória ao Windows Release Health e páginas oficiais de KB
- Cruzamento com MVPs Microsoft verificados (Baboo / Aurélio Minerbo)
- 8 padrões de desinformação categorizados (FN-01 a FN-08)
- 11 red flags com severidade e evidência
- Lista de perfis com histórico de alegações não verificadas
- Veredicto: `VERDADEIRO` · `PARCIALMENTE VERDADEIRO` · `SENSACIONALISTA` · `FAKE NEWS`

</details>

---

<details>
<summary>🟣 <strong><a href="agents/invosint/">invosint</a></strong> <code>v1.0.0</code> — investigação de perfis públicos BR</summary>

<br>

Agente OSINT investigativo de nível expert para análise forense de perfis públicos digitais e profissionais no Brasil. Adaptável a qualquer tipo de alvo: médicos, advogados, coaches, influenciadores, profissionais de infosec e muito mais.

**Destaques:**
- Verificação de registros profissionais (CRM, OAB, CREA, CRP e equivalentes)
- Google Dorks sistematizados para fraude, identidade e acadêmico
- OPSEC Awareness — distingue opacidade fraudulenta de segurança operacional legítima
- 12 red flags categorizados com severidade (RF-01 a RF-12)
- 13 vetores de ataque mapeados (AV-01 a AV-13)
- Análise dedicada de lojas golpistas com 7 sinais estruturados e thresholds
- Análise de pirâmide financeira e MLM fraudulento com aviso de torpeza bilateral
- Confidence level com cap de 95/100 para perfis com OPSEC legítimo

</details>

---

### ⚫ Mais agentes em desenvolvimento

Novos agentes serão adicionados progressivamente. Se você tem uma ideia de agente investigativo, abra uma [issue](../../issues) com a descrição do escopo, fontes de referência e metodologia proposta.

---

## 🚀 Como usar qualquer agente

**1. Escolha o agente** adequado para sua investigação.

**2. Abra o `prompt.txt`** da pasta do agente e copie o conteúdo completo.

**3. Preencha os dados do alvo** nos campos marcados como `SUBSTITUIR` no topo do prompt.

**4. Cole em qualquer LLM compatível:**

- [Grok](https://grok.com/) — Expert / SuperGrok
- [Claude](https://claude.ai)
- [ChatGPT](https://chat.openai.com)
- [Gemini](https://gemini.google.com)
- [Copilot](https://copilot.microsoft.com)
- [DeepSeek](https://chat.deepseek.com/)
- [ArenaAI](https://arena.ai/)

**5. Receba o relatório** completo com todas as seções obrigatórias, matriz de red flags, arquivo `.txt` forense e diagrama Mermaid exportável.

---

## 📐 Formato TOON

Todos os agentes deste projeto estão disponíveis também no formato **TOON (Token-Oriented Object Notation)** — uma notação estruturada e legível por humanos e máquinas, projetada para definir agentes de IA de forma versionável e extensível.

O arquivo `.toon` de cada agente é o formato canônico do projeto. O `prompt.txt` é gerado a partir dele para facilitar o uso imediato em interfaces de LLMs.

---

## 🗂️ Saída padronizada

Todos os agentes geram dois artefatos ao final da investigação:

```
📄 Relatório TXT forense    →  [agent-slug]-[identificador]-[data].txt
📊 Diagrama Mermaid          →  [agent-slug]-[identificador]-[data].mmd
```

O diagrama é compatível com GitHub README, GitHub Gist e [mermaid.live](https://mermaid.live).

---

## 🤝 Contribuindo

Contribuições são bem-vindas. Se você criou um novo agente, aprimorou um existente, adicionou uma entrada verificada em alguma lista ou encontrou um erro, abra uma issue ou pull request.

**Para adicionar um novo agente**, a pasta deve conter obrigatoriamente `README.md`, `prompt.txt` e `prompt.toon`, seguindo a estrutura e os padrões de qualidade dos agentes existentes. Cada agente precisa ter: escopo bem definido, hierarquia de fontes documentada, padrões de detecção categorizados e saída estruturada em TXT + Mermaid.

**Para adicionar uma entrada em listas internas** de um agente (como perfis monitorados no winprobe ou red flags no osint), são obrigatórios URL do conteúdo original, URL do desmentido por fonte verificável e data aproximada de ambos.

---

## ⚠️ Aviso legal

Este projeto é de uso **estritamente investigativo, informativo e educacional**. Todos os dados são obtidos exclusivamente de **fontes públicas verificáveis**. Os relatórios gerados não constituem prova judicial e não devem ser utilizados para fins de difamação, assédio ou qualquer atividade ilícita.

O uso é de responsabilidade exclusiva de quem executa a investigação. Cada agente possui seu próprio aviso legal detalhado no respectivo `README.md` — leia antes de usar.

Respeite a legislação vigente, incluindo a **LGPD (Lei nº 13.709/2018)** e os **arts. 138, 139 e 140 do Código Penal** (crimes contra a honra).

---

## 📄 Licença

Distribuído sob a licença **MIT**. Consulte o arquivo [`LICENSE`](./LICENSE) para mais detalhes.

A licença MIT permite uso, cópia, modificação e distribuição livre, inclusive para fins comerciais, desde que o aviso de copyright e a licença sejam mantidos. Os avisos legais específicos de cada agente são parte integrante do projeto e devem ser preservados em todas as versões derivadas.

---

## 📞 Suporte 

Se precisar de ajuda ou quiser falar com a equipe, entre no nosso servidor de suporte:

[![Servidor de Suporte](https://img.shields.io/badge/Servidor%20de%20Suporte-Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/FncVNprdgP)

---

## 🌟 Star History

<a href="https://www.star-history.com/?repos=ravenastar-js%2Fravagents&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/image?repos=ravenastar-js/ravagents&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/image?repos=ravenastar-js/ravagents&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/image?repos=ravenastar-js/ravagents&type=date&legend=top-left" />
 </picture>
</a>

---

<div align="center">
  <sub>agents · prompts investigativos para LLMs · use com ceticismo, responsabilidade e fontes verificáveis</sub>
</div>