# **Evaluación *in silico* de Favipiravir para su reposicionamiento contra COVID-19**

Espinosa-Hernández S. Hurtado-Solórzano J.A. Ruiz-Sánchez E.

**Benemérita Universidad Autónoma de Puebla. Pue,Pue,México; Universidad Michoacana de San Nicolás de Hidalgo. Morelia, Mich, México; Centro de Investigación y de Estudios Avanzados del IPN. Zapopán, Jal, México.**

## **1. Introducción**

La emergencia sanitaria causada por la COVID-19 (Coronavirus disease-2019) ha cobrado hasta principios de agosto 256,246 vidas (CONACYT, 2020) debido a la falta de un tratamiento, encendiendo las alarmas sanitarias a nivel mundial desde el inicio de la pandemia; aún con la aplicación de vacunas aprobadas por emergencia sanitaria, tan sólo el 24.2% de la población mundial ha sido inmunizada (Mathieu, E. et al. 2021), sin mencionar que sólo funcionan como medio preventivo de un cuadro grave de la enfermedad y no como tratamiento contra ella. Es por esto que se ha convertido en una necesidad el desarrollo de un fármaco antiviral contra SARS-CoV-2 (Severe Acute Respiratory Syndrome Coronavirus 2), sin embargo, el desarrollo de un fármaco de in novo es un procedimiento muy largo y costoso. Considerando lo anterior se han desarrollado diversos estudios de reposicionamiento de fármacos, basados en el uso de un fármaco existente con un nuevo fin terapéutico contra la  COVID-19.

https://user-images.githubusercontent.com/78750648/130305523-ca975e6a-a075-4694-b2e2-e32cacb0bcfe.mov

![Figura 1  Estructura de Favipiravir-RTP en su forma activa](https://user-images.githubusercontent.com/78750648/130305434-651375f0-fd4f-4aa3-8b71-2434fd5ec6a6.png)

*Figura 1. Estructura de Favipiravir-RTP en su forma activa*

Favipiravir es un profármaco inicialmente utilizado en casos de influenza resistentes al tratamiento convencional. Este es convertido a su forma activa Favipiravir-RTP tal como se vio anteriormente en la Figura 1, tras una ribosilación y fosforilación intracelular, que inhibe la ARN polimerasa dependiente de ARN (RdRp), tal como se muestra en la Figura 2 mediante competencia con los nucleótidos de purina, previniendo la replicación del genoma viral, así como la formación de nuevos viriones, (Esquema 1). El dominio catalítico de la RdRp se encuentra bien conservado entre los virus de ARN, por lo tanto es posible que este antiviral tenga efecto sobre el sitio catalítico de la RdRp del SARS-CoV-2.

![Figura 2  Estructura de la ARN polimerasa dependiente de ARN (RdRp)](https://user-images.githubusercontent.com/78750648/130305576-ca10e71c-c530-47c2-b5b1-a3be3ef9c9b3.png)

*Figura 2. Estructura de la ARN polimerasa dependiente de ARN (RdRp)*

![Esquema 1  Proceso de inhibición de RdRp por Favipiravir-RTP](https://user-images.githubusercontent.com/78750648/130305619-9e6138c9-8e57-4dcf-999f-1e1cb07d9259.png)

*Esquema 1. Proceso de inhibición de RdRp por Favipiravir-RTP*

El análisis de acoplamiento molecular (molecular docking) permite buscar la mejor conformación y posición de un ligando dentro de un receptor, por ejemplo, una enzima (Saldívar et al. 2016), mediante el estudio de las fuerzas de unión entre ambas estructuras; el acoplamiento molecular se ha convertido en una herramienta esencial para el descubrimiento y reposicionamiento de fármacos (Ferreira et al., 2015). La unión entre un fármaco (F) y su receptor (R) está descrita por la constante de asociación (ecuación 1), siendo ésta una reacción de asociación simple, mientras más alta sea la constante, mayor es la energía liberada en la interacción del receptor y el fármaco, dependiendo de la afinidad de unión del complejo ligando-receptor (Ferreira et al. 2015).

![Ec1](https://user-images.githubusercontent.com/78750648/130305689-88b3e5d2-05cf-4e11-a71e-91fef89c6f49.JPG)

Para poder realizar el acoplamiento molecular es necesario contar con la estructura tridimensional del ligando y del receptor, dichas estructuras pueden ser obtenidas a partir del Protein Data Bank (PDB). En este trabajo se realiza el acoplamiento de Favipiravir, posible fármaco para tratar la enfermedad ocasionada por SARS-CoV-2, a partir de la interacción del sitio activo (residuos D760 y D761) (Poner el VÍDEO residuos)  (Hillen, H. et al. 2020) de la RdRp y el Favipiravir-RTP. 

## **2. Metodología**

### *2.1  Análisis de acoplamiento molecular in silico*

Se realizó el acoplamiento molecular a partir de la estructura cristalina de RdRp obtenida a partir del Protein Data Bank (PDB) con el código 7BW4 y el fármaco Favipiravir-RTP obtenido de PubChem con el CID 5271809. Posteriormente se editaron las moléculas con el programa PyMOL eliminando las estructuras que no se requieren.

Una vez realizada la edición de la proteína y el fármaco a evaluar se procedió a añadir la carga e hidrógenos polares a la RdRp en el programa AutoDock Tools y se convirtió en formato .pdbqt; el Favipiravir-RTP se convirtió al mismo formato. Por último, se introdujeron los comandos correspondientes en símbolo del sistema (cdm) y con ayuda del programa Vina (O. Trott, 2010) se desarrolló el acoplamiento. 

### *2.2 Análisis de la dinámica molecular*

Por medio de la plataforma SwissParam, se obtuvieron los archivos necesarios para realizar la dinámica molecular, para su posterior ejecución empleando Gromacs 2021 GPU mediante la plataforma Google Colab donde se efectuaron los pasos necesarios para el acondicionamiento y subsiguiente análisis de dinámica molecular.

## **3. Resultados y discusión**

### *3.1  Acoplamiento molecular  RdRp-Favipiravir*

Los valores de afinidad en el acoplamiento molecular RdRp-Favipiravir van desde -6.4 a -6.9 kcal/mol. Sin embargo para el análisis de dinámica molecular fue vital observar si los modelos interaccionaban con los residuos D760 y D761 pertenecientes al sitio activo de RdRp, destacando que el modelo nueve con una menor afinidad (Tabla 1) tiene una directa unión con el sitio activo de RdRp (Figura 3).

![Figura 3](https://user-images.githubusercontent.com/78750648/130305972-c45b5320-7f77-45f6-bb52-b5ee9f5fdeb6.png)

*Figura 3. Primer modelo de interacción entre Favipiravir y el sitio activo (residuos D760 y D761) de RpRd con afinidad de -6.9 kcal/mol*

https://user-images.githubusercontent.com/78750648/130306027-c628bf84-5d74-4d88-b787-35cc16e9eb55.mov

Por otra parte, si bien el primer modelo (Figura 4) no tiene una directa interacción con los residuos de interés cuenta con los mejores valores de afinidad  y es posible que dentro del organismo logre bloquear a la RdRp.

![Imagen5](https://user-images.githubusercontent.com/78750648/130305999-0622a3d7-3506-4081-9585-4705bb5b8989.png)

*Figura 4. Noveno modelo de interacción entre Favipiravir y el sitio activo (residuos D760 y D761) de RpRd con afinidad de -6.4 kcal/mol*

https://user-images.githubusercontent.com/78750648/130306066-618b5f54-98a6-474f-b5ef-38f0149df7ab.mov

| Modelo  | Afinidad (kcal/mol) |
| ------------- | ------------- |
| 1 | -6.9 |
| 2 | -6.9 |
| 3 | -6.8 |
| 4 | -6.7 |
| 5 | -6.7 |
| 6 | -6.7 |
| 7 | -6.5 |
| 8 | -6.5 |
| 9 | -6.4 |


Tabla 1. Afinidad del acoplamiento molecular de RdRp-Favipiravir

### *3.2  Dinámica molecular  RdRp-Favipiravir*

#### *3.2.1  Presión*

#### *3.2.2  Densidad*

#### *3.2.3 Raíz de la desviación cuadrática media (RDCM)*

#### *3.2.4  Potencial de energía Lennard-Jones*

#### *3.2.5  Potencial de energía Coulombic (Coul-SR)*
