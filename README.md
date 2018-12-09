# Luis_Ricardo_Data_Mining
Repositório para as atividades e trabalho final da disciplina  CAP 359 - Principles and Applications of Data Mining

# Escopo da Disciplina CAP 359 - Principios e Aplicações de Mineração de Dados
## Aluno: Luis Ricardo Arantes Filho - Doutorando CAP INPE

# Classificação e Análise Inteligente de Espectros de Supernovas

## Introdução
Uma supernova termonuclear ocorre apenas em sistemas com mais de uma estrela, onde uma anã branca absorve o Hidrogênio de uma companheira (estrelas que podem estar na sequência principal, no estado de gigante vermelha, ou anã branca), desta forma, quando a massa da anã branca atinge o limite de Chandrasekhar (≈ 1,4 M⨀) a estrela entra em colapso e explode. Supernovas que ocorrem desta maneira são denominadas supernovas de tipo Ia. As condições de formação de supernovas Ia, por meio de anãs brancas são bem definidas. A reação ocorre em estrelas compostas por Carbono e Oxigênio em condições degeneradas. Isto pode ser observado pela análise meticulosa das curvas de luz (magnitude em função do tempo) e do espectro óptico (comprimento de onda em função do fluxo de radiação) que apresentam certa homogeneidade [1, 2, 3].

As curvas de luz permitem a análise no decorrer de aproximadamente 40 a 60 dias após a explosão da estrela. Em contrapartida, pode se analisar o tipo de supernova pelo espectro óptico em poucos dias, no momento em que a explosão atinge o pico de luminosidade máxima [2, 3]

A importância da análise das supernovas de tipo Ia está na constatação deste objeto como sendo uma vela padrão (fontes de luz bem definidas). Supernovas como velas padrão geram implicações cosmológicas referentes a modelos de análise que tratam da taxa a qual se expande o Universo [4, 5]. A análise espectral de supernovas se sobressai em relação à curva de luz, pois permite o estudo de galáxias com redshifts elevados (galáxias que se distanciam no cosmos) assim que a supernova atinge a sua luminosidade máxima, não dependendo de um tempo maior do que cinco dias.

## Problema
Avaliação espectral para identificar as supernovas Ia pode ser feita com acurácia quando o espectro atinge a luz máxima (fase espectral = 0.0 dias), este período tem uma variação de aproximadamente -2.5 a +2.5 dias em relação a luz máxima. Este período foi denominado período de brilho Máximo em [6], pois as classificações em relação aos elementos químicos como o SI e o S são mais evidentes nas supernovas de tipo Ia. 

A questão de complexidade na classificação eleva-se quando os espectros pertencem a períodos distintos de observação, ou seja, quando estão antes do período do brilho máximo e depois do período de brilho máximo. Isto ocorre, pois as características de formato, de elementos e de intensidades das explosões de supernovas mudam completamente. Desta maneira é difícil executar uma avaliação acurada de tipos espectrais, principalmente, na identificação das importantes supernovas Ia. A tabela 1 ilustra como as fases de supernovas podem ser divididas no decorrer do tempo.
<p align="center"> Tabela 1 - Definição das Fases espectrais</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_Data_Mining/blob/master/tabela de fases.png">
</p>

<p align="center"> Fonte: Produção do autor</p>

A figura 1 ilustra um quadro para alguns exemplos das imagens de espectros da supernova de tipo Ia SN 1994ae, ilustrando cada espectro em uma de suas fases definidas na tabela 1.

<p align="center"> Figura 1 - Plotagem das Fases da Supernova Ia SN 1994ae</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_Data_Mining/blob/master/fases.png">
</p>

<p align="center"> Fonte: Produção do autor</p>

A figura 1 ilustra uma mudança considerável nos espectros no decorrer do tempo, existe a correlação entre os padrões de supernova na Fase inicial, Pré-Maximo e na fase de Máximo, isto se dá devido ao inicio da explosão e da grande energia inicial gerada no fenômeno. Entretanto, conforme a explosão progride a matéria e gases ionizados são ejetados para o meio interestelar e o remanescente se transforma drasticamente de uma explosão homogênea para uma dispersão do gás. A figura 2 ilustra transformação da explosão da supernova SN 2014J no decorrer do tempo.

<p align="center"> Figura 2 - Evolução da explosão da supernova SN 2014J</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_Data_Mining/blob/master/gas_dispersao.png">
</p>

<p align="center"> Fonte: Produção do autor</p>

Os remanescentes da explosão são considerados como nuvens de gás com grandes concentrações de energia e por isso provém a denominação de fase nebular. Neste mesmo sentido a luminosidade inicial da supernova é menor, como é mostrada na sua curva de luz. A figura 3 ilustra a curva de luz para 23 supernovas de tipo Ia que ilustram a luminosidade máxima e o decaimento no decorrer dos dias.

<p align="center"> Figura 3 - Curvas de luz para 23 supernovas Ia</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_Data_Mining/blob/master/curva de luz.png">
</p>

<p align="center"> Fonte: Branch (1992)</p>

## Dados

Os espectros de luz das SNs foram obtidos no repositório aberto The Open Supernova Catalog [7], atualmente mantido por dois pesquisadores do Harvard-Smithsonian Center for Astrophysics (CfA). O acervo é uma coletânea dos dados de 17 bases de espectros mais contribuições individuais. Nele, estão disponíveis espectros de SNs dos tipos Ia, Ib, Ic, II e os tipos classificados apenas por fotometria. A Tabela 2 discrimina a quantidade de dados que foram obtidos para utilização no classificador.

<p align="center"> Tabela 2 - Dados espectrais de supernovas</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_Data_Mining/blob/master/tabela de dados.png">
</p>

<p align="center"> Fonte: Gillochon et al.(2017)</p>

## Proposta

Neste sentido, este trabalho propõe uma análise dos dados espectrais de supernovas para a classificação de tipo e de fases de supernovas de forma a criar um sistema seguro que construa relações entre diversas variaveis e possa classificar corretamente cada tipo. Este trabalho busca identificar as principais componentes dos espectros de supernovas, por meio de técnicas de mineração de dados, e assim gerar esquemas de classificação para os tipos Ia, Ib, Ic e II.

## Solução

Neste trabalho buscamos duas soluções distintas para o problema de classificação e análise de fases espectrais em supernovas. Para análise de fases utilizamos uma abordagem voltada a algoritmos de agrupamento. Para a classificação de tipos utilizamos uma abordagem voltada a redes neurais artificiais para classificar os 4 grupos de supernovas.

A ordem de visualização dos notebooks é a seguinte:

### [Manipulando dados brutos de Supernovas](Manipulando dados brutos de Supernovas.ipynb)
### [Relatório_Atividades_Principios_e_Aplicacoes_Mineracao_de_dados](Relatório_Atividades_Principios_e_Aplicacoes_Mineracao_de_dados.ipynb)
### [Extraindo atributos dos DataFrames](Extraindo atributos dos DataFrames.ipynb)
### [Agrupamento de dados - DBscan](Agrupamento de dados - DBscan.ipynb)
### [Redes Neurais para Classificação de Tipos](Redes Neurais para Classificação de Tipos.ipynb)

## Referências
[1]	BAADE, W; ZWICKY, F. On super-novae. Proceedings of the National  Academy of Sciences, v. 20, n. 5, p. 254-259, 1934.

[2]	BRANCH, D.; TAMMANN, G. A. Type Ia supernovae as standard candles. Annual review of astronomy and astrophysics, v. 30, n. 1, p. 359-389, 1992.

[3]	FILIPPENKO, A. V. Optical spectra of supernovae. Annual Review of Astronomy and Astrophysics, v. 35, n. 1, p. 309-355, 1997.

[4]	RIESS, A. G. et al. 1998. Observational evidence from supernovae for an accelerating universe and a cosmological constant. The Astronomical Journal, v. 116, n. 3, p. 1009, 1998.

[5]	PERLMUTTER, S. et al. 1999. Measurements of omega and lambda from 42 high-redshift supernovae. The Astrophysical Journal, v. 517, n. 2, p. 565, 1999.

[6]	ARANTES FILHO, L. R. Classificação Inteligente de Supernovas utilizando Sistemas de Regras Nebulosas. Dissertação (Mestrado em Computação Aplicada) — Instituto Nacional de Pesquisas Espaciais (INPE), São José dos Campos, 2018.

[7] J. Gillochon, J. Parrent, L. Z. Kelley, and R. Margutti. An open catalog for supernova data. The Astrophysical Journal, 835(1):64, 2017
