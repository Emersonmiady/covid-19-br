# COVID-19: análise dos casos e mortes no Brasil
---
Este projeto foi desenvolvido durante o **Bootcamp de Data Science Aplicada (Alura)**, no Módulo 1. Neste módulo tivemos o primeiro contato com **Manipulação e Visualização de Dados**, entrando de forma prática na área de Ciência de Dados. As aulas foram feitas em cima dos dados financeiros do SUS.

Como proposta inicial de desafio, foi pedido uma análise referente a base de dados de produção hospitalar, seja número de internação, óbito, AIH ou taxa de mortalidade. Entretanto, o DATASUS acabou ficando fora do ar e, então, acabamos utilizando os dados do projeto Brasil.io, sobre os **casos de COVID-19** no Brasil.

- Análise completa em "**covid_19_brasil.ipynb**".

Observação: para melhorar a visualização de algumas imagens, por conta da resolução que foi comprometida, recomendo clicar em "Open in Colab", no começo do *notebook*.

# Contexto
---
O contexto todo mundo já sabe, 2020 foi o ano da COVID-19, deixando milhões de casos e mortes no mundo todo... Entretanto, o meu objetivo nesse projeto, foi ver, com a **análise exploratória**, como estava a **situação no país até o dia 09/11/20**, e também fazer comparações entre as **UF's** e as **Regiões brasileiras**, porém focando nos **números por 100 mil habitantes**. 

# Ferramentas utilizadas
---
- Linguagem de programação Python;
- Pacotes: pandas, numpy, datetime, matplotlib, seaborn;
- Notebook: Google Colaboratory.

# Descrição breve das etapas
---
## 1. Pré-processamento
- Exclusão das variáveis `place_type`, `city`, `city_ibge_code`, `estimated_population_2019`;
- Manipulações com as colunas para descobrir os valores de casos e mortes por 100 mil habitantes;
- Criando a coluna das Regiões brasileiras, podendo realizar assim, as análises por esta escala.

## 2. Análise Exploratória dos Dados
O que mais foi utilizado foram gráficos de barras, para saber os números em cada UF até o momento, por 100 mil habitantes, e também o de linhas, por conta dos dados seguirem uma ordem temporal. Algumas visualizações abaixo:
![](https://github.com/Emersonmiady/covid-19-br/blob/main/img/deaths_100k_uf_until_the_moment.png?raw=true)
![](https://github.com/Emersonmiady/covid-19-br/blob/main/img/acum_cases_deaths_regions_until_the_moment.png?raw=true)
![](https://github.com/Emersonmiady/covid-19-br/blob/main/img/acum_cases_100k_region.png?raw=true)
![](https://github.com/Emersonmiady/covid-19-br/blob/main/img/new_cases_br.png?raw=true)

## 3. Conclusões resumidas
- Sobre as Unidades Federativas:
  -	As UF's que possuem os maiores números de casos acumulados / 100 mil habitantes são, em ordem decrescente: **RR**, **DF** e **AP**. O pior deles é Roraima, que vem apresentando uma taxa de crescimento maior nos últimos tempos;

  - As UF's que possuem os maiores números de mortes acumuladas / 100 mil habitantes são, em ordem decrescente: **DF**, **RJ** e **MT**. Mesmo tendo o DF como primeiro nesse caso, eu considero RJ o pior dos três, pois sua população absoluta é **muito** diferente, comparando com as outras duas UF's, tendo **muitas** pessoas, tanto em números absolutos quanto em porcentagem da população, que se contaminaram com o COVID-19.

- Sobre as regiões:
  - A região que possui o maior número de casos/mortes acumulados/as por 100 mil habitantes é o **Centro-Oeste**. Essa região é a que deve tomar mais cuidado, pois apresenta a maior taxa de crescimento em todas essas medidas;

  - A atenção deve-se atentar principalmente em **DF** e **MT**, pois além de serem os responsáveis por aumentar as medidas acima, apresentam os maiores números de mortes acumuladas / 100 mil habitantes.
  
- Sobre o Brasil como um todo:
  - A porcentagem de mortes no dia 27/10, pelas pessoas que pegaram COVID-19 é de **2,9%**;
  - Os maiores valores das mortes diárias ficaram sob um período **mais longo**, se comparado com os maiores valores dos casos diários da doença.

Em todas as nossas análises móveis, notamos que os maiores valores diários foram por volta de Julho e Setembro.

Felizmente, os novos valores diários já alcançaram seus picos, e suas taxas de crescimento, no caso dos números acumulativos por 100 mil habitantes, estão decaindo. Aparentemente já passamos da pior fase! (mal sabia ainda o que estava por vir)
