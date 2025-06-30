# 🚀 Gerenciamento de Máquinas Virtuais no Azure

## 📚 Sobre o Projeto

Este repositório faz parte do desafio prático da DIO sobre gerenciamento de máquinas virtuais (VMs) no Microsoft Azure. Aqui, compartilho **resumos, anotações, capturas de tela e dicas práticas** para ajudar nos estudos e futuras implementações na nuvem da Microsoft.

---

## 🎯 Objetivos do Projeto

✅ Consolidar o aprendizado sobre máquinas virtuais no Azure  
✅ Produzir material de apoio para revisões rápidas  
✅ Compartilhar conhecimento com a comunidade DIO e outros estudantes  
✅ Praticar versionamento e documentação técnica no GitHub

---

## 💻 Conteúdos Abordados

### ✅ Criação de Máquinas Virtuais

- Criação via **Portal Azure**
- Criação via **Azure CLI**
- Criação via **PowerShell**

---

### ✅ Tamanhos e Tipos de VM

- Séries (B, D, E, F, etc.)
- Diferenças entre SKU (vCPUs, memória, disco, IOPS)
- Exemplos:
  | Série | Uso Principal                   | Exemplo de Tamanho |
  |-------|---------------------------------|--------------------|
  | B     | Workloads leves                 | B1s, B2ms          |
  | D     | Aplicações gerais               | D2s_v3, D4s_v5     |
  | E     | Workloads que exigem memória    | E2s_v3, E4s_v4     |

---

### ✅ Tipos de Disco e Armazenamento

- Standard HDD
- Standard SSD
- Premium SSD
- Ultra Disk

| Tipo de Disco   | Indicação                       |
|-----------------|---------------------------------|
| Standard HDD    | Dados pouco acessados          |
| Standard SSD    | Workloads leves e médios       |
| Premium SSD     | Alta performance, apps críticos|
| Ultra Disk      | Latência ultra-baixa           |

---

### ✅ Rede Virtual (VNet) e IP

- Criação de VNet
- Sub-redes
- Configuração de IP público/privado
- NSG (Network Security Group)

---

### ✅ Segurança

- Configuração de NSG
- SSH keys (Linux)
- Senha forte (Windows)
- Regra mínima de acesso externo

---

### ✅ Custos e Pricing

- Utilização do **Azure Pricing Calculator**
- Importância de parar/desalocar VMs quando não estiverem em uso
- Boas práticas para economizar custos:
  - Escolher SKUs menores em testes
  - Utilizar Reservas (Reserved Instances) para workloads fixos
  - Avaliar custos de storage (discos premium são mais caros)

---

## 📸 Capturas de Tela

Imagens estão disponíveis na pasta [`/images`](./images). Exemplos incluídos:
- Criação de VM no Portal
- Configuração de disco
- Configuração de rede
- Visualização do Pricing Calculator

---

## 🛠️ Passo a Passo: Criando uma VM no Azure Portal

### Portal Azure

1. Acesse o portal [https://portal.azure.com](https://portal.azure.com)
2. No menu lateral, clique em **Máquinas Virtuais**
3. Clique em **Criar**
4. Preencha os dados:
   - Nome da VM
   - Região
   - Sistema Operacional (Windows ou Linux)
   - Tamanho (SKU)
   - Usuário e senha ou chave SSH
   - Disco do sistema
   - Configuração de rede
5. Clique em **Revisar + Criar**
6. Clique em **Criar**

---

## 🚀 Azure CLI – Criação de VM (Exemplo Linux)

```bash
az vm create \
  --resource-group MeuGrupo \
  --name MinhaVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys \
  --size Standard_B1s
```
```powershell
⚙️ Azure PowerShell – Criação de VM (Exemplo Windows)
powershell
Copiar
Editar
New-AzVm `
    -ResourceGroupName "MeuGrupo" `
    -Name "MinhaVMWindows" `
    -ImageName "Win2019Datacenter" `
    -Location "East US" `
    -Size "Standard_D2s_v3" `
    -Credential (Get-Credential)
💡 Dicas Rápidas
✅ Sempre avalie o custo antes de subir VMs grandes
✅ Para estudar, use SKUs pequenos (ex.: B1s)
✅ Use SSH ao invés de senha em Linux
✅ Desligue as VMs quando não estiver utilizando
✅ Documente tudo para futuras consultas
```

## 🔗 Referências

- [Microsoft Learn – Gerenciar máquinas virtuais do Azure](https://learn.microsoft.com/pt-br/training/modules/manage-virtual-machines-azure/)
- [Azure Pricing Calculator](https://azure.microsoft.com/pt-br/pricing/calculator/)
- [Documentação Oficial do GitHub](https://docs.github.com/pt)
- [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/)

---

## 👨‍💻 Autor

**Eduardo**  
[LinkedIn](#) | [GitHub](#)


