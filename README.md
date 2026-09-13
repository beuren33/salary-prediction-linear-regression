# Regressão Linear para Previsão de Salário

Este projeto usa regressão linear simples para prever o salário de uma pessoa a partir dos seus anos de experiência. É um dos problemas mais didáticos do machine learning e serve muito bem para entender a ideia central da regressão: encontrar a reta que melhor descreve a relação entre uma variável de entrada e um valor numérico de saída. A ideia prática é direta, informa-se quantos anos de experiência alguém tem e o modelo devolve uma estimativa de salário, baseada no padrão que aprendeu observando muitos casos reais.

## Como funciona

A regressão linear parte do princípio de que existe uma relação aproximadamente reta entre a entrada e a saída, no caso entre experiência e salário. O modelo aprende dois números, a inclinação e o ponto onde a reta cruza o eixo, de forma que a reta resultante passe o mais perto possível de todos os pontos do conjunto de treino. Uma vez ajustada essa reta, prever o salário de um novo valor de experiência é só localizar aquele ponto na reta e ler o valor correspondente.

O fluxo do projeto segue o padrão do scikit-learn. Os dados são carregados, separados entre a feature de experiência e o alvo de salário, e usados para treinar um modelo de LinearRegression. Depois o modelo é usado para fazer previsões em valores de experiência que se quer estimar.

## Dados

A base usada é o Salary Dataset, baixado do Kaggle, que relaciona anos de experiência ao salário correspondente. É um conjunto pequeno e limpo, ideal para focar no conceito da regressão sem a distração de um pré-processamento pesado.

## Resultados

O modelo aprende bem a tendência de que mais experiência acompanha salário maior. Ao pedir previsões para alguns valores de experiência, o resultado ficou coerente e crescente, por exemplo por volta de 38 mil para cerca de 1,4 ano de experiência, 48 mil para 2,5 anos e 60 mil para 3,8 anos. Esses números mostram a reta aprendida em ação, transformando anos de experiência em uma estimativa de salário.

## Como rodar

Instale as dependências:

```bash
pip install -r requirements.txt
```

Depois abra o notebook e execute as células em ordem:

```bash
jupyter notebook notebook/regressao_linear.ipynb
```

O notebook baixa a base do Kaggle pelo kagglehub na primeira execução.

## Estrutura do projeto

```
salary-prediction-linear-regression/
├── notebook/
│   └── regressao_linear.ipynb   # treino e previsao da regressao linear
├── requirements.txt
└── .gitignore
```

## Observações e próximos passos

Por ser um modelo simples, a regressão linear tem seus limites, e o principal deles é justamente supor que a relação é uma reta. Na vida real o salário costuma depender de mais fatores além da experiência, então um passo natural é evoluir para a regressão múltipla, incluindo outras variáveis, ou testar modelos que capturam relações não lineares quando os dados mostram que a reta não é suficiente.
