# Analise_Financeira.bitcoin

## Descrição Projeto


**Conjunto de dados:** Dataframe extraído de uma API, disponibilizada pelo site Yahoo. 

**Arquivo:** Dataframe


**Objetivo:** Analisar a cotação do bitcoin em tempo real, verificar sazonalidades, plotar e testar gráficos diversos para visualização e, compilar a análise em um relatório, podendo ser exportado em PDF.

**IDE:** Colab


**Linguagem:** Python


**Principais bibliotecas utilizadas:**

•	Pandas, para manipulação, modelagem e tratamento dos dados; 

•	Numpy, para realizar cálculos numéricos; 

•	Matplotlib, para criação e visualização de gráficos;

•	Seaborn, para criação e visualização de gráficos;

•	Plotly, para criação e visualização de gráficos interativos;

•	Datetime, para manipulação com datas.


**Sequência de processos:**

1° Instalação bibliotecas;


2° Coletar dados e modelar Dataframe conforme períodos necessários para análise. Nesse caso, optou-se por utilizar uma análise de um período dos últimos 6 meses da cotação do bitcoin.


3° Realizada análise descritiva dos dados, verificando: valor médio, desvio padrão, valor mínimo, 1° quartil (25%), 2° quartil (50% - mediana), 3° quartil (75%) e valor máximo. 
Foi possível observar que os valores da média e mediana estavam próximos, evidenciando uma distribuição normal dos dados.

	
4° Realizada análise para verificar informações do Dataframe, como: período da análise, utilizado como DatetimeIndex, total de colunas e total de linhas, se existe dados nulos, tipo dos dados e quantidade de memória usada pelo Dataframe;


5° Plotado gráfico simple de linhas para verificar disposição dos dados;


6° Com a função .Rolling, foi possível estabelecer uma média móvel para anexar aos gráficos.

- A função rolling() é uma função do pandas que permite calcular estatísticas em janelas deslizantes de dados. Ela é muito útil para calcular médias móveis, desvios padrão, somatórios, mínimos e máximos, entre outras estatísticas.


7° Plotado gráfico um pouco mais robusto, incluindo média móvel em um período de 5 e 30 dias;


8° Utilizando plotly.express, foi possível criar um gráfico de linhas, com visualização interativa, utilizando apenas uma linha de comando.

plotly.express (px) é uma maneira rápida e fácil de criar visualizações dinâmicas de dados.


9° Utilizando plotly.graph_objects, foi possível criar um gráfico de linhas, com visualização interativa também, e podendo aplicar mais detalhes,  utilizando algumas linhas de comando.

- plotly.graph_objects (go) é a API de nível inferior que concede mais controle sobre suas visualizações, mas é mais intensiva em código.


10° Utilizando plotly.express com update de axes e layout foi possível plotar um gráfico de área preenchido mais completo, com botões para filtrar períodos de análise dos dados;


11° Utilizando plotly.graph_objects, plotou-se um gráfico conhecido como Candlestick e, aplicando um update foi possível incrementar e personalizar seu layout.

- Candlestick Charts: É um estilo de gráfico financeiro que descreve abertura, alta, baixa e fechamento para uma determinada xcoordenada (tempo mais provável). As caixas representam a dispersão entre os valores opene closee as linhas representam a dispersão entre os valores lowe high. Pontos de amostragem onde o valor de fechamento é maior (inferior) do que o valor de abertura são chamados de crescentes (decrescentes). Por padrão, as velas crescentes são desenhadas em verde, enquanto as decrescentes são desenhadas em vermelho.


12° Construiu-se um relatório personalizado com dois gráficos para análise gerencial;


13° Utilizando a biblioteca Kaleido, foi possível exportar o relatório em formato PDF. 

- Kaleido é uma biblioteca de plataforma cruzada para geração de imagens estáticas (por exemplo, png, svg, pdf, etc.) para bibliotecas de visualização baseadas na web, com foco particular na eliminação de dependências externas. O foco inicial do projeto é a exportação de imagens plotly.js do Python para uso por plotly.py, mas ele foi projetado para ser relativamente direto para estender a outras bibliotecas de visualização baseadas na web e outras linguagens de programação. O foco principal do Kaleido (pelo menos inicialmente) é servir como uma dependência de bibliotecas de visualização baseadas na web, como plotly.py. Como tal, o foco está em fornecer uma API programática, em vez de amigável ao usuário.
