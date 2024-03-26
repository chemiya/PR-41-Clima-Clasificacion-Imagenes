<h1>Documento resumen del proyecto para determi9nar el tiempo que hace en imagenes</h1>

<ol>
<h2><li>Resumen del proyecto</li></h2>
<p>Este proyecto consistirá en la creación de varias redes neuronales con diferentes tecnologias para clasificar diferentes imagenes en funcion del tiempo que se puede apreciar en ellas. Una red neuronal convolucional es un tipo de red neuronal artificial especialmente diseñada para procesar datos que tienen una estructura de cuadrícula, como imágenes o datos de series temporales. En este proyecto se van a crear varias y se van a tratar de optimizar sus parametros. </p>








<h2><li>Tecnologías utilizadas</li></h2>
<p>Se van a utilizar las siguientes tecnologías relacionadas con Python:</p>
<ul>
<li>Tensorflow</li>
<li>Keras</li>
<li>PyTorch</li>
<li>FastAI</li>
</ul>

<h2><li>Descripcion del conjunto de datos</li></h2>
El conjunto de datos se ha obtenido de https://www.kaggle.com/datasets/jehanbhathena/weather-dataset/data donde se pueden encontrar varias imagenes separadas en diferentes carpetas agrupandolas por el tipo de tiempo que se puede apreciar en ellas. Estas imagenes se pueden clasificar en rocio, niebla toxica, cencellada, hielo, granizo, relampagos, lluvia, arcoiris, escarcha, tormenta de arena y nieve






<h3>Separación conjunto de datos y de test</h3>
El conjunto de datos original con todas las imagenes es muy grande, con alrededor de 6900 imagenes dividias en las 11 clases comentadas previamente. Para este proyecto, se han seleccionado para cada clase 23 imagenes en cada clase para el conjunto de entrenamiento, y 12 imagenes de cada clase para el conjunto de validacion y 12 imagenes de cada clase para el de test.


<h2><li>Optimización de los parámetros</li></h2>
Para la optimizacion de parametros a continuacion se definen los parametros optimizados en cada caso. El proceso de optimizacion de parametros se realiza mediante varios bucles anidados que recorren cada combinacion diferente de parametros y crea el modelo aplicandolos. Una vez hecho esto, obtiene la precision del modelo sobre el conjunto de test y se guarda en un dataframe la combinacion de parametros establecida y la precision obtenida. Como son muchas para cada modelo el numero de combinaciones posibles de parametros, se ha optado por ir pivotando con el parametro del numero de epocas, de manera que se evaluen todas las combinaciones de parametros con el mismo numero de epocas y se genere el dataframe con los resultados. Despues se evaluan las combinaciones de parametros con otro numero de epocasy se genera el dataframe correspondiente. De esta manera estos dataframe se pueden ir almacenando en un excel y la ejecuccion del programa no es excesivamente larga.

<h3>Optimización parámetros </h3>
A continuación, se detallan los parámetros a optimizar en la red neuronal creada con FastAI:
<ul>
<li>Metrica: accuracy, error_rate, Precision(average='macro'), Recall(average='macro')</li>
<li>Épocas: 4, 6, 8</li>
<li>Batch_size: 4, 8, 12</li>
</ul>

La tabla con todos los valores sobre la precision para las diferentes combinaciones de parámetros en este modelo se puede encontrar en el Excel adjunto “erroresFastAI.xlsx”. Por lo tanto, los mejores valores en los parámetros para este modelo son los siguientes:
<ul>
<li>Metrica: accuracy</li>
<li>Épocas: 8</li>
<li>Batch_size: 8</li>
</ul>



A continuación, se detallan los parámetros a optimizar en la red neuronal creada con Pytorch:
<ul>
<li>Optimizador: SGD, Adam, Adagrad</li>
<li>Épocas: 4, 6, 8</li>
<li>Batch_size: 4, 8, 12</li>
<li>Capas: 3, 4, 5</li>
</ul>

La tabla con todos los valores sobre la precision para las diferentes combinaciones de parámetros en este modelo se puede encontrar en el Excel adjunto “erroresPytorch.xlsx”. Por lo tanto, los mejores valores en los parámetros para este modelo son los siguientes:
<ul>
<li>Optimizador: Adagrad</li>
<li>Épocas: 6</li>
<li>Batch_size: 4</li>
<li>Capas: 3</li>
</ul>


A continuación, se detallan los parámetros a optimizar en la red neuronal creada con Tensorflow y keras:
<ul>
<li>Optimizador: SGD, Adam, Adagrad</li>
<li>Épocas: 4, 6, 8</li>
<li>Batch_size: 4, 8, 12</li>
<li>Capas: 2, 3, 4</li>
</ul>

La tabla con todos los valores sobre la precision para las diferentes combinaciones de parámetros en este modelo se puede encontrar en el Excel adjunto “erroresTensorKeras.xlsx”. Por lo tanto, los mejores valores en los parámetros para este modelo son los siguientes:
<ul>
<li>Optimizador: Adam</li>
<li>Épocas: 8</li>
<li>Batch_size: 12</li>
<li>Capas: 2</li>
</ul>



Finalmente, se ha podido apreciar que el mejor resultado se ha obtenido con la red neuronal creada con FastAI con una precision de 0.788.


<h2><li>Resultado final: vídeo youtube y repositorio</li></h2>
Repositorio Github:


<h2><li>Conclusiones</li></h2>
He podido aprender a configurar los diferentes parametros de una red neuronal y como crearlas para un problema de clasificacion de imagenes con diferentes tecnologias.

</ol>
