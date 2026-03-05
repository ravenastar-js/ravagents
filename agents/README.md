
> [!IMPORTANT]
> TRATAM-SE APENAS DE MODELOS BASE, NÃO CORRESPONDENDO A MODELOS COMPLETOS.

---

## 🤖 Agentes disponíveis

<details>
<summary>🔵 <strong><a href="invosint/">winprobe-agent</a></strong> <code>v1.0.0</code> — fake news Windows/Microsoft</summary>

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
<summary>🟣 <strong><a href="winprobe/">invosint</a></strong> <code>v1.0.0</code> — investigação de perfis públicos BR</summary>

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