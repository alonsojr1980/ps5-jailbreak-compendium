# ⚡ Assistente Interativo de Jailbreak & Exploit do PS5
### *by ALONSOJR1980*

<div align="center">

[![Firmwares Suportados](https://img.shields.io/badge/Assistente%20Interativo-FW%201.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Exploit](https://img.shields.io/badge/Gerador%20Customizado-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](#)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](#)

**Idiomas / Languages:**
[🇧🇷 Português](README.md) | [🇺🇸 English](../en/README.md) | [🇪🇸 Versión en Español](../es/README.md)

</div>

Selecione o modelo do seu console PlayStation 5 e a versão do seu firmware abaixo para gerar instantaneamente um guia de execução personalizado, configurações de DNS recomendadas e comandos de injeção de payload para o terminal.

---

<!-- COMPONENTE DO WIZARD INTERATIVO -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ ASSISTENTE INTERATIVO DE FIRMWARE</div>
<h2 class="ps-wizard-title">Gerador Sob Medida de Jailbreak & Exploit</h2>
<p class="ps-wizard-subtitle">Escolha o modelo de hardware do PS5 e a versão do firmware para obter instruções customizadas de desbloqueio.</p>
</div>
<div class="ps-wizard-controls">
<!-- Seleção de Modelo -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">1. ESCOLHA O MODELO DO CONSOLE:</label>
<div class="ps-model-buttons">
<button type="button" class="ps-model-btn active" data-model="fat" onclick="setWizardModel('fat')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Fat</span>
<span class="model-sub">CFI-1000 / 1100 / 1200</span>
</button>
<button type="button" class="ps-model-btn" data-model="slim" onclick="setWizardModel('slim')">
<span class="model-icon">🕹️</span>
<span class="model-name">PS5 Slim</span>
<span class="model-sub">CFI-2000 (Leitor Removível)</span>
</button>
<button type="button" class="ps-model-btn" data-model="pro" onclick="setWizardModel('pro')">
<span class="model-icon">🚀</span>
<span class="model-name">PS5 Pro</span>
<span class="model-sub">CFI-7000 (Leitor Removível)</span>
</button>
</div>
</div>
<!-- Seleção de Firmware -->
<div class="ps-wizard-field">
<label class="ps-wizard-label">2. ESCOLHA O TIPO DE EXPLOIT E FAIXA DE FIRMWARE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Relapse Exploit</span>
<span class="ps-exploit-badge ready">WebKit</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">WebKit (JSC) + Exploit de Kernel aio_multi_wait</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">BD-JB / Mast1c0re</span>
<span class="ps-exploit-badge ready">Disco / PS2</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">Disco Blu-ray BD-J / Savegame PS2 + aio_multi_wait</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX2 / Mast1c0re</span>
<span class="ps-exploit-badge wip">Em Progresso</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">Primitivas UMTX2 e Savegame PS2 (Porting em Andamento)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">UMTX Exploit</span>
<span class="ps-exploit-badge ready">Kernel UAF</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">Primitivas Mutex libthr FreeBSD (CVE-2024-43102)</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">IPv6 Socket UAF</span>
<span class="ps-exploit-badge ready">Era de Ouro</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">Socket UAF netinet6 FreeBSD / UMTX</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Byepervisor</span>
<span class="ps-exploit-badge special">Ring -1 Root</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">Comprometimento Total do Hypervisor (Santo Graal)</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Endereço IP do Console (opcional):</span>
<span class="ps-ip-desc">Personaliza os comandos netcat no checklist de execução abaixo para o seu console.</span>
</label>
<input type="text" id="customIpInput" class="ps-input" value="192.168.1.150" placeholder="192.168.1.xxx" oninput="onCustomIpInput(this.value)">
</div>
</div>
</div>
<!-- Resultado Dinâmico -->
<div id="psWizardResult" class="ps-wizard-result"></div>
</div>

---

## 🛡️ Checklist Global de Blindagem Pré-Jailbreak

Independentemente do modelo ou faixa de firmware, aplique estas configurações antes de conectar o console à rede:

1. **Configurações do Software do Sistema**:
   - Acesse **Configurações ➔ Sistema ➔ Software do Sistema ➔ Atualizações e Configurações do Software do Sistema**.
   - Desative **Baixar Arquivos de Atualização Automaticamente**.
   - Desative **Instalar Arquivos de Atualização Automaticamente**.
2. **Economia de Energia no Rest Mode**:
   - Acesse **Configurações ➔ Sistema ➔ Economia de Energia ➔ Recursos Disponíveis no Rest Mode**.
   - Desative **Continuar Conectado à Internet**.
3. **Downloads Automáticos de Jogos e Apps**:
   - Acesse **Configurações ➔ Dados Salvos e Configurações de Jogos/Aplicativos ➔ Atualizações Automáticas**.
   - Desative **Download Automático** e **Instalação Automática no Rest Mode**.

---

## ⚠️ Lembrete Crítico sobre o Leitor Removível

> [!CAUTION]
> Se o seu console é um **PS5 Slim (CFI-2000)** ou **PS5 Pro (CFI-7000)**:
> - O leitor de disco removível exige um **Handshake** criptográfico com os servidores da Sony para ser autenticado pela primeira vez.
> - **Nunca conecte à PSN para registrar o leitor se o console estiver em firmware suscetível a jailbreak (<= 13.60)**, pois isso **forçará uma atualização irreversível para o firmware mais recente**.
> - Backups digitais, emuladores, homebrew e armazenamento em SSD M.2 funcionam 100% sem o leitor físico pareado.

---

<p align="center">
  <b>🤖 Assistente Interativo de Firmware para a Comunidade PS5</b><br>
  <i>Selecione seu modelo e firmware para gerar instruções personalizadas e seguras de desbloqueio.</i>
</p>
