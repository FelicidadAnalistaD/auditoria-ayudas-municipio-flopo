# auditoria-ayudas-municipio-flopo
#  Informe de Análisis: Optimización de Ayudas Alimentarias Municipio Flopo

##  Perfil de la Analista
* **Autora:** Felicidad Monserrat Coloma
* **Rol:** Analista de Datos Junior
* **Formación:** Certificado Profesional de Análisis de Datos de Google ("Actualmente cursándolo" - Beca FUNDAE), Prácticas autodidactas de SQL en SQLBolt

---

##  1. Declaración de Trabajo (SOW) y Diagnóstico
Este proyecto surge como una auditoría social, basada en los registros abiertos del Municipio Flopo sobre la concesión de ayudas alimentarias básicas de Emergencia a ciudadanos en situación de Extrema vulnerabilidad (personas con 0 ingresos). A través de esta investigación busco identificar de forma matemática dónde se producen las demoras en la atención al ciudadano y proponer un rediseño del flujo de trabajo que agilice la entrega de recursos a las familias y personas vulnerables.

Para este análisis, se ha utilizado una base de datos pública de simulación que contiene 49 casos reales de solicitudes gestionadas por los servicios sociales del municipio.

###  Diagnóstico de la situación actual:
* **Retraso Crítico:** Una media global de 43,75 días de espera para recibir una ayuda básica de alimentos, sin respuesta en forma económica ni alimenticia en el "Aquí y Ahora".
* **Cuellos de Botella:** La Zona Norte se identificó como la más colapsada, exigiendo una media de 5,7 documentos en comparación con las Zonas Centro y Sur.
* **ALERTAS ROJAS / Expedientes paralizados:** Detecté múltiples expedientes en el "Limbo" por más de 150 días, así como celdas con errores de registro manual en el origen.

---

##  2. Objetivo SMART del Proyecto
Optimizar el proceso de concesión de ayudas de Emergencia alimentaria en el Municipio Flopo, para reducir el tiempo de espera de los más de 60 días actuales a menos de 15 días, y disminuir la carga burocrática de una media de 5,3 documentos a un máximo de 2 documentos indispensables.

Esta reducción drástica de la documentación se basa en dos razones de eficiencia operativa:
1. **Eliminación de duplicados oficiales:** Los Ayuntamientos y órganos oficiales ya tienen en sus sistemas de datos la mayoría de los documentos que solicitan al ciudadano (como el padrón, la identidad u otros registros). Exigirlos nuevamente supone un retraso artificial innecesario, haciendo esperar al ciudadano al pedir algo que la propia Administración debe consultar internamente.
2. **Centrarse en lo indispensable:** El máximo de 2 documentos obligatorios se reservará estrictamente para aquella información excepcional y actualizada de la situación del solicitante que los organismos no posean de forma previa en su histórico.

Con esta simplificación, se logrará una respuesta del "Aquí y Ahora" para las familias y personas vulnerables.

---

##  3. Detalles del Análisis y Privacidad
* **Datos y Privacidad:** Para respetar al máximo la privacidad de las personas y proteger la información sensible de las ayudas sociales, he elegido trabajar de forma totalmente local en mi ordenador. No he subido estos datos a ninguna plataforma de internet ni a la nube, realizando todo el proceso de forma segura en mi disco duro.
* **Limpieza de Datos en Google Sheets:** Para poder calcular las medias de los días de espera de forma correcta sin que se estropeen los números, realicé una limpieza previa dentro de la hoja de cálculo de Google Sheets. Busqué las celdas donde ponía PENDIENTE o ERROR en la columna de días de espera y las cambié por valores vacíos. De esta forma, al llevar los datos a Power BI, el programa pudo calcular la media matemática exacta del municipio sin fallos.
* **Gráficos e Informe en Power BI Desktop:** Diseñé una pantalla sencilla y clara para que se entienda la situación de un vistazo:
  * *Tarjetas de Alerta:* Coloqué dos tarjetas grandes en el lateral izquierdo resaltadas en un color rojo chillón para llamar la atención. Una marca el promedio global de 43,75 días y la otra la mediana de 44,88 días de espera.
  * *Botones de filtro:* Coloqué tres botones arriba para las zonas Norte, Centro y Sur. Cuando pinchas en un botón, todo el informe se mueve y se actualiza solo para mostrar los datos de esa zona.
  * *Gráfico de dispersión:* Añadí un gráfico de puntos flotantes que cruza los ingresos de las personas con sus días de espera. Así se ve de forma muy clara cómo las familias que tienen cero ingresos sufren los retrasos más altos.

---

##  4. Conclusión y Solución del Problema
El análisis demuestra que el colapso no se debe a la falta de personal, sino a un laberinto de trámites innecesarios. Al cruzar los ingresos con los días de espera, salta a la vista que las familias con 0 ingresos, que son las que sufren la mayor vulnerabilidad, son las que más tiempo pasan atrapadas en el limbo de la administración.

Para solucionar este problema de raíz de manera constructiva, llegué a la conclusión de que se debe ejecutar este cambio en el Municipio Flopo en un plazo de 3 meses mediante tres acciones:
1. **Unificar y recortar requisitos (1º Mes):** La oficina Norte eliminará los trámites repetitivos y bajará sus exigencias de 5,7 documentos a los 2 únicos indispensables, igualando el sistema en todo el municipio.
2. **Activar la consulta interna (2º Mes):** Configurar los sistemas informáticos del Ayuntamiento y organismos oficiales del Municipio Flopo para que los funcionarios consulten los documentos en sus propias pantallas.
3. **Vía de urgencia automática (3º Mes):** Crear una regla automática en el sistema para que las solicitudes de personas con cero ingresos pasen al primer lugar de la cola, garantizando por ley que reciban la ayuda alimentaria en un plazo máximo de 15 días.

Con estas medidas organizativas aplicadas en este plazo de 3 meses, el Municipio Flopo eliminará el atasco actual y ofrecerá una atención digna, transparente y verdaderamente humana.

---

##  5. Evidencias del Cuadro de Mando

---

##  Archivos en esta Carpeta del Proyecto
* `Base_Datos_Limpia.csv`: El archivo de hoja de cálculo con los datos que utilicé para el análisis.
* `Cuadro_Mando_Flopo.pbix`: El archivo original de Power BI Desktop con los gráficos y botones interactivos.
