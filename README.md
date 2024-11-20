# Análise Bibliométrica e Modelagem/Otimização do Poli(succinato de butileno)(PBS)

# Objetivo
### Criação de uma análise bibliométrica sobre o PBS e reproduzir a  otimização da etapa de transesterificação na síntese do PBS feita em outro software pago por Ferreira (2013)(https://www.ima.ufrj.br/index.php/en/pos-graduacao/teses-e-dissertacoes/dissertacoes/2013/236-estudo-da-influencia-de-parametros-reacionais-na-sintese-do-poli-succinato-de-buteno-pbs-por-metodos-estatisticos-e-preparo-de-nanocompositos-pbs-argila-organofilica-via-polimerizacao-in-situ).


## Instalando e Caregando Bibliotecas
```
install.packages("bibliometrix") # Instala a biblioteca bibliometrix

library("bibliometrix") # Carega a biblioteca bibliometrix

install.packages("rsm") # Instala a biblioteca rsm

library(rsm) # Carega a biblioteca rsm

install.packages("lmtest") # Instala a biblioteca lmtest

library(lmtest) # Carega a biblioteca lmtest

```
# Analise Bibliometrica


```
biblioshiny() # Função para utizar o Bibliometrix
```
#### Essa função abre uma pagina no navegador onde pode se escolher as analises desejadas, aqui foram feitas: produção anual da busca, produção anual por país da busca, termos mais frequentes da busca e mapa temático, para essa busaca, foi utilizado exclusivamente a base Web of Science, devido sua capacidade de poder exportar grandes volumes de artigos, o PBS tem sido objeto de estudo para aplicações que visam mitigar os impactos ambientais. Assim na busca, foram explorados os 5000 artigos mais relevantes relacionados ao PBS utilizando as palavras-chave "biodegradável" e "impacto ambiental" na base de dados Web of Science com intervalo de tempo de 2013-2022

![Bibliometrix](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Bibliometrix.jpg)

##  Produção anual da busca

![Produção anual da busca](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Produ%C3%A7%C3%A3o%20Anual%20da%20busca.png)

#### Observa-se um crescimento quase anual na busca por pesquisas relacionadas ao tema, com exceção dos anos de 2017 e 2019, a variação nos volumes de busca em determinados anos pode indicar flutuações temporárias no interesse ou talvez um redirecionamento momentâneo para outras áreas de pesquisa, essa análise temporal evidencia a relevância persistente do PBS como objeto de estudo, sugerindo uma contínua evolução nas investigações e um comprometimento constante com o aprofundamento do entendimento desse tema.

##  Produção anual por país da busca

![Produção anual da busca](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Produ%C3%A7%C3%A3o%20Anual%20por%20Pa%C3%ADs%20da%20busca.png)

#### Destaca-se a China como o principal produtor de artigos relacionados ao PBS, algo esperado pois a produção de PBS concentra-se predominantemente no continente asiático, sendo a China líder nesse cenário. É interessante notar que, apesar de países com produção menor, como os europeus e americanos, também contribuírem com pesquisas sobre o PBS, evidenciando uma abordagem global para a investigação do PBS.

##  Termos mais frequentes da busca

![Termos mais frequentes da busca](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Termos%20mais%20frequentes%20da%20busca.png)

#### A análise dos termos relacionados ao PBS na figura revela uma forte ênfase em suas propriedades mecânicas. Palavras como "MECHANICAL-PROPERTIES", "BEHAVIOR", "CRYSTALLIZATION", "MORPHOLOGY" e "PERFORMANCE" lideram as ocorrências, destacando o interesse em compreender e melhorar essas características. Isso se explica, em parte, pela principal aplicação do PBS em embalagens, onde as propriedades mecânicas são fundamentais, além de refletir esforços para superar limitações do material.

#### Os termos "COMPOSITES", "BLENDS" e "NANOCOMPOSITES" apontam para estratégias que combinam o PBS com outros materiais, buscando maior desempenho. Já o termo "DEGRADATION", o segundo mais frequente, reforça o papel do PBS como polímero biodegradável, alinhando-se à sua proposta ambientalmente amigável.

#### Por fim, a presença de "LIFE-CYCLE ASSESSMENT" indica um interesse no impacto ambiental do PBS ao longo de todo o seu ciclo de vida, em sintonia com a crescente preocupação com sustentabilidade. Assim, a figura complementa a Fundamentação Teórica, evidenciando tanto o foco nas propriedades mecânicas quanto na busca por aplicações sustentáveis.



##  Mapa temático

![Mapa temático](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Mapa%20tem%C3%A1tico.png)

####  Os termos "mechanical-properties" e "degradation" aparecem como temas centrais, enquanto "life-cycle assessment" surge como um tema básico, indicando o foco em melhorar as propriedades mecânicas do PBS e avaliar seu impacto ambiental ao longo do ciclo de vida.

#### Termos como "nanoparticles", "release" e "delivery" estão conectados a aplicações de drug-delivery, especialmente na área biomédica. A associação de "nanoparticles" com "nanocomposites" amplia o potencial de uso do PBS, sugerindo que pesquisas envolvendo nanotecnologia e aplicações biomédicas sejam mais recentes.

#### Já os termos de nicho, como "removal", "toxicity" e "oxidation", tratam de questões ambientais. Apesar de relevantes, têm menor destaque em comparação com os temas centrais, indicando que pesquisas ambientais sobre o PBS estão mais consolidadas, mas não são o foco principal atual.

# Modelagem

#### Segundo Ferreira (2013), a síntese do PBS foi realizada em duas etapas, ambas em sistema fechado. Na primeira, o pré-polímero foi preparado por esterificação em um reator de três bocas aquecido a 150°C, com controle de temperatura feito por termopar acoplado a uma placa de aquecimento. A mistura equimolar de ácido succínico (0,304 mol) e 1,4-butanodiol foi agitada magneticamente sob fluxo de nitrogênio (0,75 bar), enquanto a água, subproduto da reação, era removida e condensada com auxílio de nitrogênio líquido. O produto foi purificado por precipitação em etanol gelado e seco em vácuo por 24 horas.

#### Na segunda etapa, a policondensação foi conduzida com tetrabutoxititânio (Ti(OBu)₄) como catalisador, escolhido por seu melhor desempenho. Inicialmente, 0,1% mol do catalisador foi adicionado ao meio reacional a 150°C. A temperatura foi então elevada gradualmente para 200°C e mantida por 12 horas. Após essa etapa, a massa molar média foi avaliada por cromatografia de permeação em gel.

#### Ferreira (2013) identificou seis variáveis principais na síntese: temperatura, tempo de reação, pressão do nitrogênio, vácuo, quantidades dos reagentes e catalisador. Os fatores temperatura e catalisador foram escolhidos por sua importância na obtenção de PBS de alta massa molar, otimizando a eficiência do processo e minimizando a degradação do polímero, abaixo é mostrado o planejamento montado com essas variáveis.

![Planejamento Composto Central](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Planejamento%20Composto%20Central.jpg)


## Criação do DataFrame
#### Com base nos dados experimentais, foi construído um dataframe. Embora o pacote rsm seja capaz de criar planejamentos CCD, ele está limitado a planejamentos do tipo 2^x, o que inviabiliza sua utilização para este caso, já que o planejamento possui apenas 7 experimentos. Por isso, a construção do dataframe foi feita manualmente.

```
Ordem <- c(1, 2, 3, 4, 5, 6, 7) # Cria uma variável com o indice dos experimentos
T <- c(-1, -1, 1, 1, 0, 0, 0) # Cria uma variável com os níveis de temperatura dos experimentos
C <- c(-1, 1, -1, 1, 0, 0, 0)# Cria uma variável com os níveis de catalisador dos experimentos
y <- c(13419, 18950, 16381, 17675, 16422, 16673, 16852) # Cria uma variável com os níveis de massa molar dos experimentos 
df <- data.frame(Ordem, T, C, y) # Criar o dataframe com as variáveis acima
print(df) # Mostra o dataframe
```
![Df](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/df.png))

## Criação e Avaliação do Modelo

### Regressão Linear 
```
modelo1 <- lm(y~T*C,data=df)# Realiza a Regressão no df, com y como resposta e T e C variáveis independentes
summary(modelo1) # Mostra o resultado da Regressão
```
![Resutados da Regressão Linear](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Resutados%20da%20Regress%C3%A3o%20Linear.jpg)

#### A Tabela acima apresenta os modelos de regressão utilizados, comparando os resultados obtidos pelo Statistica 7.0® e pelo RStudio. As linhas incluem a constante 𝐾 (termo independente) e os coeficientes das variáveis independentes, listados na segunda coluna. Na terceira coluna, estão os erros padrão, e na última, os valores p. Estes últimos devem ser inferiores ao nível de significância de 0,05, indicando até 5% de chance de erro.

##### A análise mostra que as estimativas de ambos os softwares são estatisticamente iguais, com erros padrão e valores p bastante similares. Pequenas diferenças numéricas se devem a arredondamentos ou métodos de cálculo distintos, mas as tendências gerais são consistentes. Em todas as linhas, os valores p foram menores que 0,05, indicando a significância estatística das variáveis.

##### Com base nos coeficientes da regressão, é possível prever a resposta utilizando a equação fornecida, válida para ambos os softwares: Mw=16620,71+421,75⋅T+1706,25⋅C−1059,52⋅C⋅T


### Avaliação do Modelo
```
anov <- aov(modelo1) # Realiza o ANOVA no modelo criado
summary(anov)# Mostra os resultados do ANOVA
shapiro.test(modelo1$residuals) # Realiza o teste de shapiro-wilk
bptest(modelo1) # Realiza o teste de breusch-pagan
```

#### A ANOVA é um método que decompõe a variância total e seus graus de liberdade em partes atribuídas aos fatores controlados  e ao resíduo, que está relacionado a causas não controladas. Os graus de liberdade são definidos pela diferença entre o número de observações e o número de parâmetros estimados. A soma de quadrados mede a variação dos dados, enquanto o quadrado médio é a razão entre a soma de quadrados e os graus de liberdade. A estatística F é calculada pela razão dos quadrados médios.

#### A ANOVA é usada para avaliar o impacto estatístico de fatores sobre uma resposta quantitativa, com o objetivo de determinar a importância de cada efeito. Na Tabela abaixo, com nível de significância de 5%, observa-se que os efeitos principais e a interação do modelo são estatisticamente significativos. Isso indica que há uma diferença significativa na massa molar com base nos níveis de Catalisador (C) e Temperatura (T).


![ANOVA](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/ANOVA.jpg)

#### Após a ANOVA, foi realizado o teste de normalidade de Shapiro-Wilk, que verifica se os resíduos do modelo seguem uma distribuição normal, sendo um dos métodos mais comuns para essa análise. O teste é baseado nas seguintes hipóteses:
#### H₀: Os dados seguem uma distribuição normal.
#### H₁: Os dados não seguem uma distribuição normal.
#### O valor-p do teste de Shapiro-Wilk foi de 0,15, conforme mostrado na Figura abaixo, que é superior ao nível de significância de 5%. Assim, não rejeitamos a hipótese nula, indicando que os resíduos do modelo seguem uma distribuição normal.


![Shapiro-Wilk](https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Shapiro-Wilk.png)

#### Além disso, foi realizado o teste de homocedasticidade para verificar se a variância dos resíduos é constante em todas as combinações dos níveis dos fatores, o que é essencial para a validade da ANOVA. As hipóteses testadas foram:
#### H₀: A variância é constante (homocedasticidade).
#### H₁: A variância não é constante (heterocedasticidade).
#### O teste de homocedasticidade foi conduzido utilizando o teste de Breusch-Pagan. O valor obtido foi 1, conforme mostrado na Figura abaixo. Com nível de significância de 5%, não rejeitamos a hipótese nula, indicando que a variância é constante.

![Breuch-Pagan](https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Breusch-Pagan.png)


## Otimização
#### A otimização foi realizada por meio de superfície de resposta. Embora pudesse ser construída com o modelo 1, para uma melhor visualização, optou-se por criar o modelo 2, agora utilizando os valores das variáveis em vez dos níveis.

### Criação do Modelo2 para melhor visualização
```
T1<-c(200,200,250,250,225,225,225)
C1<-c(0.1,0.3,0.1,0.3,0.2,0.2,0.2)
y <- c(13419, 18950, 16381, 17675, 16422, 16673, 16852)
modelo2 <-lm(y~T1*C1) 
persp(modelo2,C1~T1,zlab="MW",col=rainbow(50), contours="colors")
legend("bottomright",legend=c("C1−Catalisador","T1−Temperatura"), cex=0.75, pt.cex=0.75)
```
##### A superfície de resposta para o modelo, apresentada na Figura abaixo, mostra as condições em relação à massa molar obtida. Observa-se que, para alcançar uma massa molar mais alta, a temperatura não precisa estar no seu nível máximo, mas o catalisador deve estar. Para obter uma massa molar mais baixa, ambas as variáveis precisam estar em seus níveis mais baixos. Já para massas molares intermediárias, é necessária uma combinação de fatores. Por exemplo, para atingir uma massa de 16.000 D, a temperatura deve estar em seu nível mais alto e o catalisador em um nível intermediário, cerca de 0,2% p/p.

![Superfície de Resposta](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/SR.png)

#### No trabalho de Ferreira (2013), também é apresentada uma superfície de resposta obtida a partir da mesma equação de regressão, mas com valores normalizados. Embora os valores sejam diferentes, o padrão da superfície de resposta é o mesmo, como mostrado na Figura abaixo.

![Superfície de resposta do Statistica 7.0](https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Superf%C3%ADcie%20de%20resposta%20do%20Statistica%207.0.png)
