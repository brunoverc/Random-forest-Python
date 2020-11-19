#### brunovercosa.github

# Random Forest

- Random Forest

    - O Grid Search foi utilizado para buscar os melhores parâmetros.

 ```bash
pip install -U scikit-learn
```

## Desenvolvido por

Bruno Nascimento Verçosa

bruno.nv@hotmail.com | bruno@teckavan.com

## Descrição

A perca de clientes é algo que preocupa diversas empresas, com o foco da previsão do cancelamento de um cliente em diversos cenários.
Para o exemplo desse algorítmo foi utilizado a base de dados: Telco-Customer-Churn.csv do desafio do Kaggle.


#### Churn rate Prediction


## Bibliotecas

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline


from sklearn.preprocessing import LabelEncoder, OneHotEncoder
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

#from sklearn.linear_model import RidgeClassifier
from sklearn.metrics import accuracy_score

from sklearn.ensemble import RandomForestClassifier

from sklearn.model_selection import GridSearchCV

```

## Passos:

- Carregando os dados
- Análise exploratória dos dados
  - Verificando balanceamento
  - Verificando valores únicos
  - Separando colunas categóricas
  - Visualizando os dados
  
#### Após verificar as variáveis optei por utilizar as seguintes variáveis:

- Customer ID
- Gender
- PhoneService
- Contract
- TotalCharges

- Processamento das informações
  - Colunas com até 5 valores únicos serão consideradas categóricas
  - Dando um Upsampling para as classes desbalanceadas de resultado.
- Criação dos dados de parâmetros para o modelo
- Criação do GridSearch
- Treino do modelo

#### Melhor Score: 0.9081948151105694
#### Melhores parâmetros encontrados:
```
{'bootstrap': False,
 'criterion': 'gini',
 'max_depth': None,
 'max_features': 10,
 'min_samples_leaf': 1,
 'n_estimators': 250}
```

## Fonte de Dados

Dataset: Telco-Customer-Churn.csv
Disponível em: https://www.kaggle.com/blastchar/telco-customer-churn

