# Desafio de projeto: Trabalhando com Machine Learning na Prática no Azure ML

## ℹ️ Sobre:

Consiste na criação de um modelo de previsão com seus devidos pontos de extremidades configurados. Os passos realizados no processo constam neste README e, no arquivo `.json`, constam os pontos de extremidades.


## ✅ Passos realizados:

> [!IMPORTANT]
>
> - [x] Ter um cadastro na [Azure](https://azure.microsoft.com);
> - [x] Ao logar na conta, criar um **recurso** de `Machine Learning seguindo` as etapas:
>   1. No `MENU`, localizar o link `Create a resource`, em `Categories`, selecionar `AI + Machine Learning` e, por fim, clicar em `Azure Machine Learning` e `create`.
>   2. Preencher ALGUMAS informações da seção `BASIC` como `Resource group` e, em **Workspace details**: `Name`.
>   3. Ir para a seção `Review + Create` e clicar em `create`.
> - [x] Com o recurso criado/deploy finalizado, clicar em `Go to resource` e, por fim, em `Launch Studio` - para criar o modelo de forma automatizada.
> 

<br/>

Dentro do `Machine Learning Studio` é necessário seguir os passos abaixo para criação do modelo:

[x] No `Menu lateral que fica à esquerda` clicar em **ML automatizado** e, em seguida em `+ Nova tarefa de ML automatizada`;

[x] Preencher com as informações fornecidas abaixo:

> DEFINIÇÕES BÁSICAS: **Tipos de dados**

* **Nome do trabalho**: mslearn-bike-automl
* **Nome do experimento**: mslearn-bike-rental
* **Descrição**: Aprendizado de máquina automatizado para previsão de aluguel de bicicletas


>  **origem de dados**

* Selecionar a opção `A partir de ficheiros Web`.



>  **URL da WEB**

* Inserir a URL e avançar: `https://aka.ms/bike-rentals`


>  **Definições** - inserir as informações abaixo.

* **Formato do ficheiro**: Delimitado
* **Delimitador**: Vírgula
* **Codificação**: UTF-8
* **Cabeçalhos de coluna**: Só o primeiro ficheiro tem cabeçalho
* **Ignorar linhas**: Nenhuma


>  **Etapa: Esquema**

* Clicar em `Avançar e criar`.



> **Tipo de tarefa e dados**

* Selecionar `alugueldebicicletas `;
* Tipo de tarefa: `Regressão`
* Tipo: `Tabular`



>  **Configurações de tarefas**

* **Coluna de destino**: rentals (integer)
* Clicar em Exibir definições de configuração adicionais, `desmarcar as opções marcadas` em **Métrica Primária** e, em Modelos Permitidos, marcar as opções `RandomForest` e `LightGBM`.
* **Limites**
 1. **Número máximo de avaliações**: `3`
 1. **Máximo de avaliações simultâneas**: `3`
 1. **Máximo de nós**: `3`
 1. **Limiar de pontuação de métrica**: `0.085`
 1. **Tempo limite de experimentação (minutos)**: `15`
 1. **Tempo limite de iteração (minutos)**: `15`
 1. **Ativar cessação antecipada deve estar** [x] `chequada`.
 1. **Tipo de validação**: `Divisão de validação de preparação`
 1. **Porcentagem de validação dos dados**: `10`


>  **Computador**

* Deixar como `default`.


>  **Revisão**

* Clicar em `Submeter tarefa de preparação`.




## 📖 Referência:

Para a realização do desafio, utilizei a documentação oficial da `Azure Machine Learning` que pode ser acessada clicando [aqui](https://aka.ms/ai900-auto-ml).
