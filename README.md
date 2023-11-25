![](UPC_Logo.png)

Machine Learning: Trabajo Final



Alumnos:

Gonzalo Jurado (u202010216)

Carlos Castilla (u202116277)

Daniel Barrionuevo (u201922128)


## <a name="_2mixulug1yng"></a>**Milestone 4: TA3**
## <a name="_glgqrkg3bvbf"></a>**Introducción**
Con el paso del tiempo, cada objeto que es creado eventualmente pierde su forma debido a la deterioración. Según el artículo de la Biblioteca Nacional de España (2020), casos como el calor y la humedad son las causas más comunes por las que objetos pierden su estructura y se deterioran rápidamente si no es resuelto a tiempo.

Se entiende que si no se intenta hallar un modo de preservar la mayoría de los objetos posibles, estos serán perdidos permanentemente y requerirán reemplazos por cada plazo de algunos años. Es en base a este problema que se busca diseñar un medio que restaure la forma de la mayoría de objetos básicos posibles sin tener que reemplazarlos.

![](Fig_01.png)

Figura 1: Restauración de estado de objeto
##
## <a name="_qol15nkg5gpa"></a><a name="_l9bovzozfof8"></a>**Objetivos**
Este proyecto tiene como objetivos el entrenamiento de un modelo con objetos 3D, los cuales son modelos de distintos tipos de sillas, para que comprenda sus estructuras y sepa cómo diseñarlas, al igual que permitir que este reciba algún objeto 3D nuevo con alguna imperfección en su forma o color y este pueda restaurarlo en la menor cantidad de tiempo posible.

## <a name="_5uo8x6tjds1l"></a>**Marco Conceptual**
Entrenamiento de objetos 3D:

Se basa en la aplicación de técnicas de machine learning para entrenar el modelo en la identificación y comprensión de estructuras tridimensionales de distintos tipos de sillas.

Generación de diseños 3D:

Se centra en la capacidad del modelo entrenado para generar diseños de sillas basados en la comprensión adquirida durante el entrenamiento.

Detección y restauración de imperfecciones:

Consta de recibir objetos 3D con posibles imperfecciones en forma o color. Incorporando técnicas de detección de imperfecciones y algoritmos de restauración para corregir los errores en los objetos recibidos.
## <a name="_64kodnpg1dlu"></a>**Metodología**
**Transformaciones:**

Para realizar las transformaciones correspondientes se hicieron uso de las siguientes funciones:

- off\_to\_stl: Esta función convierte un archivo en formato OFF a STL. Lee el archivo OFF, extrae la información sobre vértices y caras, y crea un archivo STL correspondiente. Además, realiza validaciones de formato y manejo de errores.

- convertir\_carpeta: Toma la carpeta con archivos OFF, los convierte a archivos STL utilizando la función “off\_to\_stl”, y guarda los archivos STL resultantes en otra carpeta.

- xyz\_to\_tensor: Convierte un archivo en formato XYZ en tensor. Escala las coordenadas para que se ajusten a las dimensiones especificadas y retorna un tensor indicando si hay o no puntos en esas coordenadas.

- readOff: Lee un archivo en formato OFF y devuelve un conjunto de vértices y triángulos.

- save\_png: Lee un archivo en formato OFF y guarda la representación visual como un archivo png.

- process\_directory: Convierte los archivos OFF a STL gracias  off\_to\_stl. Además, crea imágenes PNG de los modelos 3D para uso visual y organiza los datos para entrenar y probar modelos de machine learning.

**Ejemplos:**

![](Ej_01.png)![](Ej_02.png)



![](Ej_03.png)


**Plan de impresion:**

Se utilizaron diversas bibliotecas para procesamiento de datos, manipulación de archivos 3d y generación de modelos que luego se utilizaron en la impresión 3d, tales como Numpy, Tensorflow y Keras para manipular y entrenar modelos gan. Además, se hace uso de stl para la manipulación y conversión de archivos 3d, y se utiliza la biblioteca Plotly para la visualización de modelos tridimensionales. En adición a esto, se implementa funciones para convertir archivos en formato off a stl, procesar directorios de modelos 3d y generar imágenes y tensores para su uso en el entrenamiento del gan.
## <a name="_c8w5os3em0q9"></a>**Milestone 5: TA4**
## <a name="_erct085y054v"></a>**Metodología**
**Modelo de arquitectura:**

![](Mod_01.jpeg)

![](Mod_02.jpeg)

**Configuración del entrenamiento:**

La configuración de entrenamiento utiliza un modelo gan, que consta de un generador y un discriminador. El discriminador se entrena para distinguir entre vóxeles reales y generados, mientras que el generador busca mejorar su capacidad para engañar al discriminador. Durante el entrenamiento, se ajustan los pesos del discriminador para maximizar su capacidad de distinguir entre real y falso, mientras que el generador ajusta sus pesos para minimizar esta capacidad discriminatoria. El acoplamiento entre el generador y el discriminador se logra mediante la compilación y entrenamiento del modelo gan. La configuración incluye el uso de capas convolucionales y de normalización, junto con diversas funciones y optimizadores para el entrenamiento El proceso iterativo de este enfoque permite que el generador mejore progresivamente su capacidad para producir voxels.




**Impresion 3D:**
## ![](Imp_01.jpeg)![](Imp_02.jpeg)


![](Imp_03.jpeg)![](Imp_04.jpeg)
##
##





## <a name="_yrqhl3tjyd8o"></a><a name="_5vx0mhjhgf0"></a><a name="_dxpmvbbthslt"></a><a name="_rnhscw4mw0fa"></a>**Final Milestone: TF**
## <a name="_8ecigfkiab5c"></a>**Resultados:**
5 epocas:					10 epocas:

![](Res_01.png)![](Res_02.png)
##
##



##
##

## <a name="_p0vvrs787u2h"></a><a name="_nq01e5cfg2f7"></a><a name="_fdfzdue37111"></a><a name="_6mkp3fp1jyif"></a><a name="_wcc7uvywpwph"></a>**						15 epocas:	![](Aspose.Words.00293efd-8236-4324-bf8c-914a5abe0d0d.014.png)

##
## <a name="_c8cqetugfcyp"></a><a name="_khdoozbcncdy"></a>**Conclusiones**
- El proceso de generación de cualquier figura u objeto en base a aprendizaje supervisado o no supervisado requiere alta precisión, datos de entrenamiento y tiempo para comenzar a entregar resultados aceptables.
- El loss de la red GAN disminuye lentamente en las primeras 5 épocas pero luego se dispara.
- Gracias al uso del GAN se logró generar modelos tridimensionales a partir de datos bidimensionales. Esta técnica fue de gran ayuda para mejorar la calidad y realismo de las representaciones 3D de las sillas en cuestión.
## <a name="_sl7w3z13wivm"></a>**Anexos**
- Figura 1: <https://www.restaurayrecupera.com/restauracion-sillas-alfonsinas/>

## <a name="_3w9na0j5coet"></a>**Bibliografía**
- Factores que afectan la preservación de los materiales tradicionales de bibliotecas y archivos (segunda parte). (2020). Biblioteca Nacional de España.[ ](https://www.bne.es/es/blog/blog-bne/factores-que-afectan-la-preservacion-de-los-materiales-tradicionales-de-bibliotecas-y-archivos-segunda-parte)<https://www.bne.es/es/blog/blog-bne/factores-que-afectan-la-preservacion-de-los-materiales-tradicionales-de-bibliotecas-y-archivos-segunda-parte>
