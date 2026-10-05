# Dio Desafio: Otimizando Custos no Azure

Este documento tem como objetivo explicar de forma clara e prática os principais fatores que afetam os custos na **Microsoft Azure**, como calcular o **Custo Total de Propriedade (TCO)**, utilizar a **Calculadora do Azure**, e explorar o **Cost Management + Billing**. Ao final, há um passo a passo para criar uma estimativa de Máquina Virtual no portal.

---

## 🌐 Fatores que afetam os custos

- **Tipo de recurso**: Máquinas Virtuais, Banco de Dados, Armazenamento, Rede, cada um possui modelos de cobrança diferentes.
- **Consumo**: O uso efetivo (CPU, memória, transações, GB armazenados) impacta diretamente o valor.
- **Manutenção**: Atualizações, backups e monitoramento podem gerar custos adicionais.
- **Área geográfica**: Os preços variam conforme a região escolhida (ex.: Brasil vs. EUA).
- **Tráfego de rede**: Saída de dados (egress) para fora do Azure é cobrada.
- **Assinatura**: Tipos de contrato (Pay-As-You-Go, Enterprise Agreement, CSP) influenciam descontos e benefícios.

---

## 💰 Custo Total de Propriedade (TCO)

O TCO ajuda a comparar custos de infraestrutura local vs. nuvem.

1. **Definir suas cargas de trabalho**  
   - Servidores, bancos de dados, armazenamento e rede devem ser mapeados.
2. **Ajustar suposições**  
   - Estimar crescimento, uso médio, licenciamento e manutenção.
3. **Exibir relatório**  
   - O Azure gera relatórios com projeções de economia e custos.

---

## 🖥️ Impacto das cargas de trabalho nos custos

- **Servidores (VMs)**: Custos variam por tamanho, tipo (General Purpose, Compute Optimized), sistema operacional e tempo de execução.
- **Banco de Dados**: Modelos de cobrança por DTUs, vCores ou transações. Serviços gerenciados (Azure SQL, Cosmos DB) podem reduzir custos de manutenção.
- **Armazenamento**: Cobrança por GB/mês, tipo de redundância (LRS, ZRS, GRS) e operações de leitura/escrita.
- **Rede**: Custos de tráfego de saída, balanceadores de carga, VPNs e firewalls.

---

## 📊 Itens que impactam os custos

- **Software Assurance + Benefício Híbrido do Azure**: Permite usar licenças locais no Azure, reduzindo custos de VMs Windows e SQL.
- **GRS (Geo-Redundant Storage)**: Mais caro que LRS/ZRS, mas garante replicação entre regiões.
- **Máquinas Virtuais**: Custos dependem de tamanho, região e sistema operacional.
- **Eletricidade**: No Azure, já está embutida no custo; em on-premises é um gasto adicional.
- **Armazenamento**: Quanto maior o volume e redundância, maior o custo.
- **Mão de obra de TI**: Nuvem reduz custos de manutenção física, mas exige gestão de serviços.

---

## 🧮 Calculadora do Azure

🔗 [Azure Pricing Calculator](https://azure.microsoft.com/pt-br/pricing/calculator/)

- **Quando usar**: Planejamento de novos projetos, estimativas de migração, simulações de cenários.
- **Prós**:
  - Interface simples e intuitiva.
  - Permite comparar diferentes serviços e regiões.
  - Exporta relatórios em Excel/PDF.
- **Contras**:
  - Estimativas podem não refletir uso real.
  - Não considera descontos específicos de contrato.
  - Não inclui custos indiretos (treinamento, suporte).

---

## 📈 Cost Management + Billing

Ferramenta nativa do Azure para monitorar e otimizar custos.

- **Overview**: Visão geral dos gastos por assinatura e recurso.
- **Cost Analysis**: Relatórios detalhados por serviço, grupo de recursos ou tags.
- **Cost Alerts**: Alertas configuráveis para avisar quando gastos ultrapassam limites.
- **Budgets**: Definição de orçamento mensal/anual com acompanhamento.
- **Advisor Recommendations**: Sugestões de otimização (ex.: desligar VMs subutilizadas, mudar para instâncias reservadas).

---

## 🚀 Passo a Passo: Criando uma estimativa de Máquina Virtual no Portal Azure

1. **Acesse o Portal Azure**: [https://portal.azure.com](https://portal.azure.com)
2. **No menu lateral**, clique em **Criar um recurso**.
3. **Selecione "Máquina Virtual"**.
4. **Configurações básicas**:
   - Escolha a **assinatura** e **grupo de recursos**.
   - Defina a **região** (ex.: Brazil South).
   - Selecione o **sistema operacional** (Windows/Linux).
   - Escolha o **tamanho da VM** (ex.: Standard_B2s).
5. **Configurações adicionais**:
   - Disco (SSD/HDD, LRS/GRS).
   - Rede (IP público, balanceador).
   - Segurança (firewall, backup).
6. **Na aba "Revisar + Criar"**, o portal exibirá uma **estimativa de custo mensal**.
7. **Confirme a criação** ou exporte a estimativa para análise.

---

## 📌 Conclusão

Gerenciar custos no Azure exige atenção a múltiplos fatores: tipo de recurso, consumo, região e licenciamento. Ferramentas como a **Calculadora do Azure** e o **Cost Management + Billing** são essenciais para planejar e otimizar gastos. O uso consciente de benefícios como o **Azure Hybrid Benefit** e escolhas adequadas de redundância podem gerar economias significativas.

