# ELN22104_2020_2


# Atividade 1
## 

### Exercício 1

Resolução manuscrita do exercício 1.

![Exercício 1](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Exerc%C3%ADcio%201.jpeg)

### Exercício 2

Resolução manuscrita do exercício 2.

![Exercício 2](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Exerc%C3%ADcio%202.jpeg)

### Exercício 3

Resolução manuscrita do exercício 3.

![Exercício 3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Exerc%C3%ADcio%203.jpeg)

### Exercício 4

Resolução manuscrita do exercício 4.

![Exercício 4](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Exerc%C3%ADcio%204.jpeg)

### Exercício 5


#### O que é o NETLIST?

NETLIST nada mais é do que um arquivo texto gerado pelo próprio software que representa o circuito construído. É necessário saber que o software analisa os circuitos conforme a primeira lei de Kirchhoff ou lei dos nós. Assim, o programa identifica os componentes do circuito, seus devidos valores e suas localizações entre os nós que compõem o circuito. A NETLIST pode ser visualizada clicando em View -> SPICE netlist, na aba superior à esquerda. 

#### Como descrever o NETLIST?

Utilizando o circuito abaixo, iremos descrever a netlist do mesmo para um melhor entendimento. Podemos observar que o circuito é composto por dois resistores, que foram representados por R1 e R2 de 2KΩ  e 1KΩ de resistência respectivamente, uma fonte V1 de 5V e dois nós que conectam os componentes, N1 e N2.

![Figura 1](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%201.PNG)

Como descrito anteriormente, o software utiliza a lei dos nós para realizar a análise do circuito, por isso, ele identifica os componentes que se encontram entre os nós e seus valores. Com isso, a NETLIST do circuito é representada como a imagem abaixo.

![Figura 2](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%202.PNG)

#### Quais os componentes básicos implementados do SPICE? (resistor, capacitor, etc...) Como é representado cada um dos componentes? Explique com um exemplo.

Os componentes básicos que são implementados no SPICE são os resistores, capacitores, indutores, diodos e o terra, com exceção do GND, os componentes são representados, respectivamente através das letras R, C, L, D. Vale ressaltar que todos estes componentes podem ser inseridos através da digitação da letra que o representa e o terra pode ser inserido ao teclarmos a letra G.

![Figura 3](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%203.PNG)

#### O que é LABEL de um nó e qual a vantagem de usar o mesmo?

LABEL ou label net é uma ferramenta que possibilita a identificação de qualquer parte do circuito. Na maioria das vezes o LABEL é utilizado para representar os nós do circuito, como pôde ser observado na Figura 2. Desta forma, facilita o entendimento da NETLIST quando o mesmo se encontra muito grande e cheio de componentes.

#### O que é um SUBKT? Faça um exemplo.

SUBCKT é um  subcircuito é utilizado para facilitar a inserção de componentes que serão utilizados constantemente ou que não se encontram disponíveis no SPICE. Os SUBCKTs são muito empregados quando utilizamos os Amplificadores Operacionais, pois desta forma é possível inserir modelos de amp-op de muitos fabricantes diferentes.

![Figura 4](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%204.PNG)

#### Como incluir novos modelos de componentes em um simulador SPICE?

É possível inserir novos modelos de componentes, basta buscar na internet o código do componente desejado e salvar na biblioteca do SPICE com o nome, por exemplo o amp-op lm741. Posteriormente, devemos construir o circuito desejado a partir de um Amp-op básico e, utilizando o comando .lib ou .sub, devemos endereçar o arquivo do componente desejado que foi salvo na biblioteca SPICE. Por fim, temos que cubstituir o nome do amp-op básico pelo nome do novo componente, neste caso lm741.

#### O que é simulação transiente .TRANS? Quando usar? Faça um exemplo.

A simulação transiente . TRANS é utilizada para fazer análise de circuitos não lineares que apresentam regime transitório. Abaixo segue um exemplo de um circuito com e o gráfico do descarregamento do indutor.

![Figura 5](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%205.PNG)

#### O que é simulação DC OPERATING (.OP)? Quando usar? Faça um exemplo.

Este tipo de simulação é utilizado quando nos deparamos com circuitos em corrente contínua, lineares e que não apresentam regime transitório.

![Figura 6](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%206.PNG)

#### O que faz a diretiva .step? Forneça exemplos de utilização.

A diretiva .step serve para analisar uma variável do circuito conforme a variação de algum parâmetro como, a resistência de um indutor ou a capacitância de um capacitor.

![Figura 7](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%207.PNG)

Na figura é possível observar a variação da corrente no resistor conforme varia o parâmetro do resistência.

#### O que faz a diretiva .means? Forneça exemplos de utilização.

Esta diretiva serve para realizar a medição quando uma condição é alcançada. Por exemplo, medir a tensão ou a corrente de um resistor quando o tempo específico é alcançado.

#### O que é a simulação DC sweep (.dc)? Quando usar? Faça um exemplo.

Esta diretiva é utilizada quando queremos variar os valores de tensões das fontes DCs.

![Figura 8](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%209.PNG)

#### Como simular um circuito em diferentes temperaturas de funcionamento?

Para simular um circuito em diferentes temperaturas de funcionamento basta adicionar a diretiva _.step temp_ e adicionar o valor inicial, o final e o passo de incremento, conforme ilustrado na imagem abaixo.

![Figura 9](https://github.com/Hentherlyn-Walter/ELN22104_2020_2/blob/main/Hentherlyn%20Walter/Atividade_1/Imagens/Figura%208.PNG)





