# introducao-matplotlib
Criei este repositório para demonstrar algumas maneiras plotar gráficos com a biblioteca matplotlib.

# O que é e para que serve a biblioteca matplotlib?

Antes de entendermos o que de fato é matplotlib, vamos enterder os métodos mais comuns para trabalharmos com dados utilizando o Python.

Para tratamento, análises e explorações de dados com Python existem uma gama de bibliotecas que podemos utilizar e, dependendo das necessidades algumas bibliotecas podem ser mais adequadas do que outras. Atualmente a biblioteca pandas vem sendo amplamente utilizado na área de dados devido sua versatilizadade e performance. Neste breve exemplo antes de chegar na matplotlib estarei mostrando formas de visualizações de dados com o pandas, temos:
- display ou print....(para base grande exibe uma fatia dos primeiros e os últimos registros, para base pequena geralmente exibe a base inteira);
- head....................(por padrão exibe apenas os 5 primeiros registros da base, mas pode ser passado um valor maior como argumento);
- tail........................(a mesma coisa que o head, a diferença é que exibe os últimos registros);
- shape...................(exibe a quantidade de linhas e colunas da base);
- info.......................(exibe informações gerais dos tipos das colunas);
- ...;

Os métodos citados apresentam os dados de forma crua, exibem como vetores e matrizes. Existem maneiras mais interessantes para visualizarmos os dados, digo, algo mais visual para facilitar a análise, obviamente, relembro a escolha de recursos depende das suas necessidades.

Sabendo disso, podemos contar com algumas bibliotecas gráficas do Python para nos auxiliar durante os processos de análises exploratórias.

<h3>Mas afinal, o quê é matplotlib?</h3>

Vamos lá, <b>matplotlib<b> é um pacote de plotagem para desktop, projetada para criar plotagens com qualidade para publicação (em sua maior parte, bidimensionais). O projeto foi criado por John Hunter em 2002 com o intuito de possibilitar uma interface de plotagem do tipo MATLAB em Python. A biblioteca matplotlib aceita vários backends de GUI em todos os sistemas operacionais e, além disso é capaz de exportar visualizações para todos os vetores comuns e formatos de gráficos raster (PDF, SVG, JPG, PNG, BMP, GIF etc.)


Para seguir com os exemplos, utilizarei as bibliotecas <b>matplotlib</b>, <b>numpy</b> e <b>pandas</b>.

<h3>instalação das bibliotecas:</h3>

<table class="table" style="width: 300px; display: table-row-group;">
    <thead>
        <tr>
            <th>pip</th>
            <th>anaconda</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>pip install matplotlib</td>
            <td>conda install -c conda-forge matplotlib</td>
        </tr>
        <tr>
            <td>pip install numpy</td>
            <td>conda install -c conda-forge numpy</td>
        </tr>
        <tr>
            <td>pip install pandas</td>
            <td>conda install -c conda-forge pandas</td>
        </tr>
        <td></td>
    </tbody>
</table>

Lembrando que se você estiver utilizando <b>jupyter notebook</b> algumas bibliotecas podem já estar instaladas como por exemplo: numpy, math e talvez até o pandas, pois o jupyter é uma ferramenta para análise de dados, mas caso não estejam instaladas use os comandos acima.



# Importando as bibliotecas

Após as devidas instalações, podemos seguir com as importações das bibliotecas necessárias para o nosso caso.

O Primeiro passo é configurar a plotagem interativa no jupyter notebook, utilize o comando a seguir:

<b>%matplotlib notebook</b>

você pode importar dessa maneira as bibliotecas:
- import numpy
- import matplotlib
- import pandas

Porém, as comunidades do Python sugerem uma pequena padronização mais conhecidas como convenções.

# Convenções das comunidades Python
Algumas configurações rápidas podem ser feitas nos projetos com Python, sejam para nomeclaturas de variáveis e funções ou até mesmo para importações das bibliotecas, por exemplo, suponha que eu nomeasse como "calcular" uma função responsável por calcular x + y, para quem está codificando será fácil entender o que essa função faz, mas conforme o projeto evolui e mais pessoas começam a trabalhar no código você concorda que "calcular" pode ser um nome genérico? portanto haveria a necessidade de deixar este nome mais explícito pois poderá existir mais funções para cálculos e pode gerar confusão. Um dos princípios do Zen do Python é "Explícito é melhor que implícito".

Pois bem, a palavra <b>numpy</b> é relativamente pequena, mas por convenção podemos encurtar mais ainda e padronizar nossos projetos de acordo com as comunidades do Python sugerem e usam.

É sempre recomendável que siga as converções das comunidades independente de qual linguagem seja, pois assim quando outros programadores precisarem realizar manutenções ou simplesmente entender seu código terão facilidade. Portanto, utilize os comandos abaixo para importar as bibliotecas:

- import numpy as np
- import matplotlib.pyplot as plt
- import pandas as pd

Perceba a inclusão de <b>"as np</b> e <b>as plt"</b>, como eu disse, é uma forma de encurtar os nomes em Python e também bastante utilizado entre os programadores.

Além disso percebam também a inclusão de <b>".pyplot"</b> depois de matplotlib. Isso é para que possamos utilizar apenas recursos de plotagem pytplot sem a necessidade de importar as demais funções da biblioteca."


## Importação das bibliotecas:
<p>import numpy as np</p>
<p>import matplotlib.pyplot as plt</p>
<p>import pandas as pd</p>

## Reforçando
Antes de plotar o gráfico, garanta que a importação do <b>matplotlib</b> esteja como <b>matplotlib.pyplot</b> para que as funções pyplot sejam chamadas na importação. Caso contrário você receberá o erro:

<p><b>AttributeError</b>: module 'matplotlib' has no attribute 'plot'</p>

<span align="center">
  <img src="https://user-images.githubusercontent.com/80490529/222750639-f5217bd2-6975-4227-91f1-8a82f0fd2cb7.png" />
</span>


# Primeiros exemplos de plotagens

Quando se fala em plotar um gráfico, claramente estamos querendo visualizar dados e, para isso se faz necessário passar alguns dados como argumentos para as funções do matplotlib.

Quais tipos de dados podemos utilizar?<br>
É comum plotarmos valores do tipo: <b>int, float, decimal</b> e etc, no geral são valores numéricos.

Para os exemplos a seguir estarei gerando dados aleatórios com o auxílio das funções da biblioteca numpy.

Neste primeiro exemplo irei criar um gráfico de linha simples, para isso os dados da plotagem estarão armazenados na variável <b>"data"</b>.

Utilize o comando abaixo para gerar um array com números inteiros de 0 a 40 intercalando de 2 em 2:

<br><b>entrada</b>:<br>data = np.arange(0, 40, 2)
<br>print(<b>data</b>)
    
<br><b>saída:</b><br>array([ 0,  2,  4,  6,  8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32,
       34, 36, 38])
 
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222756556-e011f675-87cc-4bd5-bf43-d7e9b3419b06.png" />
</span>
  
<br>Se estiver utilizando <b>jupyter notebook</b> não há necessidade de usar o print, apenas chame o nome da variável para imprimir o valor dela.

# Gerando o primeiro gráfico

Conforme mencionado, para plotarmos um gráfico é necessário passar dados para a função do matplotlib.

Utilizaremos o comando <b>plt.plot</b> e passaremos nossa variável <b>data</b> como argumento da função.

Use o comando abaixo para gerar o gráfico:

<b>plt.plot(data)</b>
    
    
# Exemplo 1 - gráfico de linha simples<br>
<img src="https://user-images.githubusercontent.com/80490529/222770540-bc92bace-cab2-4dc1-83bd-9362474bfc00.png" />
    
Percebam como é simples, criei um array e passei como argumento na função do matplotlib.
    
Assim com a função é simples o resultado é relativamente simples, digo, gerou um gráfico simples também que talvez para um caso ou outra sirva, porém, quando estamos explorando dados o ideal é que quanto mais detalhes melhor.
    
Dito isso, a biblioteca do matplotlib proporciona outras formas de criar gráficos, vou me aprofundar no conceito de Figuras.
    
# Figure & Subplots
Veja este comando abaixo:<br>
    <b>fig = plt.figure()
        
Se trata de um comando simples que armazenará na variável um objeto do tipo Figure, isto garante maior versatilidade.
        
O que quer dizer?
        
Quer dizer que agora teremos uma série de opções para configurar nossa figura. Como você deve imaginar a variável <b>fig</b> armazenou o objeto que iremos utilizar no próximo exemplo.

Para criamos um gráfico dentro de uma figura é necessário criar um ou mais <b>subplots</b>.<br>
A função <b>add_subplot</b> adiciona um subplot dentro da nossa figura, acompanhem:

# Exemplo de subplot
<br>Comando:
    <b><br>fig = plt.figure()
    <b><br>fig.add_subplot(2, 2, 1)
        
<br>Saída:
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222777887-65caa1fc-b439-4b16-a7bd-f942c9cd377f.png" />
</span>
        
Este comando cria uma subárea de plotagem na proporção 2x2, ou seja, não teremos apenas um, mas sim quatro gráficos dentro de uma figura.
        
- 2x2: representa a quantidade de subplotagens dentro de uma figura;
- 1: representa qual área do subplot iremos utilizar.
        
        
Seguindo essa lógica, podemos criar até 4 subplots dentro da nossa figura:
<br><br>fig = plt.figure()
<br>fig.add_subplot(2, 2, 1)
<br>fig.add_subplot(2, 2, 2)
<br>fig.add_subplot(2, 2, 3)
<br>fig.add_subplot(2, 2, 4)

Saída:
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222782907-9ecb4f0c-75d8-455b-af21-afee97c95d38.png" />
</span>
        
Obveamente podemos criar uma figura e adicionar mais subplots basta mudarmos as proporções. Neste exemplo irei utilizar a proporção (2, 3, 1):
        
<br><br>fig = plt.figure()
<br>fig.add_subplot(2, 3, 1)
<br>fig.add_subplot(2, 3, 6)
 
Imaginem uma matriz 2D, é exatamente a mesma lógica, se trata de uma estrutura de dados com duas dimensões.
        
Neste exemplo teremos até 6 platagens dentro da mesma figura. Em destaque os subplots 1 e 6:
        
Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222784639-806a2a01-1c1e-4fe1-941d-ce86e7cb8960.png" />
</span>

    
Seguindo a mesma lógica o comando abaixo criará um área com o preenchimento total de 6 subplots: 
        <br><br>fig = plt.figure()
        <br>fig.add_subplot(2, 3, 1)
        <br>fig.add_subplot(2, 3, 2)
        <br>fig.add_subplot(2, 3, 3)
        <br>fig.add_subplot(2, 3, 4)
        <br>fig.add_subplot(2, 3, 5)
        <br>fig.add_subplot(2, 3, 6)

Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222785931-c2b76be7-bb9a-4dc8-b0d6-209bae2275f2.png" />
</span>

        


