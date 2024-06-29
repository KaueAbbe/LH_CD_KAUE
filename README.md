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
  
<h3 align ="left"> Informações Descobertas e Respondendo Perguntas</h3>

Abaixo apresento gráficos que mostram a média de valores separados em grupos de bairros e grupos de tipo de locação.

![preco_bairro2](https://github.com/KaueAbbe/LH_CD_KAUE/assets/68445400/204769ff-9cf7-451c-b6c9-d2a7e1ffc117)

O bairro que possui valor médio maior é Manhattan, no entanto não diferença estatística entre os bairos Manhattan, Brooklyn e Staten Island.

![tipos](https://github.com/KaueAbbe/LH_CD_KAUE/assets/68445400/f566c2b1-cf59-4e17-ac21-4d49d08aba17)

Enquanto os tipos de locações, a com maior preço médio é a casa inteira / Apartamento. 

Por análises obtive a seguinte conclusão:

1. A falta de nome do apto e do host diminui o valor médio.
2. A falta de review aumenta o valor médio.

E baseado nos gráficos e nas análises criei as seguintes sugestões de negócio:

1. Podemos selecionar apartamentos que estão sem review, e sugerir ao host que abaixe o preço abaixo para aumentar a chance de locação.
2. Podemos adicionar alertas aos hosts para adicionar seus nomes ao apartamento, informando que assim agrega mais valor.
3. Podemos adicionar alertas aos hosts para adicionar nomes aos quartos, além de criar dar sugestões baseadas em outros quartos.
   
<h4 align ="left"> Melhor indicação de Compra de Apartamento</h4>

* Definindo como condição de melhor locação: ter preço médio e ter reviews.
  Tal decisão foi tomada pois assim a pessoa pode ter um lugar acessível financeiramente, e que pode obter informações sobre a locação por meio de outras pessoas.
  
* Baseando que a pessoa quer o melhor local para alugar, considerei que melhor o local com maior número de reviews e com grupo de bairro de preço médio. O lugar é: **Staten Island, no bairro de Silver Lake**. O preço médio é de $173, e possui 147 reviews.

<h4 align ="left"> O número mínimo de noites e a disponibilidade ao longo do ano interferem no preço?</h4>

*Apresento dois gráficos



![preco_noite](https://github.com/KaueAbbe/LH_CD_KAUE/assets/68445400/dd0e2d74-11ba-45e3-8b94-8297d682a700)


O gráfico acima apresenta um aglomerado de valores com baixo preço e baixo número de mínimo de noites. E apresenta valores discrepantes com altos preços e baixo valor mínimo de noite, com poucos valores de baixo preço e alto valor mínimo de noite. 

![preco_disp](https://github.com/KaueAbbe/LH_CD_KAUE/assets/68445400/f717e377-c8e2-478c-a26a-5f745f71a08e)

O gráfico apresenta valores espalhados pelo gráfico, sem apresentar nenhuma tendência.

Calculei também qual o tamanho da interferência entre os dois valores: Ambas tiveram valores muito baixos. 


* Portanto baseando nos gráficos e nos valores de correlação entre preço e variáveis, conclui-se que o **tempo mínimo de noites e a disponibilidade não tem interferência significativa no preço.**

  

  <h4 align ="left"> Padrão no nome de locações acima da média</h4>
  
* Analisando as palavras mais usadas para locações acima da média obtive a seguinte nuvem de palavras e resultados comparativos:
* 
![word_cloud_alto](https://github.com/KaueAbbe/LH_CD_KAUE/assets/68445400/f03f8953-52f4-4868-924a-a7cf2b537b4e)

* Os resultados comparativos indicam:
  1. Existem palavras que repetem tanto abaixo da média quanto acima: *Apartment, Bedroom,apt, studio, spacius*.
  2. As **palavras iguais são menos frequentes no grupo acima da média**. E os acima da média não utilizam muito a palavra room.
  3. O grupo abaixo da média utiliza palavras da localização: Brooklyn e Manhattan. 
  4. É mais comum ao grupo acima da média utilizar numerais no texto.

Baseados nesses dados faço duas sugestões:
1. Criar um painel de dicas para o host quando for criar o nome da locação, sugerindo, por exemplo, não utilizar nomes de localização.
2. Realizar uma análises aprofundade apenas nos textos para avaliar se a utilização (ou a falta) de determinadas palavras se deve ao tipo de locação e se resultado em melhores resultados na locação.



 
<h2 align ="left"> Criação do Modelo</h2>

* Tal modelo tem objetivo de precificar locações, portanto se trata de um modelo de regressão.

  Esta criação de modelo seguiu os seguintes passos:
  1. Importação de Módulos de bibliotecas necessários.
  2. Escolha da métrica: R² - r2_score -> Escolhi esta métrica pois analisa a distância entre o valor predito e real, possuindo fácil interpretação.
     
  3. Preparação dos dados:
     * Foram retirados os valores outliers, já que modelos de regressão são sensíveis a outliers e podem resultar em baixo poder de predição.
     * Separação dos dados em treino, teste e validação: Serão usados para, respectivamente, treinar, testar o modelo e validar o resulto pós otimização. Esta técnica evita com que hajá viés e vazamento de dados no modelo, garantindo que posso avaliar seu ajuste aos dados e poder de predição.
     * Obtenção das features com alta cardinalidade, salvando seus nomes. Estas features serão retiradas dos dados de treino por não agregar à generalização do modelo.
     * Criação de lista de features categóricas que terão tratamento por Técnicas de Encoding.
  
  4. Criação da Pipeline de Treino com seguintes passos:
     * Receber os dados de treino e teste.
     * Retirar as colunas com alta cardinalidade.
     * Aplicar Target Encoding em features específicas: Esta técnica transforma valores categóricos em númericos baseando no target, colocando um valor esperando. Esta técnica foi utilizando em apenas features bastantes valores únicos.
     * Aplicar OneHotEncoding na feature bairro_group: Esta técnica cria quantidade de colunas igual a quantidade de cardinalidade na feature original, onde cada nova colunas informa com 0 ou 1 se a locação é de tal bairro ou não. Utilizei essa técnica apenas em feature com baixa cardinalidade.
     * Aplicação do MinMaxScaler: Usado para reorganizar os valores dos dados contínuos entre 0 e 1, para auxiliar na melhor performance dos modelos. O uso deste Scaler é porque os dados não seguem distribuição normal.
     * Treinamento do modelo utilizando validação cruzada: O uso da validação cruzada foi para realizar mais de um treinamento com split dos dados de treino, obtendo um valor médio da métrica escolhida.
     * Fazer um predict com dados de teste e avaliar a perfomace: Com este valor observo se os resultados de treino e teste estão discrepantes, assim indicando overfitting ou underfitting.

  5. Otimização de Hiper Parâmetros do melhor modelo:
     * O melhor modelo escolhido teve que apresentar a melhor perfomance no treino e no teste. Além de não apresentar overfitting nem underfitting, pois assim garanto que o modelo está tenho boa performance e generalização.
     * Também foi levado em consideração o tempo de treino do modelo, medido de forma heurística. Isto porque é importante que o modelo também possa trazer resultados mais rápidos.
     * A otimização foi feita utilizando RandomizedSearchCV e GridSearchCV: O Randomized foi utilizado para otimizar por ser mais rápido que o GridSearch, no entanto também utilizei o GridSearch com menos entradas para poder fazer uma busca mais vasta dentro das combinações possíveis de hiper parâmetros.

    6. Criação da Pipeline com Modelo Otimizado
       * Com o resultado da melhor combinação de hiperparâmetros, criei a pipelina seguinte as mesma especificações da pipeline de treino, alterando apenas o modelo para ter os hiperparâmetros encontrados.
       * Realizei o teste do modelo final com os dados de validação: O uso dos dados de validação serve para avaliar o desempenho do modelo com dados nunca vistos.
    7. Criação de uma função preditora:
       * A função preditora foi criada pois o treino do modelo possuia dados criados durante tratamento, e que não serão passados quando ocorrer um predição com novos dados.
       * A função adicionar os dados novos: São basicamentos dados missing de determinadas colunas
       * A função remover colunas que não foram usadas no treinamento: as de alta cardinalidade.
       * A função lê o arquivo Pickle da pipeline otimizada e retorna a predição.
    8. Salvamento da pipeline otimizada e da função em formato pkl para ser disponibilidade para um futuro deploy e usada em predições de novos dados. 


  

  
<h3 align ="left"> Resultados Modelo </h3>

O modelo utilizado foi: HistGradientBoostingRegressor, pelos seguintes motivos:
* O modelo é do tipo Ensemble, que utiliza vários algoritmos que melhora a generalização e robustez.
* O modelo performa mais rápido que o GradientBoostingRegressor, que é um "irmão" do modelo.
* O modelo apresentou rapidez e desempenho melhor, tanto no treino como no teste.
* **Após otimização:** O modelo apresentou R² = 70%. Isto mostra que o modelo possui boa generalização dos dados, e tem bom poder de predição.

1. Com os dados dados pelo desafio (dicionário escrito na etapa de instalação e execução deste readme) **o resultado obtido pelo preditor foi: $ 192.99**.


<h2 align ="center"> Próximas Etapas</h2>

Os resultados finais apresentados foram obtidos com dados de validação do modelos, o que mostra que o modelo perfomaria bem no dia a dia. O próximo passo seria fazer o deploy do modelo, para ser utilizado pela empresa. Além disto, deveria ser estabelecer formas acompanhar o desempenho do modelo com o tempo. Outras etapas são avaliar e projetar as sugestões dados neste relatório, passando aos times necessários. 

<h2 align ="center">Autor 🚀</h2>
<a>
<img style = "border-radius: 50%;" src = https://github.com/KaueAbbe/Analise_ChurnRate/assets/68445400/bd4b5b79-4826-4d72-91e4-5fc7532ac19b width="250px;" alt=""/>

 <sub><b></b></sub></a> 

<h4> Feito com 💙 por Kaue Hermann Abbehausen 👋🏽 
<br/> 
 
 1.Cientista de Dados
 
 2. Formado em Física na Universidade Federal de Uberlândia
 
 3. Mestre em Física Estatística na Universidade de Brasília</h4>
<h4> Entre em contato por</h4>
<div align = "center"> 

<div align = "center"> 
   <a href="https://www.linkedin.com/in/kaue-abbehausen-5b1922165/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  <a href="https://www.instagram.com/kaue.hermann/" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:kaueabbehausen@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white"></a>
</div>
