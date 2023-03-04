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
  
  
# Criando uma figura com mais subplots
Podemos criar mais subplots basta mudarmos as proporções. Neste exemplo irei utilizar a proporção (2, 3, n):

<br><br>fig = plt.figure()
<br>fig.add_subplot(2, 3, 1)
<br>fig.add_subplot(2, 3, 6)
 
 
Neste exemplo teremos até 6 platagens dentro da mesma figura. Em destaque os subplots 1 e 6:
        
Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222784639-806a2a01-1c1e-4fe1-941d-ce86e7cb8960.png" />
</span>

    
Seguindo a mesma lógica o comando abaixo criará uma área com preenchimento total de 6 subplots: 
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


Assim como a variável <b>fig</b> está armazenado a figura, é possível criar cada subplot em uma variável diferente.

<br><br>fig = plt.figure()
<br>ax_1 = fig.add_subplot(2, 2, 1)
<br>ax_2 = fig.add_subplot(2, 2, 2)
<br>ax_3 = fig.add_subplot(2, 2, 3)
<br>ax_4 = fig.add_subplot(2, 2, 4)

Cada subplot é independente do outro, ou seja, não há uma ordem para utilizarmos eles.


# Outras maneiras de criar figuras e subplots

Uma maneira simplificada de realizar o mesmo processo é criarmos um array numpy que armazenará os objetos com subplots.

Veja o exemplo abaixo:

<br>fig, axes = plt.subplots(2, 3)

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222856072-740cd61a-74b6-479c-80dc-4264c082da31.png"/>
</span>

Com apenas uma linha a instrução passada armazenará a figura na variável <b>fig</b> e <b>axes</b> armazenará os subplots.

# Ajustando as áreas de plotagem

Observem que algumas configurações são criadas e exibidas automaticamente nos gráficos, percebam que em nenhum momento passamos os valores dos eixos y e x, os espaçamentos entre os subplots também são automáticos, porém podemos ajustar conforme nossas necessidades.

A seguir mostrarei algumas configurações básicas e bastante utéis:

1) nrows - Número de linhas no gráfico.
2) ncols - Número de colunas no gráfico.
3) sharex - Um boolean que define se os subplots compartilham o mesmo eixo x.
4) sharey - Um boolean que define se os subplots compartilham o mesmo eixo y.
5) subplot_kw - Um dicionário de argumentos adicionais que pode ser passado para a função add_subplot.
6) gridspec_kw - Um dicionário de argumentos adicionais que pode ser passado para a função GridSpec.
7) **fig_kw - Um dicionário de argumentos adicionais que pode ser passado para a função criar figura.
8) layout - Um array de tuplas que especifica a localização de cada subplot no gráfico.
9) squeeze - Um boolean que define se os subplots devem ser ajustados para caber no

Observem os argumentos <b>sharex</b> e <b>sharey</b>, conforme a descrição mostra, são argumentos do tipo boolean (False/True) que tem como objetivo compartilhar os eixos X e Y dos subplots, acompanhe o exemplo abaixo:

# Compartilhandos apenas eixos X
<br>fig, axes = plt.subplots(nrows = 2, ncols = 3, sharex = True)

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863179-994b1627-1702-4b9b-bff9-ffcaaf534a55.png" />
</span>

# Compartilhandos apenas eixos Y
<br>fig, axes = plt.subplots(nrows = 2, ncols = 3, sharey = True)

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863275-6d846969-75c7-4059-9d99-78daadd1f42f.png" />
</span>


# Compartilhandos eixos Y e X
<br>fig, axes = plt.subplots(nrows = 2, ncols = 3, sharex = True, sharey = True)

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863460-722d082d-f18e-496d-ab2d-483844db5590.png" />
</span>

# Ajustando espaçamentos entre os subplots
<br>fig, axes = plt.subplots(nrows = 2, ncols = 4, sharey=True, sharex=True)
<br>fig.subplots_adjust(wspace=0, hspace=0)

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222864117-e7ee11ff-fe36-4d53-9cc6-d114800f1b90.png" />
</span>

Percebam a nova função chamada "<b>subplots_adjust</b>", ela serve para ajustar os espaçamentos entre os gráficos da figura.


# Definição de cores
...
