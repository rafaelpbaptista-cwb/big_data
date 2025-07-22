# Título: Relatório uso AutoML e biblioteca Spark MLlib

## Aluno: Rafael De Pauli Baptista

## Disciplina: Introdução a Big Data

Relatório detalhando o uso de uma de uma ferramenta de AutoML para uma análise inicial de modelos de machine learning e uma análise um pouco mais aprofundada usando o biclioteca Spark MLlib.

Para a ferramenta de AutoML foi utilizado o [Orange Data Mining](https://orangedatamining.com/).

O dataset selecionado foi os dos sobreviventes do naufrágio do *Titanic*. Foi utilizado uma versão deste dataset disponibilizado pela própria ferramenta *Orange Data Mining*.
Os modelos de machine learning selecionados para o exercício foram *Random Forest* e *Regressão Logística*.

### Análise Exploratória do Conjunto de Dados: Titanic

O dataset utilizado neste estudo contém informações sobre os passageiros do Titanic. Ele traz informações de cada passageiro.

Abaixo, apresentamos uma amostra das 10 primeiras linhas do *dataset* para ilustrar sua estrutura e conteúdo.

#### Amostra dos Dados

| survived | status | age | sex |
|:---|:---|:---|:---|
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |
| yes | first | adult | male |

#### Dicionário de Dados

Os campos (colunas) presentes no dataset são descritos a seguir:

* **survived:** A variável alvo (target) do nosso estudo. Indica se o passageiro sobreviveu ao naufrágio (`yes`) ou não (`no`).
* **status:** Representa a classe socioeconômica do passageiro, que é um indicador do tipo de bilhete adquirido. Pode ser `first` (Primeira Classe), `second` (Segunda Classe),`third` (Terceira Classe) ou `crew` (Tripulação).
* **age:** Categoria de faixa etária do passageiro, como `adult` (adulto) ou `child` (criança).
* **sex:** O sexo do passageiro, registrado como `male` (masculino) ou `female` (feminino).

#### Gráficos relativos aos dados

Segue gráficos exploratórios retirados da ferramenta *Orange Data Mining*.

- Quantidade de sobreviventes

![Quantidade de sobreviventes](./relatorio/imagens/01_Qtdade_sobreviventes.png)