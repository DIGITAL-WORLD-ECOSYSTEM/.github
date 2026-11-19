# DIGITAL WORLD ECOSYSTEM
### Arquitetura Soberana • Infraestrutura DePIN • Governança Descentralizada

Bem-vindo ao **DIGITAL WORLD ECOSYSTEM**, ecossistema tecnológico integrado da **ASPPIBRA-DAO** projetado para assegurar autonomia local, coordenação global, custódia descentralizada e liquidação em blockchain.

---

## 🏛️ Diagrama Arquitetural Oficial — Os 4 Pilares do Ecossistema

```mermaid
flowchart TD
    %% Estilos Globais
    classDef rootStyle fill:#1e293b,stroke:#38bdf8,stroke-width:3px,color:#ffffff,font-weight:bold;
    classDef pilarDevOS fill:#0f172a,stroke:#3b82f6,stroke-width:2px,color:#ffffff;
    classDef pilarCloud fill:#0f172a,stroke:#f59e0b,stroke-width:2px,color:#ffffff;
    classDef pilarIPFS fill:#0f172a,stroke:#06b6d4,stroke-width:2px,color:#ffffff;
    classDef pilarBC fill:#0f172a,stroke:#10b981,stroke-width:2px,color:#ffffff;
    classDef funcBox fill:#1e293b,stroke:#475569,stroke-width:1px,color:#f8fafc;

    %% Nó Raiz
    ROOT["🏛️ ASPPIBRA-DAO<br><b>ECOSSISTEMA DIGITAL INTEGRADO</b>"]:::rootStyle

    %% Quatro Pilares Principais
    subgraph S_PILAR1 ["🖥️ PILAR 01: AUTONOMIA LOCAL"]
        P1["<b>DEVOS DESKTOP</b><br>Custódia Soberana & Execução Offline"]:::pilarDevOS
        F1_1["🔐 <b>Cofre Criptográfico (Vault)</b><br>• Sementes BIP-39 / Secp256k1<br>• Encriptação Argon2id + AES-GCM<br>• Limpeza de RAM (zeroize)"]:::funcBox
        F1_2["📄 <b>Motor Typst Soberano</b><br>• Compilação nativa em PDF<br>• Certidões e laudos offline<br>• Hash SHA-256 imediato"]:::funcBox
        F1_3["💾 <b>SQLite Local (WAL)</b><br>• devos_vault.sqlite (Identidades)<br>• real_estate.sqlite (Territorial)"]:::funcBox
        F1_4["🎛️ <b>Edições Especializadas</b><br>• DevOS Node (Serviço DePIN)<br>• DevOS Cockpit (Gestão/Auditoria)"]:::funcBox
    end

    subgraph S_PILAR2 ["☁️ PILAR 02: COORDENAÇÃO GLOBAL"]
        P2["<b>ASPPIBRA CLOUD</b><br>Cloudflare Edge Mesh"]:::pilarCloud
        F2_1["⚡ <b>Gateway de Borda (Workers)</b><br>• Roteamento global de APIs<br>• Latência ultrabaixa distribuída"]:::funcBox
        F2_2["📊 <b>Estado Relacional (D1)</b><br>• Catálogo global de entidades<br>• Livro-razão contábil de dupla entrada"]:::funcBox
        F2_3["📦 <b>Armazenamento R2</b><br>• Distribuição de anexos transitórios<br>• URLs pré-assinadas temporárias"]:::funcBox
        F2_4["🛡️ <b>Guarda Ed25519 Anti-Replay</b><br>• Validação criptográfica de nós<br>• Controle estrito de nonces"]:::funcBox
    end

    subgraph S_PILAR3 ["🌐 PILAR 03: REDE P2P & CUSTÓDIA"]
        P3["<b>IPFS + DePIN</b><br>Armazenamento Descentralizado"]:::pilarIPFS
        F3_1["🏷️ <b>Endereçamento por CID</b><br>• CIDs criptográficos imutáveis<br>• Independência de servidores centrais"]:::funcBox
        F3_2["⚖️ <b>Prova de Custódia (ADR-012)</b><br>• Desafio Storage Proof local<br>• Comprovação matemática de posse"]:::funcBox
        F3_3["📡 <b>Malha Gossip P2P</b><br>• Difusão distribuída de dados<br>• Sincronização resiliente entre nós"]:::funcBox
    end

    subgraph S_PILAR4 ["⛓️ PILAR 04: CONSENSO & LIQUIDAÇÃO"]
        P4["<b>BLOCKCHAIN EVM</b><br>Execução Autônoma On-Chain"]:::pilarBC
        F4_1["💰 <b>Infraestrutura Financeira</b><br>• Token nativo ASPPBR<br>• Redes Arbitrum, Polygon, BSC<br>• Liquidação atômica e pagamentos"]:::funcBox
        F4_2["🗳️ <b>Governança Descentralizada</b><br>• ASPPIBRA-DAO On-Chain<br>• Votações de propostas e quórum<br>• Execução de parâmetros via Smart Contracts"]:::funcBox
        F4_3["📜 <b>Notarização Digital</b><br>• Ancoragem de CIDs e hashes SHA-256<br>• Prova irrefutável de anterioridade"]:::funcBox
    end

    %% Conexões do Topo
    ROOT --> P1
    ROOT --> P2
    ROOT --> P3
    ROOT --> P4

    %% Derivações Internas dos Pilares
    P1 --> F1_1
    P1 --> F1_2
    P1 --> F1_3
    P1 --> F1_4

    P2 --> F2_1
    P2 --> F2_2
    P2 --> F2_3
    P2 --> F2_4

    P3 --> F3_1
    P3 --> F3_2
    P3 --> F3_3

    P4 --> F4_1
    P4 --> F4_2
    P4 --> F4_3

    %% Fluxos de Integração Cruzada
    F1_2 -.->|Publica Documento| F3_1
    F1_1 -.->|Assina Transação| F4_1
    F3_1 -.->|Ancoragem de CID| F4_3
    F4_2 -.->|Eventos On-Chain| F2_2
    F2_1 -.->|Sincronização Global| F1_4
```

---

## 🧩 Detalhamento dos 4 Pilares e suas Derivações

### 🖥️ PILAR 01: DEVOS DESKTOP — Autonomia Local & Custódia Soberana
> *Ambiente nativo para execução offline, custódia e emissão probatória.*

* **Cofre Criptográfico de Chaves (Zero-Trust Local):**
  * Derivação hierárquica determinística BIP-39/BIP-44 (`m/44'/60'/0'/0/x` para EVM e Ed25519 para a rede).
  * Encriptação local em repouso com **Argon2id + AES-256-GCM**.
  * Limpeza estrita de memória RAM após uso (`zeroize`). As chaves privadas **nunca** deixam o dispositivo.
* **Motor de Documentação Soberana (Typst Engine):**
  * Compilação local, nativa e determinística de relatórios periciais e certidões imobiliárias em PDF.
  * Cálculo instantâneo do hash **SHA-256** do documento gerado para vinculação à blockchain.
* **Persistência Relacional Segregada (SQLite WAL):**
  * `devos_vault.sqlite`: Cofre de credenciais, identidades e configurações críticas locais.
  * `real_estate.sqlite`: Base cadastral territorial e registros geoespaciais.
* **Edições Especializadas:**
  * **DevOS Node:** Execução em segundo plano para provimento de nós DePIN, rotinas e serviços de rede.
  * **DevOS Cockpit:** Interface gráfica para governança executiva, auditoria territorial e assinatura de lotes.

---

### ☁️ PILAR 02: ASPPIBRA CLOUD — Coordenação Global & Serviços de Borda
> *Malha de borda global serverless para roteamento e catálogo institucional.*

* **Gateway Distribuído de Borda (Cloudflare Workers / Hono):**
  * Roteamento de APIs em escala global com latência ultrabaixa e alta resiliência.
* **Registro de Estado e Livro-Razão (Cloudflare D1):**
  * Catálogo de entidades públicas, dispositivos e metadados institucionais.
  * Livro-razão contábil de dupla entrada (`financial_ledger_entries`) auditável.
* **Armazenamento Seguro de Anexos (Cloudflare R2):**
  * Distribuição transitória de objetos via URLs pré-assinadas com expiração programada.
* **Guarda de Dispositivos & Anti-Replay (`devosDeviceGuard`):**
  * Validação criptográfica de assinaturas Ed25519 enviadas pelos nós Desktop, com verificação de *nonces* atômicos para proteção contra repetição.

---

### 🌐 PILAR 03: IPFS + DePIN — Rede P2P & Custódia Verificável
> *Camada descentralizada de armazenamento para documentos e metadados imutáveis.*

* **Endereçamento Imutável por Conteúdo (CIDs):**
  * Arquivos identificados univocamente por seu conteúdo criptográfico, livres de censura ou pontos únicos de falha.
* **Prova de Armazenamento Local (Desafio ADR-012):**
  * Protocolo criptográfico onde os nós DePIN comprovam matematicamente a posse íntegra dos dados sem precisar retransmitir arquivos inteiros.
* **Malha Gossip P2P:**
  * Difusão distribuída de dados e comunicação resiliente entre nós da rede.

---

### ⛓️ PILAR 04: BLOCKCHAIN EVM — Execução, Consenso & Liquidação On-Chain
> *Camada de regras de consenso, liquidação financeira irrevogável e fé pública matemática.*

* **Infraestrutura Financeira & Token ASPPBR:**
  * Padrão ERC-20 em redes EVM de alta eficiência (Arbitrum, Polygon POS, BSC).
  * Liquidação atômica e transferências financeiras sem intermediários bancários centrais.
* **Governança Descentralizada (ASPPIBRA-DAO):**
  * Ciclo integral de governança on-chain: propostas, quórum qualificado, votação auditável e execução programática.
* **Notarização Digital & Prova de Anterioridade:**
  * Ancoragem definitiva de CIDs e hashes SHA-256 em contratos inteligentes, garantindo eficácia jurídica e rastreabilidade perene.

---

## 🔄 Matriz de Integração entre as Camadas

| Origem ➔ Destino | Operação Técnica Realizada |
|---|---|
| **DevOS ➔ IPFS** | Publica documento gerado pelo Typst via RPC local (`127.0.0.1:5001`) e obtém o CID. |
| **DevOS ➔ Blockchain** | Assina transações de transferência ou governança localmente no cofre via Secp256k1. |
| **IPFS ➔ Blockchain** | Contratos inteligentes gravam o CID como prova de existência e integridade do ativo. |
| **Blockchain ➔ Cloud** | Workers indexam recibos, eventos e confirmações on-chain no banco relacional D1. |
| **Blockchain ➔ DevOS** | DevOS consulta RPCs multi-chain para atualizar saldos nativos e tokens ASPPBR em tempo real. |
| **Cloud ➔ DevOS** | Distribui estado global consolidado para visualização no DevOS Cockpit. |

---

## 🔐 Princípios Inegociáveis de Segurança

1. **Custódia Soberana Absoluta:** Chaves privadas nunca são enviadas para a nuvem; residem exclusivamente no cofre local do usuário.
2. **Imutabilidade Operacional:** Toda alteração crítica requer consenso em blockchain ou validação de dupla entrada contábil.
3. **Privacidade por Projeto:** Processamento sensível e geração documental ocorrem de ponta a ponta em ambiente offline.

---

<div align="center">
  <sub>© DIGITAL WORLD ECOSYSTEM • ASPPIBRA-DAO • Todos os direitos reservados</sub>
</div>
