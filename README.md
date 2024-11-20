# Analise Bibliometrica e Modelagem/Otimização do Poli(succinato de butileno)(PBS)

# Objetivo
### Criação de uma análise bibliométrica sobre o PBS e reproduzir a  otimização da etapa de transesterificação na síntese do PBS feita em outro software pago por Ferreira (2013).


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

#### Na figura 11, a análise dos termos relacionados ao PBS revela uma ênfase significativa nas propriedades mecânicas desse polímero. Termos como "MECHANICAL-PROPERTIES," "BEHAVIOR," "CRYSTALLIZATION," "MORPHOLOGY" e "PERFORMANCE" lideram as ocorrências, destacando a importância atribuída ao entendimento aprofundado e à melhoria das características mecânicas do PBS. Como discutido na Fundamentação Teórica , a aplicação principal do PBS em embalagens pode explicar essa ênfase, pois as propriedades mecânicas desempenham um papel crucial nesse contexto. Além disso, a abordagem pode visar superar as limitações mecânicas inerentes ao PBS.Outros termos relevantes, como "COMPOSITES," "BLENDS" e "NANOCOMPOSITES," indicam uma abordagem que envolve a incorporação de outros compostos para aprimorar ainda mais as propriedades mecânicas do PBS. Essa estratégia é consistente com a busca por soluções que possam expandir as aplicações práticas do PBS, especialmente em setores onde demandas mecânicas mais robustas são necessárias.O termo "DEGRADATION" surge como o segundo mais frequente, corroborando a aplicação do PBS na formulação de polímeros degradáveis. Essa ênfase na degradação está alinhada com a natureza ambientalmente amigável do PBS, que se decompõe de maneira mais eficiente em comparação com polímeros convencionais.Destaca-se também o termo "LIFE-CYCLE ASSESSMENT" como o décimo mais recorrente, indicando uma abordagem que vai além das propriedades intrínsecas do PBS. Isso sugere investigações sobre o impacto ambiental global do PBS, possivelmente em comparação com outros polímeros, alinhando-se à preocupação crescente com a sustentabilidade e o ciclo de vida completo dos materiais.Em síntese, a Figura 11 reforça os temas abordados na Fundamentação Teórica , evidenciando uma considerável atenção às propriedades mecânicas do PBS, bem como uma forte orientação para aplicações que buscam mitigar impactos ambientais por meio de suas propriedades degradáveis.



##  Mapa temático

![Mapa temático](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Mapa%20tem%C3%A1tico.png)

#### Na Figura 12, destacando os termos "mechanical-properties" e "degradation" como temas motor e "life-cycle assessment" como um tema básico nas pesquisas sobre PBS. A notável recorrência desses termos indica a contínua ênfase na compreensão e aprimoramento das propriedades mecânicas do PBS, bem como na avaliação abrangente de seu impacto ambiental ao longo do ciclo de vida. Quanto aos termos "nanoparticles," "release" e "delivery", é possível estabelecer conexões entre eles, nas aplicações em drug-delivery, especialmente na área biomédica. Contudo, a associação de "nanoparticles" também com "nanocomposites" indica uma amplitude de aplicação para o PBS. A categorização desses termos como temas emergentes sugere que as pesquisas sobre aplicações de drug-delivery e nanotecnologia com PBS podem ser mais recentes ou terem se desenvolvido recentemente.Os termos pertencentes ao tema de nicho, como "removal," "toxicity" e "oxidation", estão intrinsecamente relacionados a questões ambientais. Embora esses temas sejam desenvolvidos, a sua menor relevância em comparação com os temas motores, como as propriedades mecânicas, indica que as preocupações ambientais associadas ao PBS podem ser áreas de pesquisa consolidadas, porém com menor destaque.

# Modelagem

#### Segundo Ferreira (2013), a síntese do PBS foi realizada em duas etapas, ambas empregando um sistema fechado. Na primeira etapa, o pré-polímero foi preparado por esterificação em um reator de três bocas imerso em um banho de silicone. A temperatura do meio reacional foi controlada utilizando um termopar acoplado a uma placa de aquecimento IKA, enquanto um condensador foi utilizado para evitar a perda de reagentes. Foi aplicada agitação magnética e um fluxo de nitrogênio com pressão de aproximadamente 0,75 bar. A mistura reacional consistia em uma quantidade equimolar previamente testada (0,304 mol) de ácido succínico e 1,4-butanodiol, com a temperatura ajustada para 150°C. Durante a reação de esterificação, que durou 5 horas, a água, subproduto da reação, foi removida e coletada por meio de um condensador, com sucção a vácuo, enquanto é continuamente resfriado com nitrogênio líquido para condensar os vapores removidos do meio reacional.No sistema fechado, uma placa de aquecimento foi utilizada juntamente com um fluxo de nitrogênio diretamente no meio reacional. O vácuo foi aplicado por meio de uma bomba. Para condensar os vapores, um balão foi imerso em um banho de etanol com gelo na saída do condensador. O condensador foi continuamente resfriado em contato com nitrogênio líquido. Os produtos sintetizados foram dissolvidos em clorofórmio, precipitados em excesso de etanol em um banho de gelo para obter um produto mais puro. O precipitado foi então lavado com etanol e seco em vácuo à temperatura ambiente por 24 horas, na Figura 6 e mostrado um fluxograma simplificado de como ocorreu a esterificação. Na segunda etapa, a transesterificação, ocorreu a policondensação do pré-polímero utilizando tetrabutoxititânio (Ti(OBu)4) como catalisador, também foram testados outros catalisadores, porém o tetrabutoxititânio foi o que apresentou melhores resultados, sendo utilizado apenas ele. Inicialmente, adicionou-se 0,1% mol do catalisador ao meio reacional a 150°C. Posteriormente, a temperatura foi gradualmente aumentada para 200°C e mantida nesse patamar por 12 horas, após essa etapa a massa molar ponderal média é medida através da cromatografia de permeação em gel, que permite a separação e a determinação do peso molecular dos polímeros em solução, na Figura 7 e mostrado um fluxograma simplificado de como ocorreu a transesterificação.Pela descrição da síntese, temos seis variáveis de interesse: Temperatura do meio reacional, Tempo de reação, Pressão do nitrogênio, Vácuo, Quantidades dos reagentes e Catalisador. A escolha dos fatores temperatura e catalisador se baseia em considerações industriais e científicas relevantes, onde na obtenção de PBS de alta massa molar, destaca-se o uso de catalisadores eficientes, como à base de titânio, frequentemente empregados em quantidades significativas (100-360 ppm), visando minimizar a exposição do polímero a altas temperaturas e reduzir a degradação no reator, embora essa abordagem possa resultar em polímeros com baixa estabilidade térmica. Assim, a seleção dos fatores temperatura e catalisador neste estudo visa otimizar a síntese do PBS, explorando como esses parâmetros podem ser ajustados para alcançar uma massa molar desejável sem comprometer outras propriedades importantes do polímero, como a estabilidade térmica e a biodegradabilidade (Jacquel et al., 2011). Na Figura 8 é mostrado o sistema utilizado por Ferreira (2013).mostra os valores e níveis dos parâmetros avaliados no planejamento experimental e as respostas em termos de massa molar, para o planejamento experimental feito por Ferreira (2013), utilizando o software Statistica 7.0.

![Planejamento Composto Central](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Planejamento%20Composto%20Central.jpg)


## Criação do DataFrame
#### Com os dados experimentais, foi feito um dataframe, apesar do pacote rsm criar planejamentos CCD ele só consegue criar planejamentos 2^x, que impede a criação do desse planejamento pelo pacote já que ele tem 7 experimentos apenas, assim foi feito um dataframe.

```
Ordem <- c(1, 2, 3, 4, 5, 6, 7) # Cria uma varivel com o indice dos experimentos
T <- c(-1, -1, 1, 1, 0, 0, 0) # Cria uma varivel com os níveis de temperatura dos experimentos
C <- c(-1, 1, -1, 1, 0, 0, 0)# Cria uma varivel com os níveis de catalisador dos experimentos
y <- c(13419, 18950, 16381, 17675, 16422, 16673, 16852) # Cria uma varivel com os níveis de massa molar dos experimentos 
df <- data.frame(Ordem, T, C, y) # Criar o dataframe com as variaveis acima
print(df) # Mostra o dataframe
```
![Df](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/df.png))

## Criação e Avaliação do Modelo

### Regressão Linear 
```
modelo1 <- lm(y~T*C,data=df)# Realiza a Regressão no df, com y como resposta e T e C variaveis independentes
summary(modelo1) # Mostra o resultado da Regressão
```
![Resutados da Regressão Linear](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/Resutados%20da%20Regress%C3%A3o%20Linear.jpg)

#### Na Tabela 3, são fornecidos os modelos de regressão. Na dissertação de Ferreira (2013), também foi conduzida uma análise de regressão linear utilizando o software Statistica 7.0 ®. Portanto, a Tabela 3 apresenta os resultados de ambos os softwares para fins de comparação. As linhas representam a constante (K) como termo independente do modelo e as variáveis independentes incluídas na equação de regressão. Mais especificamente, na segunda coluna da Tabela 4, são listados os coeficientes (regressores) de cada variável independente. Na terceira coluna, são indicados os erros padrão de cada coeficiente, enquanto na última coluna, são exibidos os valores p. O valor p registrado nesta coluna deve ser inferior ao nível de significância escolhido, usualmente, considerando-se um valor crítico de p menor ou igual ao nível de significância de 0,05. Em outras palavras, é aceitável até 5% de chance de erro (Reis, 2013).
#### Ao comparar os valores obtidos no Statistica 7.0® e no RStudio, observamos que as estimativas são estatisticamente iguais, e os erros padrão e os valores p são bastante similares entre as duas plataformas. Quaisquer diferenças numéricas podem ser atribuídas a arredondamentos ou métodos específicos de cálculo em cada software. No entanto, as tendências gerais e os padrões dos resultados são consistentes. Em ambos os casos, os valores p foram menores que 0,05 em todas as linhas, indicando que essas variáveis são estatisticamente significativas.
#### A partir das estimativas da regressão, é possível formular uma equação para prever a resposta, apesar de ter formulado um modelo, Ferreira (2013), não testou posteriormente. Como as estimativas são iguais em ambas as plataformas, a equação de regressão é a mesma para ambas, a Equação 2:
#### Mw = 16620,71+421,75∙T+1706,25∙C-1059,52∙C∙T


### Avaliação do Modelo
```
anov <- aov(modelo1) # Realiza o ANOVA no modelo criado
summary(anov)# Mostra os resultados do ANOVA
shapiro.test(modelo1$residuals) # Realiza o teste de shapiro-wilk
bptest(modelo1) # Realiza o teste de breuch-pagan
```

![ANOVA](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/ANOVA.jpg)

#### a ANOVA, um método que decompõe a variância total e seus graus de liberdade em partes atribuídas aos fatores controlados (os tratamentos) e a uma parte denominada de resíduo, que está relacionada a uma causa não controlada. Os graus de liberdade são definidos como o número de observações menos o número de parâmetros estimados. A soma de quadrados mede a variação dos dados, e o quadrado médio é a razão entre a soma de quadrados e os graus de liberdade. A estatística F é baseada na razão dos quadrados médios (Dutra, 2023). Os resultados da ANOVA são apresentados na Tabela 4.
#### De acordo com Govaerts et al. (2020), a análise de variância (ANOVA) é primariamente empregada para avaliar a influência estatística de um conjunto de fatores sobre uma resposta quantitativa, com o objetivo principal de determinar a importância e a significância de cada efeito identificado. Com base nisso, a conclusão pode ser tirada da Tabela 5 de que, considerando um nível de significância de 5%, os efeitos principais e a interação do modelo foram estatisticamente significativos. Portanto, pode-se inferir que há uma diferença significativa na massa molar com base nos níveis de Catalisador (C) e no Temperatura (T).
#### Após a realização da ANOVA, foi conduzido o teste de normalidade utilizando o teste de Shapiro-Wilk. Este teste verifica se os resíduos do modelo seguem uma distribuição normal, sendo um dos métodos mais comuns para verificar a normalidade. 
#### O teste é executado com as seguintes hipóteses:
#### H0: Os dados seguem uma distribuição normal.
#### H1: Os dados não seguem uma distribuição normal.
#### O valor-p do teste de Shapiro-Wilk foi calculado como 0,15, como mostrado na Figura 13, o que significa que é maior que o nível de significância de 5%. Portanto, não rejeitamos a hipótese nula, indicando que há evidências para acreditar que os resíduos do modelo seguem uma distribuição normal.

![Shapiro-Wilk](https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Shapiro-Wilk.png)

#### Além disso, foi realizado o teste de homocedasticidade para avaliar se a variância dos resíduos é constante em todas as combinações dos níveis dos fatores. Este teste é importante porque a análise de variância requer o pressuposto de variâncias homocedásticas. As hipóteses a serem testadas são:
#### H0: A variância é constante (homocedasticidade).
#### H1: A variância não é constante (heterocedasticidade).
#### O teste de homocedasticidade foi realizado usando o teste de Breusch e Pagan, o resultado do teste de Breusch e Pagan foi de 1, como mostra a Figura 14, considerando o nível de significância de 5%, não rejeitamos a hipótese nula, indicando que a variância é constante.

![Breuch-Pagan]((https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Breusch-Pagan.png))


## Otimização
#### A otimização foi realizada por superfieciede resposta, apesar de poder ser contruida com o modelo1, par uma melhor visulaização, foi criado o modelo2 agora com os valores nas variaveis em vez dos niveis.

### Criação do Modelo2 para melhor visualização
```
T1<-c(200,200,250,250,225,225,225)
C1<-c(0.1,0.3,0.1,0.3,0.2,0.2,0.2)
y <- c(13419, 18950, 16381, 17675, 16422, 16673, 16852)
modelo2 <-lm(y~T1*C1) 
persp(modelo2,C1~T1,zlab="MW",col=rainbow(50), contours="colors")
legend("bottomright",legend=c("C1−Catalisador","T1−Temperatura"), cex=0.75, pt.cex=0.75)
```
##### A superfície de resposta construída para o modelo é mostrada na Figura 16, revelando as condições em relação à massa molar obtida. Observa-se que, para alcançar uma massa molar mais elevada, a temperatura não necessariamente precisa estar em seu nível mais alto, mas o catalisador sim. Por outro lado, para uma massa molar mais baixa, é necessário que ambas as variáveis estejam em seus níveis mais baixos. Para massas molares intermediárias, observa-se uma combinação de fatores. Por exemplo, para obter uma massa de 16000 D, é necessário ter a temperatura em seu nível mais elevado e o catalisador em um nível intermediário, aproximadamente 0,2%p/p.

![Superfície de Resposta](https://github.com/AEAA17/Modelagem/blob/94d23773bfed4c358c4e6c8bd8a9984c6d882497/Imagens/SR.png)

#### Além disso, no trabalho de Ferreira (2013), também é apresentada uma superfície de resposta obtida a partir da mesma equação de regressão, porém seus valores foram normalizados, mas essa superfície de resposta apresenta o mesmo padrão,  e pode ser observada na Figura 17.

![Superfície de resposta do Statistica 7.0](https://github.com/AEAA17/Modelagem/blob/41a75cb457deaf7f1403c773da453af58cc5ce87/Imagens/Superf%C3%ADcie%20de%20resposta%20do%20Statistica%207.0.png)
