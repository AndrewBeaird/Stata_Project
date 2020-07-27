# Stata_Project
Stata project during graduate school.

# Estadística Descriptiva (35 %)

Utilizando el subconjunto de la base de datos CASEN 2017 que se le ha entregado [sub set casen2017 v11.dta] calcule los ítem (α), (β) y (γ). 

A pesar de que debió haber quedado claro durante las sesiones del
taller, no está de más recalcar que todas las tablas solicitadas en esta sección deben ser realizadas
mediante el uso de loops (forvalues, foreach, while, etc) y matrices, para luego ser exportadas en
formato LATEXy ser impresas en formato pdf. De no realizar los procedimientos recién descritos, por
ejemplo, generando la tabla en Excel o copiando y pegando desde el output de STATA, esta parte
no tendrá puntaje.

# (α) Caracterice la distribución de ingresos (yoprcor) por años de escolaridad (esc) separando
Caracterice la distribución de ingresos (yoprcor) por años de escolaridad (esc) separando por hombres y mujeres construyendo el Cuadro (1). 
En la construcción de su Cuadro debe
tener presente lo siguiente:

• Columna 1 representa cantidad de personas con i años de escolaridad.

• Columna 2 representa la media del ingreso con i años de escolaridad.

• Columna 3 es la cantidad de hombres con i años de escolaridad.

• Columna 4 representa la media del ingreso de los hombres con i años de escolaridad.

• Columna 5 es la cantidad de mujeres con i años de escolaridad

• Columna 6 representa la media del ingreso de las mujeres con i años de escolaridad.

• Columna 7 representa la media del ingreso de los hombres.

• Columna 8 representa la media del ingreso de las mujeres.

• Columna 9 corresponde al estadístico t resultante del test de medias realizado sobre el ingreso
separando por hombres y mujeres.

# (β) Caracterice la Inclusión Financiera nacional (y27a-y27g) construyendo el Cuadro (2).
Para esto usted debe notar que:

• Column 1 corresponde a la frecuencia absoluta del grupo i.F

• Column 2 corresponde a la frecuencia absoluta de hombres del grupo.

• Column 3 corresponde a la frecuencia absoluta de mujeres del grupo.

De esta forma, la primera columna Total corresponde a una frecuancia absoluta, mientras
que las dos siguientes (Prop. Hombres y Prop. Mujeres ) corresponden a una proporción.
Para la primera columna no utilice decimales, y para las segunda y tercera entregue las
participaciones de cada género con 3 decimales.

# (γ) Caracterice la Cotización Previsional (o29) de la población chilena construyendo el Cuadro
(3). Para esto usted deberá notar que este Cuadro no cuenta con una fila final llamada
Total como aparecía en las anteriores. Esto se debe a que este Cuadro representa solamente
participaciones porcentuales, por ende, la suma vertical de cada columna debe ser igual a uno
(100 %). o en términos formales. Entregue sus valores usando 3 decimales.

# Generación de Variables (35 %)

Siguiendo con la base utilizada en la sección anterior realice lo siguiente:
(a) Genere una variable llamada n comuna que contenga la cantidad de personas que fueron
encuestadas en cada comuna.
(b) Genere una variable llamada decil de ingreso que contenga los deciles de ingreso para la
variable yoprcor. Además de esto, esta variable deberá contener etiquetas sobre los valores
de modo que cuando, por ejemplo, ejecutemos un “tabulate” sobre esta, aparezca en el primer
decil (asociado al valor 1) el texto “Primer Decil de Ingreso”, para el segundo “Segundo
Decil de Ingreso” y así sucesivamente. Recuerde que los deciles deben contener el 10 % de la
población en cada uno de sus tramos, sea cuidadoso a la hora de revisar si la forma en la que
realizó sus deciles cumple con esta condición.
(c) Genere una variable que Dummy que tome el valor de 1 si el encuestado reside en la Región
Metropolitana y 0 en caso contrario. Además de esto etiquete dicha variable el string “Encuestado en Región Metropolitana”. Adicionalmente, etiquete los valores iguales a 1 con
el string “Región Metropolitana”, y los ceros con “Región Diferente a la Metropolitana”
(d) Genere una variable que contenga la cantidad mujeres que ganan más de un millón de pesos
(“yoprcor”) por región.

Nivel Experto (20 %)
A usted se le ha entregado la base da datos base productos la cual contiene 6 variables que
caracterizan el desempe˜no económico de una serie de firmas entre el a˜no 2000 y 2006 para diferentes
productos que estas comercializaron en dicho periodo. Las variables contenidas en la base se detallan
a continuación:
firma : Corresponde al identificador de la Firma (i)
year: Variable Indicador que identifica el periodo t de la firma (i).
id prod: Variable que identifica el producto (j) vendido en el periodo (t) por la firma (i).
meta ventas: Corresponde a la meta de ventas que se propuso lograr la firma (i) durante el
periodo (t) para el producto (j).
ventas: Corresponde a las ventas reales que realizó la empresa (i) durante el periodo (t) para
el producto (j).
costos Corresponde a los costos en los que incurrió la firma (i) durante el periodo (t) para
el producto (j)
A continuación usted deberá resolver las siguientes preguntas:
1. Genere una variable llamada prod loss que identifique los productos que no lograron cubrir
sus costos independiente de la firma que lo produjo y el tiempo en el que fue vendido. Esta
variable debe tomar el valor de 1 si el costo no fue cubierto, un 0 para aquellas firmas que si
lograron cubrirlos.
2. Genere una variable llamada y prod loss y que tome el valor de 1 para todo el periodo t
de operación si es que, al menos uno, de los productos no logró cubrir sus costos
3. Genere una variable que muestre si es que el producto j está cumpliendo su meta de ventas
independiente de la firma que lo produjo y el tiempo en el que fue vendido. Llame a esta
variable cumple meta
4. Genere una variable que tenga por nombre cumple meta todos que tome el valor de 1
para todo el periodo t si es que la firma logró cumplir sus metas de ventas en TODOS
sus productos j y un 0 si es que fracasó en cumplir sus metas de ventas en al menos un
producto.
5. Genere una variable que muestre el promedio de ventas por firma (i) y a˜no (t) y llámela
ventas mean.
6. Genere una variable llamada costos mean que muestre el promedio de los costos por firma
(i) y a˜no (t).
7. Adicionalmente deberá crear una variable llamada prod mas vendido que contenga el producto que tuvo la mayor cantidad de ventas por periodo y firma.

Al finalizar esta parte usted debería terminar con una base de datos que, para la primera
firma, debería lucir como lo que se muestra en la Tabla (8). Acá debe tener cuidado, muchas
de las variables anteriores requieren de una serie de variables auxiliares que se combinan con
el uso de bys, egen y gen para ser construidas, por lo que no intente generar cada una
de las variables anteriores con “una sola linea de código”, hay un par que son un poco más
complejas que eso y requieren dos o tres.


# Presentación de Estimaciones (30 %)
(a) Basado en el trabajo de Rajan & Zingales 1995, sobre estructura de capital de las firmas. Se
pide que replique la Tabla (4), haciendo uso del comando outreg2. (Loops serán bonificados, mas
no penalizados). Las variables que necesitará ocupar son : leverage tang market book ln sales y
prof las cuales se encuentran disponibles en la BASE base present resultados.dta

(b) Ahora agregue como control la variable Edad de la firma (age), pero no reporte el coeficiente,
sino que despliegue una nota explicativa sobre que se está controlando por dicha variable en las
estimaciones del Cuadro (5)

(c) Ahora sobre la Cuadro (5), agrupe las variables Tangibility (tang) y Market to book Ratio
(market book) en un grupo de variables llamado “Assets” y las variables Logaritmo de las
Ventas (ln sales) y Profit (porf ) en otro llamado “Performance”. Es decir replique la Cuadro
(6)







