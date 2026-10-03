<h1 align="center" class="ps-main-header">⚡ Interactive PS5<br>Jailbreak & Exploit Wizard ⚡</h1>
<p align="center" class="ps-header-author">by ALONSOJR1980</p>

<div align="center">

[![Firmware PS5](https://img.shields.io/badge/Assistente%20Interativo-Rotas%20de%20Firmware-success?style=for-the-badge&logo=playstation&logoColor=white)](#)
[![Guia](https://img.shields.io/badge/Guia-Passo%20a%20Passo-blueviolet?style=for-the-badge&logo=playstation&logoColor=white)](#)

**Idiomas / Languages:**
[🇧🇷 Português](README.md) | [🇺🇸 English](../en/README.md) | [🇪🇸 Versión en Español](../es/README.md)

</div>

Selecione o modelo do seu PS5 e a faixa de firmware para ver as instruções adequadas ao seu console. Siga as etapas exibidas; não é necessário aprender como o software funciona.

---

<!-- COMPONENTE DO WIZARD INTERATIVO -->
<div class="ps-wizard-container" id="psWizard">
<div class="ps-wizard-header">
<div class="ps-wizard-badge">⚡ ASSISTENTE INTERATIVO DE FIRMWARE</div>
<h2 class="ps-wizard-title">Configuração do PS5 passo a passo</h2>
<p class="ps-wizard-subtitle">Escolha o modelo do console e a faixa de firmware para ver as etapas correspondentes.</p>
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
<label class="ps-wizard-label">2. ESCOLHA A FAIXA DO FIRMWARE:</label>
<div class="ps-exploit-grid">
<button type="button" class="ps-exploit-btn active" data-fw="9.60 - 13.60" onclick="setWizardFw('9.60 - 13.60')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 9.60–13.60</span>
<span class="ps-exploit-badge ready">ETAPAS DISPONÍVEIS</span>
</div>
<div class="ps-exploit-range">Firmware 9.60 – 13.60</div>
<div class="ps-exploit-sub">Siga as etapas exibidas para esta faixa de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="14.00+" onclick="setWizardFw('14.00+')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 14.00 ou superior</span>
<span class="ps-exploit-badge wip">SEM ETAPAS</span>
</div>
<div class="ps-exploit-range">Firmware 14.00+</div>
<div class="ps-exploit-sub">Este assistente não tem uma rota para esta versão. Mantenha o console offline.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="7.00 - 8.20" onclick="setWizardFw('7.00 - 8.20')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 7.00–8.20</span>
<span class="ps-exploit-badge wip">VERIFIQUE A ROTA</span>
</div>
<div class="ps-exploit-range">Firmware 7.00 – 8.20</div>
<div class="ps-exploit-sub">Este assistente ainda não inclui todas as etapas para esta faixa.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="6.00 - 6.50" onclick="setWizardFw('6.00 - 6.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 6.00–6.50</span>
<span class="ps-exploit-badge wip">AINDA NÃO PRONTO</span>
</div>
<div class="ps-exploit-range">Firmware 6.00 – 6.50</div>
<div class="ps-exploit-sub">Ainda não há instruções passo a passo para esta faixa.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="5.00 - 5.50" onclick="setWizardFw('5.00 - 5.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 5.00–5.50</span>
<span class="ps-exploit-badge ready">ETAPAS DISPONÍVEIS</span>
</div>
<div class="ps-exploit-range">Firmware 5.00 – 5.50</div>
<div class="ps-exploit-sub">Siga as etapas exibidas para esta faixa de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="3.00 - 4.51" onclick="setWizardFw('3.00 - 4.51')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 3.00–4.51</span>
<span class="ps-exploit-badge ready">ETAPAS DISPONÍVEIS</span>
</div>
<div class="ps-exploit-range">Firmware 3.00 – 4.51</div>
<div class="ps-exploit-sub">Siga as etapas exibidas para esta faixa de firmware.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="1.00 - 2.50" onclick="setWizardFw('1.00 - 2.50')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Firmware 1.00–2.50</span>
<span class="ps-exploit-badge wip">VERIFIQUE A ROTA</span>
</div>
<div class="ps-exploit-range">Firmware 1.00 – 2.50</div>
<div class="ps-exploit-sub">Este assistente ainda não inclui todas as etapas para esta faixa.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="8.21 - 9.59" onclick="setWizardFw('8.21 - 9.59')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Verifique a compatibilidade</span>
<span class="ps-exploit-badge wip">SEM ETAPAS</span>
</div>
<div class="ps-exploit-range">Firmware 8.21 – 9.59</div>
<div class="ps-exploit-sub">Este assistente não tem uma rota verificada para esta faixa.</div>
</button>
<button type="button" class="ps-exploit-btn" data-fw="unlisted" onclick="setWizardFw('unlisted')">
<div class="ps-exploit-header">
<span class="ps-exploit-name">Meu firmware não está na lista</span>
<span class="ps-exploit-badge wip">VERIFIQUE PRIMEIRO</span>
</div>
<div class="ps-exploit-range">Outra versão de firmware</div>
<div class="ps-exploit-sub">Não escolha uma faixa próxima; verifique a compatibilidade primeiro.</div>
</button>
</div>
<div class="ps-ip-wrap">
<label for="customIpInput" class="ps-ip-label">
<span class="ps-ip-title">Endereço IP do Console (opcional):</span>
<span class="ps-ip-desc">Usado para preencher os comandos se você escolher o método com computador ou celular.</span>
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
> - O leitor de disco removível precisa de um registro online único com a Sony para parear com o console.
> - **Nunca conecte à PSN para registrar o leitor se o console estiver em firmware suscetível a jailbreak (<= 13.60)**, pois isso **forçará uma atualização irreversível para o firmware mais recente**.
> - Backups digitais, emuladores, homebrew e armazenamento em SSD M.2 funcionam 100% sem o leitor físico pareado.

---

<p align="center">
  <b>🤖 Assistente Interativo de Firmware para a Comunidade PS5</b><br>
  <i>Selecione seu modelo e firmware para gerar instruções personalizadas e seguras de desbloqueio.</i>
</p>
