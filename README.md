# 🚀 Desafio de Previsão de Preços Indicium

## 💻 Sobre o projeto

Este projeto tem como objetivo desenvolver um modelo de previsão de preços a partir do dataset oferecido, avaliando sua performance com métricas adequadas.

Durante a análise, foram respondidas as seguintes perguntas:

### 1 - Supondo que uma pessoa esteja pensando em investir em um apartamento para alugar na plataforma, onde seria mais indicada a compra?
**Resposta:** O melhor bairro para investimento é Manhattan, com média de preço de U$ 196,88.

### 2 - O número mínimo de noites e a disponibilidade ao longo do ano interferem no preço?
**Resposta:** O número mínimo de noites e a disponibilidade têm pouca influência no preço, pois a correlação entre essas variáveis é baixa. Outros fatores, como localização e tipo de acomodação, impactam mais a precificação.

### 3 - Existe algum padrão no texto do nome do local para lugares de mais alto valor?
**Resposta:** Sim, existe um padrão, e as palavras mais comuns em locais mais caros são:
```
[('in', 1208), ('bedroom', 725), ('apartment', 558), ('apt', 515), ('luxury', 478), ('loft', 467), ('w', 443), ('the', 408), ('village', 385), ('park', 372)]
```

### 4 - Como foi feita a previsão do preço?
**Resposta:** O problema é de regressão, pois prevemos um valor contínuo (preço). Utilizei variáveis como localização, tipo de quarto, noites mínimas e reviews, que influenciam o preço. Escolhi o modelo **Random Forest Regressor** devido à sua precisão e robustez, apesar de ser mais pesado. As métricas usadas (**MAE, MSE e R²**) avaliam erro médio, penalizam desvios e medem o ajuste do modelo.

### 5 - Previsão de preço para um apartamento específico
Dado um apartamento com as seguintes características:
```json
{
  "id": 2595,
  "nome": "Skylit Midtown Castle",
  "host_id": 2845,
  "host_name": "Jennifer",
  "bairro_group": "Manhattan",
  "bairro": "Midtown",
  "latitude": 40.75362,
  "longitude": -73.98377,
  "room_type": "Entire home/apt",
  "minimo_noites": 1,
  "numero_de_reviews": 45,
  "ultima_review": "2019-05-21",
  "reviews_por_mes": 0.38,
  "calculado_host_listings_count": 2,
  "disponibilidade_365": 355
}
```
**Resposta:** Sugestão de preço: **U$ 298.73**

---

## 🎲 Obtenção de dados
O dataset utilizado para este projeto foi fornecido pela Indicium e contém informações detalhadas sobre acomodações disponíveis para alugar em diferentes bairros, incluindo preço, localização e tipo de hospedagem.

## 🛠 Tecnologias
As seguintes ferramentas foram usadas na construção do projeto:
- **Python**
- **Jupyter Notebook**
- **Pandas** (manipulação de dados)
- **Scikit-Learn** (treinamento do modelo)
- **Matplotlib e Seaborn** (visualização de dados)

---

## 🚀 Como executar o projeto

### 1. Clone o repositório
```sh
git clone https://github.com/AllysonVBM/Previsao_de_Precos
.git
```

### 2. Crie e ative um ambiente virtual
```sh
python -m venv venv
# No Windows
venv\Scripts\activate
# No Linux/Mac
source venv/bin/activate
```

### 3. Instale as dependências
```sh
pip install -r requirements.txt
```
📥 Baixe o modelo aqui: [Google Drive - modelo_predicao.pkl](https://drive.google.com/file/d/1TJhmnoLtTyafV3T68EWfekLMyFvP2xUm/view?usp=drive_link)
e o coloque no local do ambiente virtual

### 4. Instale um kernel Jupyter para esse ambiente virtual
```sh
ipython kernel install --user --name=nome_do_ambiente_virtual
```

### 5. Selecione o kernel instalado no Jupyter Notebook
Ao abrir o Jupyter Notebook, escolha o kernel correspondente ao ambiente virtual criado.

### 6. Execute as células do notebook
Abra o notebook e execute todas as células a partir do menu **Run All**.

---

## 📊 Resultados
Os resultados do modelo demonstram que a previsão de preços foi bem-sucedida, com boa acurácia para diferentes tipos de acomodações. A escolha do modelo Random Forest Regressor se mostrou eficaz, e as métricas utilizadas ajudaram a avaliar seu desempenho de forma adequada.

---

## 📌 Conclusão
O projeto forneceu insights valiosos sobre os fatores que influenciam o preço de acomodações. A análise indicou que **a localização é o principal fator determinante** no preço, e que palavras-chave como "luxury" e "loft" são comuns em locais mais caros. O modelo desenvolvido permite previsões precisas, auxiliando investidores a tomar decisões informadas sobre o mercado imobiliário.



