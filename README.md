# LAB05 - Analisis de paquetes de red - IDS

### Sergio Marchena 16387
 
 
## Modelo con PCA
```
N of components:  35
Accuracy:  0.44112198994442975
Matriz de confusion: 
 [[1025 2997]
 [1227 2309]]
              precision    recall  f1-score   support

      normal       0.46      0.25      0.33      4022
     anomaly       0.44      0.65      0.52      3536

    accuracy                           0.44      7558
   macro avg       0.45      0.45      0.42      7558
weighted avg       0.45      0.44      0.42      7558
```

## Modelo sin PCA
```
N of components:  41
Accuracy:  0.950648319661286
Matriz de confusion: 
 [[3844  178]
 [ 195 3341]]
              precision    recall  f1-score   support

      normal       0.95      0.96      0.95      4022
     anomaly       0.95      0.94      0.95      3536

    accuracy                           0.95      7558
   macro avg       0.95      0.95      0.95      7558
weighted avg       0.95      0.95      0.95      7558

```

## Conlusion: 

Como se puede observar el modelo con menor numero de feautures (el PCA) tiene una precision muy baja comparada con el modelo sin ninguna reduccion de dimensionalidad. El modelo con PCA tiene una precision de 44% y el modelo sin PCA tiene 95%. 
* Los valores de precision del modelo con PCA estan por 45% mientras que el modelo sin PCA tiene valores de precision de 95%. 
* Los valores de recall del modelo con PCA para clasificar trafico normal es de 25% y para anomalias el 65%, por lo que es un poco mejor. El modelo sin PCA tiene 95% en promedio para ambos casos.
* El modelo con PCA tiene un valor de f1 para trafico normal de 33% y un 52% de deteccion de anomalias, por lo que aproximadamente clasifica 1/2 anomalias de forma correcta. Mientras que el modelo sin PCA tiene 95% de f1-score. 

En conclusion, para este modelo de regresion logistica, el PCA no ayudó si no perjudicó al modelo y no se recomienda. 
