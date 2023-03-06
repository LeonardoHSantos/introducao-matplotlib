# introducao-matplotlib

# FINALIDADE
Tenho como finalidade apresentar alguns recursos da biblioteca matplotlib e mostrar que pode ser uma boa alternativa durante as análises exploratórias.
 
Na minha visão, entendo que um dos fatores principais que podem impedir o desenvolvimento e implementação de melhorias é a falta de conhecimentos, em específico quando não há interesse em conhecer mais, sabendo disso se você tem preguiça de aprender ou pior não quer aprender, talvez esse material não sirva para você. Fiz com o intuito de replicar meus conhecimentos.

# INTRODUÇÃO
Antes de entendermos o que de fato é matplotlib, preciso esclarecer de onde irei obter os dados e qual ferramenta irei utilizar para os exemplos.

Atualmente quais ferramentas você utiliza para trabalhar com dados? talvez o Pacote Office? Excel e PowerPoint? PowerBI e SQL? Bom, eu já trabalhei com essas e algumas utilizei por tempo suficiente ao ponto de compreender que "para cada necessidade há uma ferramenta apropriada". Afirmo que essas citadas são boas ferramentas sem contar que existem planos gratuitos que servem bem.

### Então para que mudar?

Questão interessante e darei minha visão sobre. Apenas quando conhecemos o potencial de cada ferramenta podemos escolher qual utilizar para determinada atividade. Exemplo, por que utilizar matplotlib?

Quando estamos trabalhando com dados obviamente temos que entender quais tipos de dados estamos analisando e quais informações podemos extrair e assim chegar em resultados significantes. Como a própria palavra diz estamos "extraindo informações" e não criando dashboards e KPIs, ou seja, antes de ir para tomada de decisões e criar painés de controle é interessante entender até onde podemos chegar com os dados disponíveis.

Logo se faz necessário escolher alguma ferramenta que armazena, trata dados e nos possibilita criar visualizações, por isso cabe o uso da biblioteca matplolib pois concentra muitos recursos e dois dos principais são:

- platagem de dados (gráficos);
- possibilidade de utilizar em conjunto com bibliotecas de tratamento de dados tais como pandas e numpy;

Utilizar com essas 2 bibliotecas são de grande ajuda pois nem sempre teremos os dados perfeitamente limpos e no formato que precisamos para criar nossas análises e relatórios.

Pois bem, acredito que assim como já ocorreu comigo, pode ter acontecido ou ainda acontecer com vocês, algumas empresas que trabalhei tinham políticas e regras rígidas no quesito dados, um consenso bem comum era que os gestores das áreas definiam quais níveis de acessos, dados e quais ferramentas iriam disponibilizar para cada área, concordo e apoio, mas para quem já teve dificuldades para trabalhar com arquivos de 1GB ou mais entenderá melhor a diferença que faz ter uma ferramenta apropriada e, que para chegar aos relatórios gerenciais umas das maiores dificuldades podem estar no tempo empregado para tratar os dados e o nível de conhecimentos que precisa ter para trabalhar com uma ou mais ferramentas simultaneamente.

Por alguns anos utilizei apenas os recursos do Pacote Office para realizar tarefas corriqueiras das simples as complexas para tratar, analisar, criar dashboards, automatizar rotinas com macros, VBA e etc. Como eu disse e repito, são boas ferramentas e atenderão suas necessidades muito bem, porém, nunca fui de me contentar com o básico, unindo isso ao fato da valorização tanto do Python quanto do profissional de Data Science, decidi me desenvolver mais com Python e confesso que no início tive um bom desafio, digo, é um pouco desafiador para quem está acomodado com Excel e PowerPoint começar a utilizar novas ferramentas que exigem codificação, entender desde os conceitos mais simples aos mais avançados para estar em um nível profissional.

Ferramentas estão aí para nos ajudar, seja algo simples ou complexo sempre teremos que nos aperfeiçoar, logo entendemos que aprender é uma constante e é muito satisfatório aprender algo e conseguir colocar em prática.


# ALINHAMENTO
Os nomes VsCode e PyCharm são bem conhecidos na área de tecnologia, se tratam de IDE's. Mas para me acompanhar e chegar aos mesmos resultados sugiro que utilizem o Jupyter Notebook, além de ser uma ferramenta desenvolvida para trabalhar com dados é amplamente utilizada sem contar que se algo der errado o Jupyter informa o erro e caso você não consiga resolver poderá contar com a internet, provavelmente alguém já resolveu ou sugeriu algo para solucionar o problema.

# BIBLIOTECAS PYTHON

Se você pesquisar na internet "o que são bibliotecas Python" terá algo assim "As bibliotecas Python são um conjunto de módulos e funções úteis que reduzem o uso de código no programa.". Pode ser que isso cause mais questionamentos do que esclarecimentos. Então "resumindo", quando trabalhamos com desenvolvimento de aplicações independente de qual linguagem estamos programando, há uma série de classes e funções que precisamos desenvolver para entregar pequenas partes de uma aplicação, dito isso, algumas funcionalidades são comuns e podem ser replicadas e escaladas para os projetos, logo, algumas empresas, comunidades, ou até mesmo equipes do projeto podem criar e compartilhar soluções através de pacotes de códigos baseadas nas necessidades comuns e assim otimizar o processo de desenvolvimento dos projetos, sem contar que muitas bibliotecas são desenvolvidas e testadas pelas comunidades e até mesmo utilizadas por grandes empresas de tecnologia, o que torna mais confiável a instalação dos pacotes. Outro detalhe importante, conforme o tempo passsa geralmente são desenvolvidas algumas atualizações dos pacotes com implementações de novas funcionalidades e resolução de bugs, então vale a pena ficar atento e acompanhar o que acontece nas comunidades.

# BIBLIOTECAS AUXILIARES

Para me auxiliar na utilização do matplotlib, irei utilizar as bibliotecas pandas e numpy para gerar e armazenar dados. São amplamente utilizadas para trabalhar com dados devido a versatilizadade e performance.


# MAS AFINAL O QUE É E PARA QUE SERVE O MATPLOTLIB?

Vamos lá, "<b>matplotlib<b> é um pacote de plotagem para desktop, projetada para criar plotagens com qualidade para publicação (em sua maior parte, bidimensionais). O projeto foi criado por John Hunter em 2002 com o intuito de possibilitar uma interface de plotagem do tipo MATLAB em Python. A biblioteca matplotlib aceita vários backends de GUI em todos os sistemas operacionais e, além disso é capaz de exportar visualizações para todos os vetores comuns e formatos de gráficos raster (PDF, SVG, JPG, PNG, BMP, GIF etc.)".

Esta é uma boa descrição que o desenvolvedor de software Wes Mckinney fez no livro "Python para análise de dados".

Nas minhas palavras, matplotlib é um pacote de ferramentas que nos permite criar e configurar gráficos com poucas linhas de código.

# INSTALAÇÃO DAS BIBLIOTECAS DE ACORDO A IDE
Para seguir com os exemplos irei instalar e importar as bibliotecas necessárias.

### vs code ou pycharm: PIP
### JYPYTER NOTEBOOK - ANACONDA PROMPT (anaconda3): CONDA

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
    </tbody>
</table>

Lembrando que se você estiver utilizando <b>jupyter notebook</b> algumas bibliotecas podem já estar instaladas como por exemplo: numpy, math e talvez até o pandas, pois o jupyter é uma ferramenta para análise de dados, mas caso não estejam instaladas use os comandos acima.



# Importando as bibliotecas

Após as devidas instalações, podemos seguir com as importações das bibliotecas necessárias para o nosso caso.

O Primeiro passo é configurar a plotagem interativa no jupyter notebook, utilize o comando a seguir:

<b>%matplotlib notebook</b>

primeiro exemplo de importação, apenas para demonstrar não utilizem ainda:
- import numpy
- import matplotlib
- import pandas

As comunidades do Python sugerem uma padronização mais conhecidas como convenções.

### Convenções das comunidades Python
Algumas configurações rápidas podem ser feitas nos projetos com Python, sejam para nomeclaturas de variáveis e funções ou até mesmo para importações das bibliotecas, por exemplo, suponha que eu nomeasse como "calcular" uma função responsável por calcular x + y, para quem está codificando será fácil entender o que essa função faz, mas conforme o projeto evolui e mais pessoas começam a trabalhar no código você concorda que "calcular" pode ser um nome genérico? portanto haveria a necessidade de deixar este nome mais explícito pois poderá existir mais funções para cálculos e pode gerar confusão. Um dos princípios do Zen do Python é "Explícito é melhor que implícito".

Pois bem, a palavra <b>numpy</b> é relativamente pequena, mas por convenção podemos encurtar mais ainda e padronizar nossos projetos de acordo com as comunidades do Python sugerem e usam.

É sempre recomendável que siga as converções das comunidades independente de qual linguagem seja, pois assim quando outros programadores precisarem realizar manutenções ou simplesmente entender seu código terão facilidade. Portanto, utilizem os comandos abaixo para importar as bibliotecas:

## Importação das bibliotecas:
<pre><code>
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
</pre></code>

Percebam a inclusão de <b>"as np</b> e <b>as plt"</b>, como eu disse, é uma forma de encurtar os nomes em Python e também bastante utilizado entre os programadores.

Além disso percebam também a inclusão de <b>".pyplot"</b> depois de matplotlib. Isso é para que possamos utilizar apenas recursos de plotagem pytplot sem a necessidade de importar as demais funções da biblioteca."

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

Para os exemplos a seguir estarei gerando dados aleatórios com o auxílio das funções da biblioteca numpy e pandas.

Neste primeiro exemplo irei criar um gráfico de linha simples, para isso os dados da plotagem estarão armazenados na variável <b>"data"</b>.

Utilize o comando abaixo para gerar um array com números inteiros de 0 a 40 intercalando de 2 em 2:

comando:
<pre><code>
data = np.arange(0, 40, 2)
print(data)
</pre></code>
    
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
<pre><code>
plt.plot(data)
</pre></code>
    
    
# Exemplo 1 - gráfico de linha simples<br>
<img src="https://user-images.githubusercontent.com/80490529/222770540-bc92bace-cab2-4dc1-83bd-9362474bfc00.png" />
    
Percebam como é simples, criei um array e passei como argumento na função do matplotlib.
    
Assim como a função é simples o resultado é relativamente simples, digo, gerou um gráfico simples também que talvez para um caso ou outra sirva, porém, quando estamos explorando dados o ideal é que quanto mais detalhes melhor.
    
Dito isso, a biblioteca do matplotlib proporciona outras formas de criar gráficos, vou me aprofundar no conceito de Figuras.
    
# Figure & Subplots
Veja este comando abaixo:<br>
<pre><code>
fig = plt.figure()
</pre></code>
        
Se trata de um comando simples que armazenará na variável um objeto do tipo Figure, isto garante maior versatilidade.
        
O que quer dizer?
        
Quer dizer que agora teremos uma série de opções para configurar nossa figura. Como você deve imaginar a variável <b>fig</b> armazenou o objeto que iremos utilizar no próximo exemplo.

Para criamos um gráfico dentro de uma figura é necessário criar um ou mais <b>subplots</b>.<br>
A função <b>add_subplot</b> adiciona um subplot dentro da nossa figura, acompanhem:

# Exemplo de subplot
<br>Comando:
<b>
<pre><code>
fig = plt.figure()
fig.add_subplot(2, 2, 1)
</pre></code>
        
<br>Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222777887-65caa1fc-b439-4b16-a7bd-f942c9cd377f.png" />
</span>
        
Este comando cria uma subárea de plotagem na proporção 2x2, ou seja, não teremos apenas um, mas sim quatro gráficos dentro de uma figura.
        
- (2, 2, ...) significa 2x2: representa a quantidade de subplotagens dentro de uma figura;
- (..., ..., 1): representa qual área do subplot iremos utilizar.
        
        
Seguindo essa lógica, podemos criar até 4 subplots dentro da nossa figura:
<br>
<pre><code>
fig = plt.figure()
fig.add_subplot(2, 2, 1)
fig.add_subplot(2, 2, 2)
fig.add_subplot(2, 2, 3)
fig.add_subplot(2, 2, 4)
</pre></code>

Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222782907-9ecb4f0c-75d8-455b-af21-afee97c95d38.png" />
</span>
  
  
# Criando uma figura com mais subplots
Podemos criar mais subplots basta mudarmos as proporções. Neste exemplo irei utilizar a proporção (2, 3, n):

<br>
<pre><code>
fig = plt.figure()
fig.add_subplot(2, 3, 1)
fig.add_subplot(2, 3, 6)
</pre></code>
 
 
Neste exemplo teremos até 6 platagens dentro da mesma figura. Em destaque os subplots 1 e 6:
        
Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222784639-806a2a01-1c1e-4fe1-941d-ce86e7cb8960.png" />
</span>

    
Seguindo a mesma lógica o comando abaixo criará uma área com preenchimento total de 6 subplots: 
<br>
<pre><code>
fig = plt.figure()
fig.add_subplot(2, 3, 1)
fig.add_subplot(2, 3, 2)
fig.add_subplot(2, 3, 3)
fig.add_subplot(2, 3, 4)
fig.add_subplot(2, 3, 5)
fig.add_subplot(2, 3, 6)
</pre></code>

Saída:<br>
<span align="center">
    <img src="https://user-images.githubusercontent.com/80490529/222785931-c2b76be7-bb9a-4dc8-b0d6-209bae2275f2.png" />
</span>


Assim como a variável <b>fig</b> está armazenado a figura, é possível criar cada subplot em uma variável diferente.

<br>
<pre><code>
fig = plt.figure()
ax_1 = fig.add_subplot(2, 2, 1)
ax_2 = fig.add_subplot(2, 2, 2)
ax_3 = fig.add_subplot(2, 2, 3)
ax_4 = fig.add_subplot(2, 2, 4)
</pre></code>

Cada subplot é independente do outro, ou seja, não há uma ordem para utilizarmos eles.

# Outras maneiras de criar figuras e subplots

Uma maneira simplificada de realizar o mesmo processo é criarmos um array numpy que armazenará os objetos com subplots.

Veja o exemplo abaixo:

<br>
<pre><code>
fig, axes = plt.subplots(2, 3)
</pre></code>

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

# Compartilhando apenas eixos X
<br>
<pre><code>
fig, axes = plt.subplots(nrows = 2, ncols = 3, sharex = True)
</pre></code>

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863179-994b1627-1702-4b9b-bff9-ffcaaf534a55.png" />
</span>

# Compartilhando apenas eixos Y
<br>
<pre><code>
fig, axes = plt.subplots(nrows = 2, ncols = 3, sharey = True)
</pre></code>

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863275-6d846969-75c7-4059-9d99-78daadd1f42f.png" />
</span>


# Compartilhando eixos Y e X
<br>
<pre><code>
fig, axes = plt.subplots(nrows = 2, ncols = 3, sharex = True, sharey = True)
</pre></code>

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222863460-722d082d-f18e-496d-ab2d-483844db5590.png" />
</span>

# Ajustando espaçamentos entre os subplots
<br>
<pre><code>
fig, axes = plt.subplots(nrows = 2, ncols = 4, sharey=True, sharex=True)
fig.subplots_adjust(wspace=0, hspace=0)
</pre></code>

<span>
    <img src="https://user-images.githubusercontent.com/80490529/222864117-e7ee11ff-fe36-4d53-9cc6-d114800f1b90.png" />
</span>

Percebam a nova função chamada "<b>subplots_adjust</b>", ela serve para ajustar os espaçamentos entre os gráficos da figura.


# Utilização das bibliotecas pandas e matplotlib

Agora que já fiz a introdução de como funciona o matplotlib vou criar dados fictícios e converter em DataFrame, é muito útil e nos beneficia ainda mais para criar plotagens.

# Criando o Dataframe

Irei utilizar a biblioteca pandas, portanto, garanta que esteja importada. Lembrando da convenção importar assim: "import pandas as pd".

Os dados de exemplo serão da quantidade de vendas e faturamento de 3 filiais no período de 5 semanas.

# gerando a quantidade de vendas por filial - 5 semanas
<br>comando:
<pre><code>
dados_qt_vendas_ult_5_semanas = np.random.randint(500, 1500, size=(3, 5))
dados_qt_vendas_ult_5_semanas
</pre></code>
<br>
<span>
 <img src="https://user-images.githubusercontent.com/80490529/223018615-468f34d5-7d5f-43a5-9a77-721ba8770af4.png" />
</span>

# gerando o total faturado por filial - 5 semanas
<br>comando:
<pre><code>
dados_tt_faturamento_ult_5_semanas = np.random.randint(5000, 15000, size=(3, 5))
dados_tt_faturamento_ult_5_semanas
</pre></code>
<br>
<span>
 <img src="https://user-images.githubusercontent.com/80490529/223018752-8c514a2d-2341-460d-b236-dc9ea576e21e.png" />
</span>

<br>Legal, já tenho os dados das vendas para 3 filiais. Agora basta criar o DataFrame e para fazer isso existem inúmeras maneiras, demonstrarei uma forma prática e rápida:


# gerando o DataFrame no formato 1:
<br>comando:
<pre><code>
base = {
    "vendas": dados_qt_vendas_ult_5_semanas.flatten(),
    "faturamento": dados_tt_faturamento_ult_5_semanas.flatten()
}
df = pd.DataFrame(
    data=base,
    index=pd.MultiIndex.from_product(
        [ lista_filiais,  range(1, 6) ],
        names=["filial", "semana"]))
</pre></code>
<span>
 <img src="https://user-images.githubusercontent.com/80490529/223018851-7aeb18ea-7aaf-4ffa-9495-6458904255c3.png" />
</span>
 
 
# CRIANDO O PRIMEIRO GRÁFICO UTILIZANDO O PANDAS
 <br>comando:
<pre><code>
fig, axes = plt.subplots(2, 3, figsize=(18, 12))
# df["vendas"].loc["Curitiba/PR"].plot(ax=axes[0, 0], legend="Curitiba/PR", color="g", title= 'Vendas - Curitiba/PR')
df["vendas"].loc["São Paulo/SP"].plot.area(ax=axes[0, 1], legend="São Paulo/SP", color="orange",alpha=1, title= 'Vendas - São Paulo/SP')
df["vendas"].loc["Porto Alegre/RS"].plot(ax=axes[0, 2], legend="Porto Alegre/RS", color="b", title= 'Vendas - Porto Alegre/RS')

df["faturamento"].loc["Curitiba/PR"].plot.bar(ax=axes[1, 0], legend="Curitiba/PR", color="g", title= 'Faturamento - Curitiba/PR')
df["faturamento"].loc["São Paulo/SP"].plot.hist(ax=axes[1, 1], legend="São Paulo/SP", color="orange", alpha=0.5, title= 'Faturamento - São Paulo/SP')
df["faturamento"].loc["Porto Alegre/RS"].plot.pie(ax=axes[1, 2], legend="Porto Alegre/RS", title= 'Faturamento - Porto Alegre/RS')
</pre></code>
 
 <span>
 <img src="https://user-images.githubusercontent.com/80490529/223020675-30c0df58-b1f5-4da1-956d-a026eeb9488d.png" />
</span>
 
Comentei a linha do axes[0, 0] para plotar o gráfico separadamente. Para este axes irei avançar um pouco mais na personalização passando alguns argumentos separados.
 
# PERSONALIZAÇÃO EXCLUSIVA DE AXES
 
Para o axes[0,0] irei personalizar alguns detalhes do gráfico separadamente, percebam que quantidade de instruções aumentam assim como o nível de detalhes no gráfico.
 
 <pre><code>
 df["vendas"].loc["Curitiba/PR"].plot(
    ax=axes[0, 0],
    label='Curitiba/PR',
    fontsize=14,
    alpha=1, color="#0000CD",
    linestyle='-',
    marker='o',
    markersize=4)

# configuração do título do gráfico
axes[0, 0].set_title("Quantidade de Vendas Semana - Curitiba/PR", size=18)

# configuração da legenda do gráfico
# é possível definir a legenda junto com a escolha do axes e personalizar separadamente
axes[0, 0].legend(fontsize=20, loc='lower left')

# definição de novos valores para o eixo X
labels_x = ["1", "A", "2", "2.5", "D", "3.5", "plot", "4.5", "5", "cinco", 6]
axes[0, 0].set_xticklabels(
    labels_x,
    size=14,
    rotation=45
);

# configuração dos títulos dos eixos Y e X
axes[0, 0].set_ylabel('Vendas - Curitiba/PR', fontsize=25)
axes[0, 0].set_xlabel('Curitiba/PR', size=16, color="#0000CD");

fig.subplots_adjust(wspace=0, hspace=0.4)
</pre></code>
 
<span>
 <img src="https://user-images.githubusercontent.com/80490529/223022248-0fb0b244-703e-4b6d-aa92-e30795351163.png" />
</span>
 
 ### POSICIONAMENTOS - LEGENDA
 
Observem que configurei a leganda utilizando o argumento "loc" e passei como parâmetro o valor "lower left".
 
Aqui estão alguns parâmetros que podem ser utilizados para definir a posição da legenda:

 <table class="table" style="width: 300px; display: table-row-group;">
    <thead>
        <tr>
            <th>argumentos</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>best</td>
            <td>upper right</td>
        </tr>
    </tbody>
</table>
 
'best', 'upper right', 'upper left', 'lower left', 'lower right', 'right', 'center left', 'center right', 'lower center', 'upper center', 'center'
 


