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

A questão de complexidade na classificação eleva-se quando os espectros pertencem a períodos distintos de observação, ou seja, quando estão antes do período do brilho máximo e depois do período de brilho máximo. Isto ocorre, pois as características de formato, de elementos e de intensidades das explosões de supernovas mudam completamente. Desta maneira é difícil executar uma avaliação acurada de tipos espectrais, principalmente, na identificação das importantes supernovas Ia.
A tabela 1 ilustra como as fases de supernovas podem ser divididas no decorrer do tempo.
IMAGENS...
<p align="center"> Tabela 1 - Definição das Fases espectrais</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/phases.png">
</p>

<p align="center"> Fonte: Blondin (2012)</p>

A figura 2 ilustra um quadro para alguns exemplos das imagens de espectros da supernova de tipo Ia SN 1994ae, ilustrando cada espectro em uma de suas fases definidas na tabela 1.

<p align="center"> Figura 2 - Plotagem das Fases da Supernova Ia SN 1994ae</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/phases.png">
</p>

<p align="center"> Fonte: Blondin (2012)</p>

A figura 2 ilustra uma mudança considerável nos espectros no decorrer do tempo, existe a correlação entre os padrões de supernova na Fase inicial, Pré-Maximo e na fase de Máximo, isto se dá devido ao inicio da explosão e da grande energia inicial gerada no fenômeno. Entretanto, conforme a explosão progride a matéria e gases ionizados são ejetados para o meio interestelar e o remanescente se transforma drasticamente de uma explosão homogênea para uma dispersão do gás. A figura 3 ilustra transformação da explosão da supernova SN 2014J no decorrer do tempo.

<p align="center"> Figura 3 - Evolução da explosão da supernova SN 2014J</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/phases.png">
</p>

<p align="center"> Fonte: Blondin (2012)</p>

## Dados

Os espectros de luz das SNs foram obtidos no repositório aberto The Open Supernova Catalog [], atualmente mantido por dois pesquisadores do Harvard-Smithsonian Center for Astrophysics (CfA). O acervo é uma coletânea dos dados de 17 bases de espectros mais contribuições individuais. Nele, estão disponíveis espectros de SNs dos tipos Ia, Ib, Ic, II e os tipos classificados apenas por fotometria. A Tabela 2 discrimina a quantidade de dados que foram obtidos para utilização no classificador.

<p align="center"> Tabela 2 - Dados espectrais de supernovas</p>

<p align="center">
<img src="https://github.com/LuisRicardoAF/Luis_Ricardo_DataScience_Files/blob/master/phases.png">
</p>

<p align="center"> Fonte: Blondin (2012)</p>

## Proposta

