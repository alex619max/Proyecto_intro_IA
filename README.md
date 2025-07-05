# Proyecto_intro_IA

### Problema
La neumonía es un corresponde una forma de infección respiratoria causada por una bacteria o un virus. Esta afección puede ser leve o potencialmente mortal, sin importar la edad del individuo, aunque es la principal causa infecciosa de muerte infantil en el mundo. Además de los niños, población con riesgo se considera a los adultos mayores y personas con problema de salud previos.
Tener la información de neumonía en lo antes posible puede ser la diferencia entre la vida y la muerte al recibir el tratamiento adecuado.


### Plan de acción
Los pulmones están formados por pequeños sacos llamados alvéolos, que se llenan de aire cuando una persona sana respira. Cuando una persona tiene neumonía, los alvéolos se llenan de pus y líquido, lo que dificulta la respiración y limita la absorción de oxígeno. A través de Rayos X se puede observar el estado de los pulmones permite determinar si la persona presenta la enfermedad. 
El dataset a trabajar corresponde a varias imágenes de radiografías del torso, en donde están presente 2 etiquetas, imágenes de rayos x de individuos sin neumonía y radiografías de pulmones con neumonía según si la causa es por una bacteria y un virus.  
El dataset está disponible en kaggle: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia/data 
Para esta tarea de poder identificar la enfermedad a través de imágenes haremos uso de redes neuronales convolucionales. Haremos uso de modelos destacados, ResNet, VGG-16, y GoogleNet disponibles en Pytorch, con el objetivo de comparar rendimiento, además para el uso de la técnica de "Transfer Learning" para ahorrar en rendimiento y usar conocimientos previos disponibles de estas redes ya entrenadas.

### Justificación del modelo

Utilizar para esta tarea redes neuronales convolucionales es la mejor opción para el trabajo de evaluar imágenes, dada su escalabilidad, detección de patrones y el usar menos parámetros que trabajar con la imagen directamente teniendo cada píxel como una feature. Sin embargo, la reducción de parámetros conduce a la perdida de información, si las categorías poseen características muy sensibles que se puedan perder por disminuir la dimensionalidad en el input o dentro de la red, el rendimiento puede llegar a ser no aceptable. La elección de 3 redes distintas es porque cada red tiene distintas estructuras y formatos que permiten mejorar el rendimiento computacional o detectar más variedad de patrones.
