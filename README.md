# Análisis del Mercado Inmobiliario
### Prediccion del precio de propiedades en Buenos Aires, Argentina con datos de publicaciones en la página web Properati

Con los datos que se encuentran en este repositorio, provistos por el portal web Properati, realicé el siguiente análisis del mercado inmobiliario en Buenos Aires, Argentina:

La mayoria de las publicaciones en la pagina son de propiedades tipos vivienda (Casas, Apartamento y PHs)



La gran mayoria de publicaciones se hacen de propiedades en Buenos Aires, y de esa ciudad en el barrio Palermo. 


Parece no haber una relación marcada entre cuanto se demora la propiedad en ser vendida y caracteristicas medibles como su tamaño, y numero de espacios y baños, podría ser simplemente cuestión de que tan bueno sea tu agente inmobiliario. Pero se podría afirmar que el barrio donde está ubicada la propiedad si afecta si se vende más o menos rapido que el promedio.
Los barrios con comportamientos marcados fueron

|Más rápido que el promedio |Más lento que el promedio  |
--- | --- |
|Villa Santa Rita -- Nuñez -- Belgrano -- San Nicolás -- Villa Pueyrredón -- Velez Sarsfield -- Monte Castro -- Monserrat -- San Cristobal -- Centro / Microcentro -- Villa Ortuzar -- Caballito -- Colegiales -- Paternal -- Tribunales -- Palermo -- Villa Crespo| Villa Lugano -- Pompeya -- Villa Soldati -- Mataderos -- Saavedra -- Villa Luro -- Liniers -- Parque Avellaneda -- Floresta -- Flores -- Parque Chacabuco -- Parque Patricios -- Agronomía -- Puerto Madero|

Utilizamos 80276 datos para nuestro entreno y usando las superficies totales y cuviertas, y el número de baños de las propiedades (['surface_total', 'surface_covered', 'bathrooms']) elegidas por su correlación con la variable objetivo ('price'), y el Mean Absolute Error como métrica de error.

Se entrenaron:
- Regresión Lineal, valores defaut
- K vecinos mas cercanos, valores Default y n_neighbors = 3, weights = distance
- Árbol de Decisión, valores default y max_depth = 30

|	|LR MAE ($ USD)|KNN Default MAE ($ USD)|KNN Optimized MAE ($ USD)|DT Default MAE ($ USD)|DT Optimized MAE ($ USD) |
---	| --- | --- | --- | --- | --- |
|Train|	90192.906013|	56969.194499|	39594.234751|	35517.577257|	35517.577257
|Test|	92186.860182|	66440.388948|	59580.735831|	55876.901390|	**55876.901390**

Estos resultados mejoran notablemente cuando el mejor modelo se utiliza para predecir los precios de las propiedades de cada barrio:
