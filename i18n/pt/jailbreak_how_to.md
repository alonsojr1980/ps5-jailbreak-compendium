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

## 📑 Índice

1. [🔍 Passo 0: Descobrir o Firmware do seu Console](#-passo-0-descobrir-o-firmware-do-seu-console)
2. [🛡️ Passo 1: Blindagem Pré-Jailbreak & Firewall Anti-Atualização](#️-passo-1-blindagem-pr%C3%A9-jailbreak--firewall-anti-atualiza%C3%A7%C3%A3o)
3. [⚠️ Aviso Crítico sobre o Leitor Removível do PS5 Slim & Pro](#️-aviso-cr%C3%ADtico-sobre-o-leitor-remov%C3%ADvel-do-ps5-slim--pro)
4. [🎮 Passo 2: Procedimento de Jailbreak por Faixa de Firmware](#-passo-2-procedimento-de-jailbreak-por-faixa-de-firmware)
   - [Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)](#m%C3%A9todo-a-firmwares-modernos-700--1360-exploit-relapse)
   - [Método B: Firmwares Estáveis 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)](#m%C3%A9todo-b-firmwares-est%C3%A1veis-300--451--500--550-umtx--ipv6)
   - [Método C: Firmwares Iniciais 1.00 – 2.50 (Byepervisor)](#m%C3%A9todo-c-firmwares-iniciais-100--250-byepervisor)
5. [📦 Passo 3: Injeção de Payloads (etaHEN & ps5-kstuff)](#-passo-3-inje%C3%A7%C3%A3o-de-payloads-etahen--ps5-kstuff)
   - [Opção 1: Carregamento Automático via USB (Recomendado)](#op%C3%A7%C3%A3o-1-carregamento-autom%C3%A1tico-via-usb-recomendado)
   - [Opção 2: Injeção via Rede com Netcat / Terminal](#op%C3%A7%C3%A3o-2-inje%C3%A7%C3%A3o-via-rede-com-netcat--terminal)
6. [🕹️ Passo 4: Instalação de Homebrew & Execução de Backups de Jogos](#️-passo-4-instala%C3%A7%C3%A3o-de-homebrew--execu%C3%A7%C3%A3o-de-backups-de-jogos)
7. [🔧 Resolução Rápida de Problemas e Recuperação de Kernel Panics](#-resolu%C3%A7%C3%A3o-r%C3%A1pida-de-problemas-e-recupera%C3%A7%C3%A3o-de-kernel-panics)

---

## 🔍 Passo 0: Descobrir o Firmware do seu Console

Antes de iniciar qualquer procedimento, verifique o firmware exato do seu PlayStation 5:

1. Ligue o console e acesse **Configurações ➔ Sistema ➔ Software do Sistema ➔ Informações do Console**.
2. Observe a linha **Software do Sistema**:
   - Formato: `XX.XX-XX.XX.XX.XX-XX.XX` (Os 4 primeiros dígitos indicam o firmware, por exemplo, `07.61`, `04.50` ou `13.60`).

### Verificação Rápida de Compatibilidade

| Firmware | Posso Fazer Jailbreak? | Método de Exploit Recomendado |
| :---: | :---: | :--- |
| **1.00 – 2.50** | ✅ **SIM** (Root de Hypervisor) | [Byepervisor / IPv6 UAF](#m%C3%A9todo-c-firmwares-iniciais-100--250-byepervisor) |
| **3.00 – 4.51** | ✅ **SIM** (Estabilidade Máxima) | [IPv6 Socket UAF / UMTX](#m%C3%A9todo-b-firmwares-est%C3%A1veis-300--451--500--550-umtx--ipv6) |
| **5.00 – 5.50** | ✅ **SIM** (Altamente Estável) | [Exploit UMTX](#m%C3%A9todo-b-firmwares-est%C3%A1veis-300--451--500--550-umtx--ipv6) |
| **6.00 – 6.50** | ⚠️ **SIM** (Port em Andamento) | [UMTX2 / Mast1c0re](#m%C3%A9todo-b-firmwares-est%C3%A1veis-300--451--500--550-umtx--ipv6) |
| **7.00 – 13.60** | ✅ **SIM** (Era Moderna) | [Exploit Relapse (aio_multi_wait)](#m%C3%A9todo-a-firmwares-modernos-700--1360-exploit-relapse) |
| **14.00+** | ❌ **NÃO** (Corrigido) | Mantenha o console **totalmente offline**. **Não atualize!** |

---

## 🛡️ Passo 1: Blindagem Pré-Jailbreak & Firewall Anti-Atualização

Atualizações em segundo plano anulam permanentemente a possibilidade de jailbreak. Configure estas opções antes de conectar o console a qualquer rede:

### 1. Checklist nas Configurações do Console
- [x] **Configurações ➔ Sistema ➔ Software do Sistema ➔ Atualizações e Configurações do Software do Sistema**:
  - Desative **Baixar Arquivos de Atualização Automaticamente**.
  - Desative **Instalar Arquivos de Atualização Automaticamente**.
- [x] **Configurações ➔ Sistema ➔ Economia de Energia ➔ Recursos Disponíveis no Modo de Repouso**:
  - Desative **Continuar Conectado à Internet**.
- [x] **Configurações ➔ Dados Salvos e Configurações de Jogos/Aplicativos ➔ Atualizações Automáticas**:
  - Desative **Download Automático**.
  - Desative **Instalação Automática no Modo de Repouso**.

### 2. Bloqueio de Domínios no Roteador / Pi-hole / AdGuard
Adicione estes domínios de atualização e telemetria da Sony à lista de bloqueio:

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

---

## ⚠️ Aviso Crítico sobre o Leitor Removível do PS5 Slim & Pro

> [!CAUTION]
> Se o seu console for um **PS5 Slim (série CFI-2000)** ou **PS5 Pro (série CFI-7000)** com leitor de discos removível:
> - O leitor exige um **Handshake** criptográfico único com os servidores da Sony para ser ativado e vinculado à placa-mãe.
> - **A Armadilha**: Se o seu console estiver em um firmware com suporte a jailbreak (<= 13.60), conectar-se à PSN para parear o leitor **forçará uma atualização irreversível para o firmware mais recente**.
> - **Regra**: Se o leitor ainda não estiver pareado, **não atualize** para pareá-lo. Backups de jogos digitais, homebrew, emuladores e armazenamento em SSD NVMe M.2 funcionam perfeitamente sem a ativação do leitor físico.

---

## 🎮 Passo 2: Procedimento de Jailbreak por Faixa de Firmware

### Método A: Firmwares Modernos 7.00 – 13.60 (Exploit Relapse)

Cobre todos os consoles PS5 (Fat, Slim e Pro) executando do firmware 7.00 ao 13.60.

#### 1. Configurar Conexão com DNS Personalizado
1. Acesse **Configurações ➔ Rede ➔ Configurações ➔ Configurar Conexão à Internet**.
2. Destaque sua rede (Wi-Fi ou Cabo), pressione **Opções (☰)** ➔ **Configurações Avançadas**.
3. Defina os parâmetros:
   - **Configurações de Endereço IP**: `Automático`
   - **Nome de Host DHCP**: `Não Especificar`
   - **Configurações de DNS**: `Manual`
     - **DNS Primário**: `45.56.67.85`
     - **DNS Secundário**: `0.0.0.0` (ou `62.210.38.117`)
   - **Servidor Proxy**: `Não Usar`
   - **Configurações de MTU**: `Automático`
4. Salve e execute o teste. *Conexão à Internet: Com Êxito*; *PlayStation Network: Com Falha* (Normal e seguro).

#### 2. Disparar o Exploit
1. Abra **Configurações ➔ Sistema ➔ Guia do Usuário, Segurança e Saúde e Outras Informações ➔ Guia do Usuário**.
2. O navegador interno redirecionará automaticamente para o host do exploit Relapse.
3. O exploit WebKit executa sozinho (realizando heap spray na memória do JavaScriptCore).
4. O exploit de kernel é acionado pela condição de corrida em `aio_multi_wait`.
5. Aguarde a confirmação na tela:
   `[+] Kernel RW Obtained! elfldr listening on port 9021...`

> [!TIP]
> Caso o console congele ou desligue repentinamente com tela preta, ocorreu um **Kernel Panic**. Aguarde 30 segundos, ligue o PS5 pelo botão físico, deixe a reparação do armazenamento concluir e tente novamente.

---

### Método B: Firmwares Estáveis 3.00 – 4.51 & 5.00 – 5.50 (UMTX / IPv6)

Estes firmwares oferecem altíssima estabilidade (taxa de sucesso próxima de 100%).

1. Defina o **DNS Primário** para `62.210.38.117` (EchoStretch) ou `165.227.83.145` (Al-Azif).
2. Abra **Configurações ➔ Sistema ➔ Guia do Usuário**.
3. Selecione o exploit:
   - Para **3.00 – 4.51**: Escolha **IPv6 UAF** ou **UMTX**.
   - Para **5.00 – 5.50**: Escolha **UMTX Exploit**.
4. O exploit conclui em segundos, ativando o `elfldr` na Porta 9021.

---

### Método C: Firmwares Iniciais 1.00 – 2.50 (Byepervisor)

A faixa de firmware mais privilegiada da história do console, com controle total de Hypervisor (Ring -1).

1. Acesse o host pelo Guia do Usuário ou via disco Blu-ray com BD-JB.
2. Execute o exploit de kernel e injete o payload **Byepervisor**.
3. O Byepervisor derrota as proteções do Hypervisor do PS5, liberando leitura/escrita bare-metal, descriptografia de RAM e desativação total de checagens de código.

---

## 📦 Passo 3: Injeção de Payloads (etaHEN & ps5-kstuff)

Com o `elfldr` aguardando conexões na **Porta 9021**, injete os payloads principais:

### Opção 1: Carregamento Automático via USB (Recomendado)

1. Formate um pendrive em **exFAT** (partição MBR).
2. Crie uma pasta chamada `payloads` na raiz da unidade:
   ```text
   Pendrive USB (exFAT):
   └── payloads/
       ├── etaHEN.bin
       └── ps5-kstuff.bin
   ```
3. Conecte o pendrive em uma porta USB traseira do PS5.
4. Ao acionar o exploit, os payloads contidos na pasta serão detectados e executados automaticamente!

---

### Opção 2: Injeção via Rede com Netcat / Terminal

Para enviar arquivos do seu computador pela rede local:

#### No Linux / macOS / WSL:
```bash
# Injetar etaHEN (Homebrew Enabler completo)
nc -w 3 <IP_DO_PS5> 9021 < etaHEN.bin

# Injetar ps5-kstuff (se não integrado no etaHEN)
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

---

## 🕹️ Passo 4: Instalação de Homebrew & Execução de Backups de Jogos

Após injetar o **etaHEN**:

1. **Acessar o etaHEN Toolbox**:
   - Abra **Configurações ➔ Sistema**.
   - Você verá a nova opção **etaHEN Toolbox**.
2. **Conectar ao Servidor FTP**:
   - O etaHEN inicializa um servidor FTP na **Porta 1337**.
   - Conecte pelo FileZilla ou WinSCP usando o IP do PS5 na porta `1337` (login Anônimo).
3. **Usar o Itemzflow (Gerenciador de Jogos)**:
   - Instale o pacote `Itemzflow.pkg` ou inicie-o diretamente.
   - Faça dump de discos físicos ou jogos digitais para um HD externo USB ou SSD NVMe M.2.
   - Execute backups diretamente do armazenamento USB sem copiar para a memória interna.
4. **Gerenciar Saves com Apollo Save Tool**:
   - Exporte, importe e reatribua saves de jogos entre diferentes contas offline.

---

## 🔧 Resolução Rápida de Problemas e Recuperação de Kernel Panics

| Problema | Causa Raiz | Solução |
| :--- | :--- | :--- |
| **Tela preta imediata / desligamento** | Kernel Panic na condição de corrida do exploit | Aguarde 30 segundos. Ligue pelo botão físico do PS5. Conclua a reparação do armazenamento e tente de novo. |
| **"Não há memória de sistema livre suficiente"** | Falha de alocação de memória no WebKit | Pressione `OK`, atualize a página ou limpe o cache do navegador nas configurações. |
| **Guia do Usuário abre a página da Sony** | Dessincronia de DNS ou roteador ignorando DNS | Revise as Configurações de Rede; confira se o DNS Primário é `45.56.67.85` e o Secundário é `0.0.0.0`. |
| **Conexão Recusada na Porta 9021** | A fase de kernel falhou ou o `elfldr` fechou | Reabra o Guia do Usuário até surgir a mensagem "Listening on 9021". |
| **Jogos fecham com erro CE-xxxx** | Payload `ps5-kstuff` não foi carregado | Certifique-se de que o `kstuff` ou `etaHEN` foi carregado antes de abrir jogos. |

---

<p align="center">
  <b>Deseja detalhes técnicos profundos, primitivas de memória, chamadas de sistema e portas de rede?</b><br>
  👉 Leia o guia técnico complementar: <b><a href="jailbreak_tech_info.md">Jailbreak do PS5: Análise Técnica Aprofundada (Tech Info)</a></b>
</p>
