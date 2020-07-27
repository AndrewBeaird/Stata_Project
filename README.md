# Stata_Project
Stata project during graduate school.

# Evaluaci´on No Presencial
# Estad´ıstica Descriptiva (35 %)

Utilizando el subconjunto de la base de datos CASEN 2017 que se le ha entregado [sub set casen2017 v11.dta]
4
calcule los ´ıtem (α), (β) y (γ)
5
. A pesar de que debi´o haber quedado claro durante las sesiones del
taller, no est´a de m´as recalcar que todas las tablas solicitadas en esta secci´on deben ser realizadas
mediante el uso de loops (forvalues, foreach, while, etc) y matrices, para luego ser exportadas en
formato LATEXy ser impresas en formato pdf. De no realizar los procedimientos reci´en descritos, por
ejemplo, generando la tabla en Excel o copiando y pegando desde el output de STATA, esta parte
no tendr´a puntaje.

# (α) Caracterice la distribuci´on de ingresos (yoprcor) por a˜nos de escolaridad (esc) separando
por hombres y mujeres construyendo el Cuadro (1). En la construcci´on de su Cuadro debe
tener presente lo siguiente:
• ni representa cantidad de personas con i a˜nos de escolaridad, por ende P22
i=0 ni = N
• x¯i representa la media del ingreso con i a˜nos de escolaridad.
• nh,i es la cantidad de hombres con i a˜nos de escolaridad, por ende P22
i=0 nh,i = Nh
• h¯
i representa la media del ingreso de los hombres con i a˜nos de escolaridad.
• nm,i es la cantidad de mujeres con i a˜nos de escolaridad, por ende P22
i=0 nm,i = Nm
• m¯ i representa la media del ingreso de las mujeres con i a˜nos de escolaridad.
• H¯ representa la media del ingreso de los hombres.
• M¯ representa la media del ingreso de las mujeres.
• t-stat corresponde al estad´ıstico t resultante del test de medias realizado sobre el ingreso
separando por hombres y mujeres.

# (β) Caracterice la Inclusi´on Financiera nacional (y27a-y27g) construyendo el Cuadro (2).
Para esto usted debe notar que:
• fi corresponde a la frecuencia absoluta del grupo i, por ende P7
i=1 fi = F
• hi corresponde a la frecuencia absoluta de hombres del grupo, por ende P7
i=1 hi = H
• mi corresponde a la frecuencia absoluta de mujeres del grupo, por ende P7
i=1 mi = M
De esta forma, la primera columna Total corresponde a una frecuancia absoluta, mientras
que las dos siguientes (Prop. Hombres y Prop. Mujeres ) corresponden a una proporci´on.
Para la primera columna no utilice decimales, y para las segunda y tercera entregue las
participaciones de cada g´enero con 3 decimales.

# (γ) Caracterice la Cotizaci´on Previsional (o29) de la poblaci´on chilena construyendo el Cuadro
(3). Para esto usted deber´a notar que este Cuadro no cuenta con una fila final llamada
Total como aparec´ıa en las anteriores. Esto se debe a que este Cuadro representa solamente
participaciones porcentuales, por ende, la suma vertical de cada columna debe ser igual a uno
(100 %), o en t´erminos formales . P8
i=1 αi =
P8
i=1 βi =
P8
i=1 δi = 100 %. Entregue sus
valores usando 3 decimales.

# Generaci´on de Variables (35 %)

# Nivel Principiante (15 %)
Siguiendo con la base utilizada en la secci´on anterior realice lo siguiente:
(a) Genere una variable llamada n comuna que contenga la cantidad de personas que fueron
encuestadas en cada comuna.
(b) Genere una variable llamada decil de ingreso que contenga los deciles de ingreso para la
variable yoprcor. Adem´as de esto, esta variable deber´a contener etiquetas sobre los valores
de modo que cuando, por ejemplo, ejecutemos un “tabulate” sobre esta, aparezca en el primer
decil (asociado al valor 1) el texto “Primer Decil de Ingreso”, para el segundo “Segundo
Decil de Ingreso” y as´ı sucesivamente. Recuerde que los deciles deben contener el 10 % de la
poblaci´on en cada uno de sus tramos, sea cuidadoso a la hora de revisar si la forma en la que
realiz´o sus deciles cumple con esta condici´on.
(c) Genere una variable que Dummy que tome el valor de 1 si el encuestado reside en la Regi´on
Metropolitana y 0 en caso contrario. Adem´as de esto etiquete dicha variable el string “Encuestado en Regi´on Metropolitana”. Adicionalmente, etiquete los valores iguales a 1 con
el string “Regi´on Metropolitana”, y los ceros con “Regi´on Diferente a la Metropolitana”
(d) Genere una variable que contenga la cantidad mujeres que ganan m´as de un mill´on de pesos
(“yoprcor”) por regi´on.

Nivel Experto (20 %)
A usted se le ha entregado la base da datos base productos la cual contiene 6 variables que
caracterizan el desempe˜no econ´omico de una serie de firmas entre el a˜no 2000 y 2006 para diferentes
productos que estas comercializaron en dicho periodo. Las variables contenidas en la base se detallan
a continuaci´on:
firma : Corresponde al identificador de la Firma (i)
year: Variable Indicador que identifica el periodo t de la firma (i).
id prod: Variable que identifica el producto (j) vendido en el periodo (t) por la firma (i).
meta ventas: Corresponde a la meta de ventas que se propuso lograr la firma (i) durante el
periodo (t) para el producto (j).
ventas: Corresponde a las ventas reales que realiz´o la empresa (i) durante el periodo (t) para
el producto (j).
costos Corresponde a los costos en los que incurri´o la firma (i) durante el periodo (t) para
el producto (j)
A continuaci´on usted deber´a resolver las siguientes preguntas:
1. Genere una variable llamada prod loss que identifique los productos que no lograron cubrir
sus costos independiente de la firma que lo produjo y el tiempo en el que fue vendido. Esta
variable debe tomar el valor de 1 si el costo no fue cubierto, un 0 para aquellas firmas que si
lograron cubrirlos.
2. Genere una variable llamada y prod loss y que tome el valor de 1 para todo el periodo t
de operaci´on si es que, al menos uno, de los productos no logr´o cubrir sus costos
3. Genere una variable que muestre si es que el producto j est´a cumpliendo su meta de ventas
independiente de la firma que lo produjo y el tiempo en el que fue vendido. Llame a esta
variable cumple meta
4. Genere una variable que tenga por nombre cumple meta todos que tome el valor de 1
para todo el periodo t si es que la firma logr´o cumplir sus metas de ventas en TODOS
sus productos j y un 0 si es que fracas´o en cumplir sus metas de ventas en al menos un
producto.
5. Genere una variable que muestre el promedio de ventas por firma (i) y a˜no (t) y ll´amela
ventas mean.
6. Genere una variable llamada costos mean que muestre el promedio de los costos por firma
(i) y a˜no (t).
7. Adicionalmente deber´a crear una variable llamada prod mas vendido que contenga el producto que tuvo la mayor cantidad de ventas por periodo y firma.

Al finalizar esta parte usted deber´ıa terminar con una base de datos que, para la primera
firma, deber´ıa lucir como lo que se muestra en la Tabla (8). Ac´a debe tener cuidado, muchas
de las variables anteriores requieren de una serie de variables auxiliares que se combinan con
el uso de bys, egen y gen para ser construidas, por lo que no intente generar cada una
de las variables anteriores con “una sola linea de c´odigo”, hay un par que son un poco m´as
complejas que eso y requieren dos o tres.


# Presentaci´on de Estimaciones (30 %)
(a) Basado en el trabajo de Rajan & Zingales 1995, sobre estructura de capital de las firmas. Se
pide que replique la Tabla (4), haciendo uso del comando outreg2. (Loops ser´an bonificados, mas
no penalizados). Las variables que necesitar´a ocupar son : leverage tang market book ln sales y
prof las cuales se encuentran disponibles en la BASE base present resultados.dta

(b) Ahora agregue como control la variable Edad de la firma (age), pero no reporte el coeficiente,
sino que despliegue una nota explicativa sobre que se est´a controlando por dicha variable en las
estimaciones del Cuadro (5)

(c) Ahora sobre la Cuadro (5), agrupe las variables Tangibility (tang) y Market to book Ratio
(market book) en un grupo de variables llamado “Assets” y las variables Logaritmo de las
Ventas (ln sales) y Profit (porf ) en otro llamado “Performance”. Es decir replique la Cuadro
(6)
Cuad






