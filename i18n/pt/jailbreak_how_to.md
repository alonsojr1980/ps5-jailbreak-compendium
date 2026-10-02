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

Um guia direto, prático e objetivo para realizar o jailbreak no PlayStation 5 nas diferentes faixas de firmware, configurar o firewall anti-atualização e injetar os payloads essenciais.

---

## 📋 Painel Interativo Passo a Passo

Clique em qualquer bloco abaixo para expandir e ver as instruções detalhadas, checklists e comandos.

<div class="step-toolbar">
  <button class="step-toolbar-btn" onclick="toggleAllSteps(true)"><span>📂</span> Expandir Todos os Passos</button>
  <button class="step-toolbar-btn" onclick="toggleAllSteps(false)"><span>📁</span> Recolher Todos os Passos</button>
</div>

<!-- PASSO 0 -->
<details class="step-tile" open>
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 0</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🔍 Descobrir o Firmware do seu Console</span>
      <span class="step-tile-desc">Identifique a versão exata do software do sistema (1.00 – 13.60) e confira a compatibilidade</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">COMPATIBILIDADE</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

### 🔍 Como Identificar o Firmware
1. Ligue o console e acesse **Configurações ➔ Sistema ➔ Software do Sistema ➔ Informações do Console**.
2. Observe a linha **Software do Sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Os 4 primeiros dígitos indicam o firmware, por exemplo, `07.61`, `04.50` ou `13.60`).

### Verificação Rápida de Compatibilidade

| Firmware | Posso Fazer Jailbreak? | Método de Exploit Recomendado |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **SIM** (Root de Hypervisor) | [Byepervisor / IPv6 UAF](#método-c-firmwares-iniciais-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **SIM** (Estabilidade Máxima) | [IPv6 Socket UAF / UMTX](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **SIM** (Altamente Estável) | [Exploit UMTX](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **SIM** (Port em Andamento) | [UMTX2 / Mast1c0re](#método-b-firmwares-estáveis-300--451--500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **SIM** (Era Moderna) | [Exploit Relapse (aio_multi_wait)](#método-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **NÃO** (Corrigido) | Mantenha o console **totalmente offline**. **Não atualize!** |

</details>

<!-- PASSO 1 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 1</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🛡️ Blindagem Pré-Jailbreak & Firewall Anti-Atualização</span>
      <span class="step-tile-desc">Bloqueie atualizações automáticas nas configurações do sistema e no DNS/Roteador</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">OBRIGATÓRIO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Atualizações automáticas em segundo plano anulam permanentemente a possibilidade de jailbreak. Aplique estas configurações antes de conectar o console a qualquer rede:

### 1. Checklist de Configurações no Console
- [x] **Configurações ➔ Sistema ➔ Software do Sistema ➔ Atualizações e Configurações do Software do Sistema**:
  - Desative **Baixar Arquivos de Atualização Automaticamente**.
  - Desative **Instalar Arquivos de Atualização Automaticamente**.
- [x] **Configurações ➔ Sistema ➔ Economia de Energia ➔ Recursos Disponíveis no Rest Mode**:
  - Desative **Continuar Conectado à Internet**.
- [x] **Configurações ➔ Dados Salvos e Configurações de Jogos/Aplicativos ➔ Atualizações Automáticas**:
  - Desative **Download Automático**.
  - Desative **Instalação Automática no Rest Mode**.

### 2. Blocklist de Domínios para Roteador / Pi-hole / AdGuard
Adicione estes domínios da Sony à lista de bloqueio do seu roteador ou servidor DNS local:

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

</details>

<!-- AVISO CRÍTICO -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number warning">AVISO</span>
    <span class="step-tile-text">
      <span class="step-tile-title">⚠️ Aviso Crítico sobre o Leitor Removível do PS5 Slim & Pro</span>
      <span class="step-tile-desc">NÃO atualize o console para realizar o pareamento do leitor de disco</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag warning">AVISO CRÍTICO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

> [!CAUTION]
> Se o seu console é um **PS5 Slim (CFI-2000)** ou **PS5 Pro (CFI-7000)** com leitor de disco removível:
> - O leitor exige um **Handshake** criptográfico único com os servidores da Sony para ser ativado e vinculado à placa-mãe.
> - **A Armadilha**: Se o console estiver em um firmware explorável (<= 13.60), conectar à PSN para registrar o leitor **forçará uma atualização irreversível para o firmware mais recente**.
> - **Regra**: Se o leitor ainda não foi registrado, **não atualize**. Backups digitais de jogos, homebrew, emuladores e armazenamento em SSD M.2 funcionam 100% sem o leitor físico pareado.

</details>

<!-- PASSO 2 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 2</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🎮 Execução do Jailbreak por Faixa de Firmware</span>
      <span class="step-tile-desc">Acione o exploit para 7.00–13.60 (Relapse), 3.00–5.50 (UMTX) ou 1.00–2.50</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">TRIGGER EXPLOIT</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Selecione o procedimento correspondente à versão de firmware do seu aparelho:

### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)

Compatível com todos os modelos de PS5 (Fat, Slim e Pro) nos firmwares 7.00 até 13.60.

#### 1. Configurar Conexão com DNS Customizado
1. Acesse **Configurações ➔ Rede ➔ Configurações ➔ Configurar Conexão com a Internet**.
2. Selecione sua rede Wi-Fi ou Cabo LAN, pressione **Opções (☰)** ➔ **Configurações Avançadas**.
3. Configure os seguintes parâmetros:
   - **Configurações de Endereço IP**: `Automático`
   - **Nome do Host DHCP**: `Não Especificar`
   - **Configurações de DNS**: `Manual`
     - **DNS Primário**: `45.56.67.85`
     - **DNS Secundário**: `0.0.0.0` (ou `62.210.38.117`)
   - **Servidor Proxy**: `Não Usar`
   - **Configurações MTU**: `Automático`
4. Salve e execute o teste de conexão. *Conexão à Internet: Êxito*; *PlayStation Network: Falhou* (Esperado e seguro).

#### 2. Disparar o Exploit
1. Acesse **Configurações ➔ Sistema ➔ Guia do Usuário, Segurança e Saúde ➔ Guia do Usuário**.
2. O navegador interno será redirecionado para a página do exploit Relapse.
3. O exploit de WebKit será acionado automaticamente (executando heap spray na memória do JavaScriptCore).
4. O exploit de kernel será acionado explorando a race condition de `aio_multi_wait`.
5. Aguarde a mensagem de confirmação:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Se o console travar ou desligar repentinamente com tela preta, ocorreu um **Kernel Panic**. Aguarde 30 segundos, ligue o console pelo botão físico de energia, aguarde a verificação de armazenamento e tente novamente.

---

### Método B: Firmwares Estáveis 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)

Faixa com estabilidade máxima (taxa de sucesso próxima de 100%).

1. Configure o **DNS Primário** do PS5 para `62.210.38.117` (EchoStretch) ou `165.227.83.145` (Al-Azif).
2. Abra **Configurações ➔ Sistema ➔ Guia do Usuário**.
3. Selecione o exploit correspondente:
   - Para **3.00 – 4.51**: Escolha **IPv6 UAF** ou **UMTX**.
   - Para **5.00 – 5.50**: Escolha **UMTX Exploit**.
4. O exploit conclui a execução em poucos segundos e inicia o daemon `elfldr` na porta 9021.

---

### Método C: Firmwares Iniciais 1.00 – 2.50 (Byepervisor)

A faixa mais privilegiada de todo o ecossistema, com controle completo de Hypervisor (Ring -1).

1. Acesse a página de exploit pelo Guia do Usuário ou via disco Blu-ray com BD-JB.
2. Dispare o exploit de kernel e injete o payload **Byepervisor**.
3. O Byepervisor assume o controle do Hypervisor do PS5, permitindo leitura e escrita arbitrária no hypervisor, bypass de checagem de assinatura de código e descriptografia de memória RAM.

</details>

<!-- PASSO 3 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 3</span>
    <span class="step-tile-text">
      <span class="step-tile-title">📦 Injeção de Payloads (etaHEN & ps5-kstuff)</span>
      <span class="step-tile-desc">Carregue o framework homebrew via USB autoloader ou Netcat na porta 9021</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">INJEÇÃO DE PAYLOADS</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Assim que o daemon `elfldr` estiver aguardando conexões na **porta 9021**, injete os payloads:

### Opção 1: Carregamento Automático via USB (Recomendado)

1. Formate um pendrive USB em **exFAT** (tabela de partição MBR).
2. Crie uma pasta chamada `payloads` na raiz do pendrive:
   ```text
   Pendrive USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecte o pendrive em uma das portas USB 3.0 traseiras do PS5.
4. Ao acionar o exploit no navegador, o loader detecta e executa os payloads da unidade USB automaticamente!

---

### Opção 2: Injeção via Rede pelo Terminal (Netcat)

Caso prefira enviar os binários a partir do seu computador pela rede local:

#### No Linux / macOS / WSL:
```bash
# Injetar etaHEN (Framework All-In-One para Homebrew)
nc -w 3 <IP_DO_PS5> 9021 < etaHEN.bin

# Injetar ps5-kstuff (se não estiver embutido no etaHEN)
nc -w 3 <IP_DO_PS5> 9021 < ps5-kstuff.bin
```

#### No Windows (PowerShell):
```powershell
$ps5_ip = "192.168.1.150"
$bytes = [System.IO.File]::ReadAllBytes("etaHEN.bin")
$client = New-Object System.Net.Sockets.TcpClient($ps5_ip, 9021)
$stream = $client.GetStream()
$stream.Write($bytes, 0, $bytes.Length)
$stream.Close(); $client.Close()
Write-Host "[SUCESSO] etaHEN enviado ao PS5!"
```

</details>

<!-- PASSO 4 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 4</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🕹️ Instalação de Homebrew & Execução de Backups de Jogos</span>
      <span class="step-tile-desc">Configuração do etaHEN Toolbox, servidor FTP porta 1337, Itemzflow e Apollo Save Tool</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">APPS & HOMEBREW</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

Após a injeção do **etaHEN**:

1. **Acessar o etaHEN Toolbox**:
   - Abra **Configurações ➔ Sistema**.
   - Você verá o novo submenu **etaHEN Toolbox**.
2. **Conectar via Servidor FTP**:
   - O etaHEN inicializa automaticamente um servidor FTP na **porta 1337**.
   - Conecte pelo FileZilla / WinSCP utilizando o IP do console e porta `1337` (login anônimo).
3. **Instalar o Itemzflow (Gerenciador de Jogos)**:
   - Instale o pacote `Itemzflow.pkg` através do instalador nas Configurações ou inicie-o diretamente.
   - Faça o dump de discos físicos ou jogos digitais para um disco rígido USB ou SSD M.2 interno.
   - Execute backups diretamente do armazenamento externo USB sem necessidade de cópia interna.
4. **Gerenciar Saves com Apollo Save Tool**:
   - Exporte, importe e reassine saves entre diferentes contas da PSN de forma totalmente offline.

</details>

<!-- PASSO 5 -->
<details class="step-tile">
<summary class="step-header">
  <span class="step-tile-left">
    <span class="step-tile-number">PASSO 5</span>
    <span class="step-tile-text">
      <span class="step-tile-title">🔧 Resolução Rápida de Problemas & Recuperação de Kernel Panics</span>
      <span class="step-tile-desc">Soluções para tela preta, erros de memória WebKit, desync de DNS e erros CE-xxxx</span>
    </span>
  </span>
  <span class="step-tile-right">
    <span class="step-tile-tag">RECUPERAÇÃO</span>
    <span class="step-tile-chevron">▼</span>
  </span>
</summary>

| Sintoma | Causa-Raiz | Solução Prática |
| :--- | :--- | :--- |
| **Tela preta instantânea / Desligamento** | Kernel Panic durante a disputa temporal da race condition | Aguarde 30 segundos. Pressione o botão físico de ligar. Aguarde a checagem de armazenamento e reinicie o exploit. |
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
