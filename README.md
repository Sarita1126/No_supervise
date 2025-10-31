## *Análisis No Supervisado*
***Autora:*** *Sara Peña Alvarez*

#### *Objetivo*
*Este proyecto explora un conjunto de datos con información **fisicoquímica de vinos tintos**.  
El objetivo fue analizar sus características, reducir la dimensionalidad de los datos y descubrir posibles patrones que expliquen las diferencias de calidad sin usar etiquetas.*

#### *Datos*
*Primero se revisó el comportamiento de las **11 variables numéricas** del vino (acidez, azúcar, alcohol, dióxido de azufre, pH, etc.).  
Los valores fueron coherentes y sin errores graves, lo que permitió aplicar técnicas de aprendizaje no supervisado con confianza.*
*Luego se analizó cómo cada característica se relaciona con la **calidad del vino (quality)**:*
- *Los vinos con **más alcohol y más sulfatos** tienden a tener mejor calificación.* 
- *Los de **alta acidez volátil** suelen ser de menor calidad.*  
- *El ácido cítrico también aporta positivamente a la frescura y estabilidad.*
*Estas relaciones se confirmaron con gráficos de caja y la **matriz de correlación**, donde el alcohol fue la variable más asociada con la calidad.*

#### *Metodología*

1. ***PCA (Análisis de Componentes Principales):***  
   *Se usó para reducir las 11 variables a solo 2 componentes, que explican cerca del **70 % de la varianza total**.  
   Estas dos dimensiones capturan las diferencias químicas más importantes del vino.*

2. ***K-means:*** 
   *Se aplicó para agrupar los vinos según sus características químicas.*
   *El mejor resultado se obtuvo con **K=2**, que separa vinos de **calidad media-baja** y **media-alta**.*  
   *El **Silhouette Score** mejoró de 0.20 a 0.40 después de usar PCA, mostrando que la reducción de dimensionalidad ayudó mucho.*

#### *Resultados*

- *La mayoría de los vinos tienen calificaciones **entre 5 y 6**, es decir, calidad media.*
- *Los vinos con **más alcohol y menos acidez volátil** suelen ser mejor valorados.* 
- *El PCA permitió ver patrones claros al graficar los datos, incluso sin usar la etiqueta de calidad.* 
- *El modelo **K-means** identificó grupos que se relacionan con diferentes estilos o niveles de calidad del vino.*
