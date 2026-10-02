# 🚀 Como Fazer Jailbreak no PS5: Guia Prático Passo a Passo
### *by ALONSOJR1980*

<div align="center">

[![Firmwares Suportados](https://img.shields.io/badge/Firmwares%20Suportados-1.00%20--%2013.60-success?style=for-the-badge&logo=playstation&logoColor=white)](https://github.com/alonsojr1980/ps5-jailbreak-compendium)
[![Exploit](https://img.shields.io/badge/Exploit%20Principal-Relapse%20%7C%20UMTX-blueviolet?style=for-the-badge&logo=codeforces&logoColor=white)](jailbreak_tech_info.md)
[![Website Online](https://img.shields.io/badge/Website%20Online-GitHub%20Pages-00d2ff?style=for-the-badge&logo=githubpages&logoColor=white)](https://alonsojr1980.github.io/ps5-jailbreak-compendium/)
[![Payloads](https://img.shields.io/badge/Payloads-etaHEN%20%7C%20ps5--kstuff-ff69b4?style=for-the-badge&logo=coffeescript&logoColor=white)](jailbreak_tech_info.md#4-engenharia-de-payloads--frameworks-do-sistema)

**Navegação / Navigation:**
[🔬 Análise Técnica Aprofundada (Tech Info)](jailbreak_tech_info.md) | [🇺🇸 English Version](../en/jailbreak_how_to.md) | [🇪🇸 Versión en Español](../es/jailbreak_how_to.md) | [🌐 Portal Principal](../../README.md)

</div>

Um guia tático, direto e gamificado para realizar o jailbreak no PlayStation 5 nas versões de firmware 1.00 até 13.60, blindar defesas anti-atualização e executar payloads.

---

<!-- GAMIFIED QUEST HUD -->
<div class="ps-quest-hud" id="psQuestHud">
  <div class="ps-hud-header">
    <div class="ps-hud-title-wrap">
      <div class="ps-hud-rank-icon" id="psRankIcon">🎮</div>
      <div>
        <div class="ps-hud-title">Campanha: Protocolo Jailbreak PS5</div>
        <div class="ps-hud-subtitle">Complete as missões para libertar o firmware e conquistar Troféus PlayStation</div>
      </div>
    </div>
    <div class="ps-hud-stats">
      <div class="ps-hud-stat-pill">
        <span>🏆 TROFÉUS:</span>
        <span id="psTrophiesCount">0 / 5</span>
      </div>
      <div class="ps-hud-stat-pill">
        <span>⚡ XP:</span>
        <span id="psProgressPct">0%</span>
      </div>
    </div>
  </div>

  <div class="ps-progress-bar-container">
    <div class="ps-progress-bar-fill" id="psProgressFill"></div>
  </div>

  <div class="ps-hud-footer">
    <div><span>△</span> Inspecionar missão &bull; <span>◯</span> Concluir & Resgatar Troféu &bull; <span>✕</span> Executar</div>
    <div class="ps-hud-controls">
      <button class="ps-btn-hud" onclick="toggleAllSteps(true)">📂 Expandir Tudo</button>
      <button class="ps-btn-hud" onclick="toggleAllSteps(false)">📁 Recolher Tudo</button>
      <button class="ps-btn-hud" onclick="resetAllQuests()">🔄 Reiniciar Campanha</button>
    </div>
  </div>
</div>

<!-- MISSÃO 0 -->
<details class="step-tile" data-quest="quest-step-0" open>
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISSÃO 0</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🎯 Reconhecimento de Alvo: Identificação de Firmware</span>
      <span class="step-tile-desc">Identifique a versão do software do sistema (1.00 – 13.60) e confira a compatibilidade</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">RECON</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DA MISSÃO:</strong> Localizar a versão exata do software do sistema no console e confirmar a faixa de compatibilidade do exploit.
</div>

### 🎒 Equipamento Necessário
- Console PS5 & Controle DualSense
- TV / Monitor

### ⚡ Execução Tática
1. Ligue o console e acesse **Configurações ➔ Sistema ➔ Software do Sistema ➔ Informações do Console**.
2. Observe a linha **Software do Sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Os primeiros 4 dígitos indicam o firmware: ex. `07.61`, `04.50`, `13.60`).

### 📊 Matriz de Compatibilidade de Firmware

| Faixa de Firmware | Status do Exploit | Vetor Tático de Ataque |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **Root de Hypervisor** | [Byepervisor / IPv6 UAF](#método-c-firmwares-iniciais-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **Estabilidade Máxima** | [IPv6 Socket UAF / UMTX](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **Altamente Estável** | [Exploit UMTX](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **Port em Andamento** | [UMTX2 / Mast1c0re](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **Era Moderna** | [Exploit Relapse (aio_multi_wait)](#método-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **Corrigido** | Mantenha o console **totalmente offline**. **Não atualize!** |

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥉 Troféu de Bronze &bull; <em>"Especialista em Reconhecimento"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-0" data-todo-text="Marcar Concluída" data-done-text="Missão Concluída" onclick="toggleQuest('quest-step-0', 'Especialista em Reconhecimento', 'Troféu de Bronze', '🎯')">
    <span>◯</span> Marcar Concluída
  </button>
</div>

</details>

<!-- MISSÃO 1 -->
<details class="step-tile" data-quest="quest-step-1">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISSÃO 1</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🛡️ Protocolo de Defesa: Blindagem Anti-Atualização</span>
      <span class="step-tile-desc">Bloqueie a telemetria da Sony e ative o firewall antes de conectar à rede</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">OBRIGATÓRIO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DA MISSÃO:</strong> Bloquear downloads acidentais de software do sistema em segundo plano para proteger o console contra atualizações irreversíveis.
</div>

### 🎒 Equipamento Necessário
- Configurações do Sistema no Console
- Roteador / Pi-hole / AdGuard (Camada extra recomendada)

### ⚡ Execução Tática: Blindagem no Console
- [x] **Configurações ➔ Sistema ➔ Software do Sistema ➔ Atualizações e Configurações do Software do Sistema**:
  - Desative **Baixar Arquivos de Atualização Automaticamente**.
  - Desative **Instalar Arquivos de Atualização Automaticamente**.
- [x] **Configurações ➔ Sistema ➔ Economia de Energia ➔ Recursos Disponíveis no Rest Mode**:
  - Desative **Continuar Conectado à Internet**.
- [x] **Configurações ➔ Dados Salvos e Configurações de Jogos/Aplicativos ➔ Atualizações Automáticas**:
  - Desative **Download Automático**.
  - Desative **Instalação Automática no Rest Mode**.

### 🌐 Lista Negra de Domínios para Roteador / Pi-hole
Adicione estes domínios da Sony à lista de bloqueio da rede:

```text
fus01.ps5.update.playstation.net
fuk01.ps5.update.playstation.net
feu01.ps5.update.playstation.net
fjp01.ps5.update.playstation.net
fkr01.ps5.update.playstation.net
fcn01.ps5.update.playstation.net
ps5.update.playstation.net
telemetry.api.playstation.com
telemetry-ingest.api.playstation.com
```

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥉 Troféu de Bronze &bull; <em>"Sentinela de Rede"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-1" data-todo-text="Marcar Concluída" data-done-text="Missão Concluída" onclick="toggleQuest('quest-step-1', 'Sentinela de Rede', 'Troféu de Bronze', '🛡️')">
    <span>◯</span> Marcar Concluída
  </button>
</div>

</details>

<!-- AVISO CRÍTICO / CHEFÃO -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">PERIGO</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚠️ Armadilha do Leitor Removível do PS5 Slim & Pro</span>
      <span class="step-tile-desc">NÃO conecte à PSN para registrar o leitor removível em firmware explorável</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">ARMADILHA</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>⚠️ INTEL DE PERIGO:</strong> O leitor de disco removível requer um <strong>Handshake</strong> criptográfico único com os servidores da Sony para ser ativado e vinculado à placa-mãe.
</div>

> [!CAUTION]
> - **A Armadilha**: Se o seu console estiver em firmware suscetível a jailbreak (<= 13.60), conectar à PSN para registrar o leitor **forçará uma atualização irreversível para o firmware mais recente**, eliminando permanentemente a capacidade de jailbreak.
> - **Regra Operacional**: Se o leitor ainda não foi registrado, **não atualize**. Backups digitais, homebrew, emuladores e armazenamento em SSD M.2 funcionam 100% sem o leitor pareado.

</details>

<!-- MISSÃO 2 -->
<details class="step-tile" data-quest="quest-step-2">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISSÃO 2</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚔️ Infiltração: Execução do Exploit & Kernel RW</span>
      <span class="step-tile-desc">Dispare o spray de WebKit e a race de aio_multi_wait para abrir a Porta 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">KERNEL BREACH</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DA MISSÃO:</strong> Conquistar primitivas arbitrárias de Kernel Read/Write e iniciar o listener do <code>elfldr</code> na <strong>Porta 9021</strong>.
</div>

### 🎒 Equipamento Necessário
- DNS do Exploit: `45.56.67.85` (Relapse) ou `62.210.38.117` (UMTX)
- Navegador do Guia do Usuário no PS5

### ⚡ Execução Tática: Selecione o Vetor do seu Firmware

#### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)
1. Acesse **Configurações ➔ Rede ➔ Configurações ➔ Configurar Conexão com a Internet**.
2. Selecione sua conexão, pressione **Opções (☰)** ➔ **Configurações Avançadas**:
   - **Configurações de DNS**: `Manual`
   - **DNS Primário**: `45.56.67.85`
   - **DNS Secundário**: `0.0.0.0` (ou `62.210.38.117`)
3. Salve e teste a conexão (*Internet: Êxito*; *PSN: Falhou* — normal e seguro).
4. Abra **Configurações ➔ Sistema ➔ Guia do Usuário, Segurança e Saúde ➔ Guia do Usuário**.
5. O host do Relapse executa o heap spray no WebKit seguido pela race condition do `aio_multi_wait`.
6. Aguarde a confirmação:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Se o console desligar repentinamente, ocorreu um **Kernel Panic**. Aguarde 30 segundos, ligue no botão físico de energia, aguarde a verificação de armazenamento e repita o exploit.

---

#### Método B: Firmwares Estáveis 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)
1. Configure o **DNS Primário** para `62.210.38.117` ou `165.227.83.145`.
2. Abra **Configurações ➔ Sistema ➔ Guia do Usuário**.
3. Selecione **IPv6 UAF** (para 3.00–4.51) ou **UMTX Exploit** (para 5.00–5.50).
4. O exploit é concluído em instantes e ativa o `elfldr` na Porta 9021.

---

#### Método C: Firmwares Iniciais 1.00 – 2.50 (Byepervisor)
1. Carregue o exploit via Guia do Usuário ou disco Blu-ray com BD-JB.
2. Injete o **Byepervisor** para assumir o controle total do Hypervisor (Ring -1).

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥈 Troféu de Prata &bull; <em>"Perímetro Invadido"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-2" data-todo-text="Marcar Concluída" data-done-text="Missão Concluída" onclick="toggleQuest('quest-step-2', 'Perímetro Invadido', 'Troféu de Prata', '⚔️')">
    <span>◯</span> Marcar Concluída
  </button>
</div>

</details>

<!-- MISSÃO 3 -->
<details class="step-tile" data-quest="quest-step-3">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISSÃO 3</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚡ Sobrecarga de Energia: Injeção de Payloads</span>
      <span class="step-tile-desc">Injete o etaHEN e o ps5-kstuff via USB autoloader ou Netcat na porta 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">INJEÇÃO DE PAYLOADS</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DA MISSÃO:</strong> Transmitir e executar os payloads essenciais (<code>etaHEN</code> &amp; <code>ps5-kstuff</code>) para desabilitar travas de segurança e habilitar homebrew.
</div>

### 🎒 Equipamento Necessário
- Pendrive USB formatado em **exFAT** (Opção 1) OU Terminal de PC com Netcat / PowerShell (Opção 2)
- Binários dos Payloads: `etaHEN.bin`, `ps5-kstuff.bin`

### ⚡ Execução Tática: Métodos de Injeção

#### Opção 1: Carregamento Automático por USB (Recomendado)
1. Formate um pendrive USB em **exFAT** com esquema de partição MBR.
2. Crie uma pasta chamada `payloads` na raiz do pendrive:
   ```text
   Pendrive USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecte o pendrive em uma das **portas USB 3.0 traseiras** do console.
4. Ao acionar o exploit no navegador, o loader detecta e executa os payloads da unidade USB automaticamente!

---

#### Opção 2: Injeção via Rede pelo Terminal (Netcat)
Envie os binários do seu computador para o IP do PS5 na **Porta 9021**:

```bash
# No Linux / macOS / WSL:
nc -w 3 <IP_DO_PS5> 9021 < etaHEN.bin
nc -w 3 <IP_DO_PS5> 9021 < ps5-kstuff.bin
```

```powershell
# No Windows (PowerShell):
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[SUCESSO] etaHEN implantado no PS5!"
```

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🥇 Troféu de Ouro &bull; <em>"Soberano do Kernel"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-3" data-todo-text="Marcar Concluída" data-done-text="Missão Concluída" onclick="toggleQuest('quest-step-3', 'Soberano do Kernel', 'Troféu de Ouro', '⚡')">
    <span>◯</span> Marcar Concluída
  </button>
</div>

</details>

<!-- MISSÃO 4 -->
<details class="step-tile" data-quest="quest-step-4">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">MISSÃO 4</span>
    <span class="step-tile-text">
      <span class="step-tile-title">👑 Libertação Total: Homebrew e Backups</span>
      <span class="step-tile-desc">Ative o etaHEN Toolbox, servidor FTP porta 1337, Itemzflow e Apollo Save Tool</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">ROOT LIBERADO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🎯 OBJETIVO DA MISSÃO:</strong> Estabelecer o ecossistema completo de homebrew e gerenciamento de backups de jogos no console desbloqueado.
</div>

### 🎒 Equipamento Necessário
- Cliente FTP (FileZilla / WinSCP)
- Pacotes Homebrew: `Itemzflow.pkg`, `Apollo.pkg`

### ⚡ Execução Tática
1. **Verificar etaHEN Toolbox**:
   - Abra **Configurações ➔ Sistema**.
   - Confirme a presença do novo menu **etaHEN Toolbox**.
2. **Acessar Servidor FTP de Alta Velocidade**:
   - O etaHEN vincula automaticamente um daemon de FTP à **Porta 1337**.
   - Conecte via FileZilla / WinSCP com credenciais anônimas.
3. **Executar o Itemzflow (Game Manager)**:
   - Instale o `Itemzflow.pkg` e abra-o na tela inicial.
   - Faça o dump de discos físicos e compras digitais para um HD externo USB ou SSD M.2 interno.
   - Execute backups diretamente do armazenamento externo USB sem necessidade de cópia interna.
4. **Gerenciar Saves com Apollo Save Tool**:
   - Exporte, importe e reassine saves entre contas da PSN de forma totalmente offline.

<div class="quest-action-bar">
  <div class="quest-reward-pill">
    <span>🏆 RECOMPENSA:</span> 🏆 Troféu de Platina &bull; <em>"Mestre Absoluto do Root"</em> (+20% XP)
  </div>
  <button class="quest-complete-btn" data-quest="quest-step-4" data-todo-text="Marcar Concluída" data-done-text="Missão Concluída" onclick="toggleQuest('quest-step-4', 'Mestre Absoluto do Root', 'Troféu de Platina', '👑')">
    <span>◯</span> Marcar Concluída
  </button>
</div>

</details>

<!-- RESPAWN / RECUPERAÇÃO -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">RESPAWN</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🚑 Diagnóstico & Ponto de Recuperação de Panics</span>
      <span class="step-tile-desc">Recuperação de Kernel Panics, estouros de memória, desync de DNS e erros CE-xxxx</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">CHECKPOINT</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

<div class="mission-brief">
  <strong>🚑 INTEL DE RESPAWN:</strong> Disputas de temporização (race conditions) no exploit podem provocar Kernel Panics inofensivos. Consulte esta tabela para retomar o controle imediatamente.
</div>

| Sintoma de Campo | Causa-Raiz | Solução Imediata |
| :--- | :--- | :--- |
| **Tela preta instantânea / Desligamento** | Kernel Panic durante a disputa temporal da race condition | Aguarde 30s. Pressione o botão físico de energia. Aguarde a checagem de armazenamento e reinicie o exploit. |
| **"Memória do sistema insuficiente"** | Estouro de heap no WebKit durante o heap grooming | Pressione `OK`, recarregue a página ou limpe os cookies do navegador nas configurações. |
| **Guia do Usuário abre a página da Sony** | Desync de DNS ou roteador ignorando DNS manual | Revise as Configurações de Rede; garanta que o DNS Primário seja `45.56.67.85` e o Secundário seja `0.0.0.0`. |
| **Conexão Recusada na porta 9021** | O estágio 2 falhou ou o `elfldr` travou | Reabra o Guia do Usuário até que a notificação de confirmação da porta 9021 seja exibida. |
| **Jogos não iniciam com erro CE-xxxx** | Payload `ps5-kstuff` não carregado na memória | Certifique-se de que o `kstuff` ou `etaHEN` foi injetado antes de iniciar os jogos. |

</details>

---

<p align="center">
  <b>Precisa de detalhes técnicos aprofundados, primitivas de memória, syscalls ou portas de rede?</b><br>
  👉 Leia o guia complementar: <b><a href="jailbreak_tech_info.md">PS5 Jailbreak: Análise Técnica Aprofundada (Tech Info)</a></b>
</p>
