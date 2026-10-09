# 🏎️ Dashboard de Vendas Porsche

**Dashboard interativa criada com IA para o desafio da plataforma DIO** – *Criando uma Dashboard da Porsche com Agentes de IA*

![HTML](https://img.shields.io/badge/HTML-único_arquivo-D5001C?style=for-the-badge&logo=html5&logoColor=white) ![Claude](https://img.shields.io/badge/Claude-Canvas_(Free)-0B0B0D?style=for-the-badge) ![Dados](https://img.shields.io/badge/Dados-100_registros-D5001C?style=for-the-badge) ![Moeda](https://img.shields.io/badge/Moeda-USD-0B0B0D?style=for-the-badge)

[🔗 Acessar a dashboard](#-dashboard-publicada) · [❓ Perguntas de negócio](#-perguntas-de-negócio) · [🧾 Prompt](#-prompt-utilizado) · [🧹 Tratamento da base](#-tratamento-da-base)

---

## 📌 Sobre o projeto

Dashboard criada a partir da **base de vendas da empresa Porsche** (`Planilha base Porsche (Sanitizada).xlsx`). Ela reúne filtros, indicadores de topo e gráficos que respondem a três perguntas de negócio, com visual inspirado na marca (preto, branco e vermelho, e tipografia condensada em caixa alta).

### ✨ O que a dashboard oferece

| Recurso | Descrição |
|---|---|
| 🎛️ **Filtros** | Linha, modelo, região, cidade, ano da venda, método de pagamento e status de entrega |
| 📊 **Indicadores de topo** | Total de vendas, receita, ticket médio, % de elétricos e híbridos e % de entregues |
| 📈 **Gráficos interativos** | Barras por modelo, linha, região, estado e cidade; evolução por mês ou trimestre; mix de motorização |
| 🗂️ **Tabela de detalhe** | Lista das vendas filtradas |
| 🌗 **Tema claro e escuro** | Acompanha a preferência do dispositivo |
| 📱 **Responsiva** | Funciona no computador e no celular |

---

## ❓ Perguntas de negócio

> Quais perguntas de negócio foram escolhidas, e por quê.

### 1️⃣ Qual modelo gera mais receita?

**Por quê:** indica onde o resultado está concentrado e, com isso, orienta decisões de estoque, foco comercial e prioridade de entrega.

### 2️⃣ Como as vendas se distribuem por região e mercado, e como evoluem ao longo do tempo?

**Por quê:** junta distribuição geográfica e evolução temporal para responder a uma pergunta de planejamento: *onde* e *quando* vender. Serve para definir metas por praça, campanhas e distribuição de veículos.

### 3️⃣ Qual o peso dos modelos elétricos e híbridos (Taycan, Macan Electric) em relação aos de combustão, e como isso muda por região?

**Por quê:** analisa o respaldo do mercado às mudanças da marca para modelos híbridos e elétricos. Saber quanto eles pesam frente à combustão mostra se o mercado está aceitando essa mudança na prática.

### 🔎 O que a dashboard mostra com os filtros padrão

Com todos os dados e o filtro padrão (que exclui vendas canceladas), a dashboard apresenta:

| Pergunta | Resultado |
|---|---|
| 1️⃣ Modelo com maior receita | **911 Dakar**, com US$ 810.600 (7% do total). A linha **911** soma 34% da receita |
| 2️⃣ Região com maior receita | **Oeste** (33%); a menor é o **Nordeste** (6%). Trimestre de maior receita: 2º de 2026 |
| 3️⃣ Peso de elétricos e híbridos | **27%** das vendas e **26%** da receita; maior participação no **Sudeste** (35%) e menor no **Nordeste** (17%) |

> ⚠️ **Atenção:** a base tem apenas 100 registros, e algumas regiões têm poucas vendas. Os resultados são indicativos.

---

## 🧾 Prompt utilizado

> O prompt que gerou a dashboard, e o que mudou nele até a versão final.

O prompt foi usado em uma única versão, sem reescritas:

```text
Crie uma dashboard em HTML no canvas, com os filtros dos dados, como modelo,
cidade, ano ou método de pagamento, que possua indicadores de topo, como total
de vendas e receita, utilize um visual que corresponda a marca da Porsche,
incluindo paleta de cores e tipografias e responsa as seguintes perguntas de
negócios:

1° Qual modelo que gera mais receita?

2° Como as vendas se distribuem por região e mercado, e como evoluem ao longo
do tempo?

3° Qual o peso dos modelos elétricos e híbridos (Taycan, Macan Electric) em
relação aos a combustão, e como isso muda por região?

gere em um arquivo único com base no arquivo anexo "Planilha base Porsche
(Sanitizada).xlsx"
```

---

## 🧹 Tratamento da base

> Que tratamento a base precisou antes de ir para a IA.

- 🔢 Conversão de alguns campos para **formato numérico**
- 💵 Ajuste da moeda comercial para **Dólar Americano (US$)**

### Regras aplicadas pela dashboard

Algumas decisões foram tomadas na construção da dashboard, e é importante conhecê-las ao interpretar os números:

- ❌ Vendas **canceladas** ficam de fora por padrão. Para incluí-las, escolha *Todos os status* no filtro de entrega.
- 📅 Registros com data **inválida** (`INVALID`) entram nos totais, mas não no gráfico de evolução no tempo.
- 🔮 Registros com data **posterior a 09/10/2026** foram mantidos como estão na planilha.
- ⚡ **Motorização:** Elétrico = Taycan e Macan Electric; Híbrido = modelos E-Hybrid; Combustão = demais.
- 🗺️ **Regiões:** a base só tem cidades dos EUA, então os estados foram agrupados em Oeste, Sudoeste, Sudeste, Meio-Oeste e Nordeste.

---

## 🤖 Ferramentas de IA

> Se foi usado ChatGPT com Canvas, um agente com skill, ou os dois.

Foi utilizado o **Claude com Canvas**, na versão **Free**.

---

## 🌐 Dashboard publicada

> O endereço da dashboard publicada.

👉 **[Abrir a dashboard](https://wellintonbm.github.io/desafio_dio_dashboard_porsche)**


---

Projeto desenvolvido para o desafio da **DIO** · Criando uma Dashboard da Porsche com Agentes de IA
