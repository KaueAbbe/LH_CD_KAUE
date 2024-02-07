<h1 align="center"> Bem vinda(o) ao Desafio Cientista de Dados😊 </h1>

![Badge em Desenvolvimento](https://img.shields.io/static/v1?label=STATUS&message=COMPLETO&color=<COLOR>)

<h1 align ="center"> Objetivo do Case🤔</h1>

Utilizar conhecimentos de ciência de dados para compreender o atual contexto de preços e suas variáveis de em um site de locação de imóveis. E com isto gerar insights de negócio e criar um modelo que precifique o valor da locação por noite.  


<h1 align ="center"> Instalando e Executando</h1>

* Para baixar e utilizar o modelo basta seguir os seguintes passo:
  1. Faça o download dos arquivos: preditor.pkl e pipeline_otimizada.pkl.
  2. Num ambiente virtual python importe a biblioteca pickle e leia o arquivo **preditor**
  3. Faça a predição do valor passando um dicionário com as seguintes chaves:
     
     {'id': 2595, 'nome': 'Skylit Midtown Castle', 'host_id': 2845, 'host_name': 'Jennifer', 'bairro_group': 'Manhattan', 'bairro': 'Midtown',
 'latitude': 40.75362, 'longitude': -73.98377, 'room_type': 'Entire home/apt', 'minimo_noites': 1, 'numero_de_reviews': 45,
 'ultima_review': '2019-05-21', 'reviews_por_mes': 0.38, 'calculado_host_listings_count': 2, 'disponibilidade_365': 355}

  4. Os valores podem ser alterados.
  5. O valor resultante é o valor predito pelo modelo


<h1 align ="center"> Resumos das Etapas</h1>

<h2 align ="left"> Tratamento dos Dados</h2>

Realizei tratamento dos dados. Este processo contou as etapas de leitura dos dados, obtenção de informações básicas do dataset, buscando inconsistênicias como valores duplicados e faltantes. Correções foram feitas nas inconsitências encontradas, criando colunas que informam a existência de valores faltantes para levar para Análise Exploratória e para o Modelo de Classificação.

* Leitura, organização e compreensão dos dados.
* Análise de tipo de dados.
* Procura e correção das inconsistências.
* Criação de Novas colunas que informam se os dados eras faltantes.
* Avaliar e retirar duplicatas.
* Criação de novo arquivo para uso futuro.

<h2 align ="left"> Análise Exploratória e Explanatória</h2>

Realizei análise estatística descritiva univariadas. Realizei análise bivariada, analisando a relação das featues com o preço, realizando nesta etapa estatística inferencial com uso de teste de hipóteses não paramétricos. Com as informações adquiridas realizei data visualization, e utilizei modelos para ajudar a compreender o papel de cada feature com relação a target(preço). Apliquei **técnicas de NLP** e visualizei o padrão de nomes de locações para altos preços e baixos preços. Com base nestas informações criei hipóteses e sugestões de negócios. 

* Análise da variável target, visualização de distribuição
* Análise de dados qualitativos e quantitativos
* Análise bivariada entre grupos da variável target
* Data visualization
* Testes de hipóteses
* Storytelling
* Criação e teste de regra de Bussines
* Técnicas de NLP
  
<h3 align ="left"> Informações Descobertas</h3>


 
<h2 align ="left"> Criação do Modelo Classificação</h2>

* Análise de Correlação e retirada de features multicolineares
* Definição da Baseline como o Recall do Modelo Antigo: 73.72%
* Separação de dados de treino, teste e validação
* Criação da Pipeline para treinamento de modelos com seguintes passos:
  1. Aplica Category Encoder, utilizando Weigth of Evidence,
  2. Escalonamento dos Dados
* Definição de Recall e F1 como métrica de Bussines
* Definicação de Validação Cruzada para treinamento
* Treinamento de seis modelos de machine learning de classificação, e definição do melhor modelo
* Otimização por Hiperparâmetros do Modelo Gradient Boost
* Criação da Pipeline do modelo Otimizado

  

  
<h3 align ="left"> Resultados Modelo </h3>





<h2 align ="center">Autor 🚀</h2>
<a>
<img style = "border-radius: 50%;" src = https://github.com/KaueAbbe/Analise_ChurnRate/assets/68445400/bd4b5b79-4826-4d72-91e4-5fc7532ac19b width="250px;" alt=""/>

 <sub><b></b></sub></a> 

<h4> Feito com 💙 por Kaue Hermann Abbehausen 👋🏽 
<br/> 
 
 1. Formado em Física na Universidade Federal de Uberlândia
 
 2. Mestrando em Física Estatística na Universidade de Brasília
    
 3. Cientista de Dados</h4>
<h4> Entre em contato por</h4>
<div align = "center"> 

 
   <a href="https://www.linkedin.com/in/kaue-abbehausen-5b1922165/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  <a href="https://www.instagram.com/cienciaeanimacao/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:kaueabbehausen@hotmail.com"><img src="https://img.shields.io/badge/Microsoft_Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white" target="_blank"></a>
</div>
