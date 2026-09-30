## Curso de Métodos Estadísticos
+ Curso de Métodos Estadísticos Ago 2026 




## Semana 2

+ Inicio del curso 12/08/26
+ Organizar mi área de trabajo
+ Crear cuenta en Github
+ Crear primer repositorio
+ Modificar el archivo README

+ 13/08/26 Segunda clase Metodos Estadisticos
+ Activar credenciales
+ Crear usuario en Gitbash
+ Credencial aprobada

## Semana 3 Metodos Estadisticos 19/08/26
+ Caleb Zarate Solis
+ 2187299
+ 19/08/26

+ Importar datos
+ Usar la funcion #read.cvs# para importar datos de excel
+ Declarar la columna tratamiento como factor y sus 2 niveles
+ utilice la funcion #as.factor##

 Obs <- read.csv("VIVERO.csv", header= TRUE)
 Obs$Tratamiento <- as.factor (Obs$Tratamiento)
 Obs$Tratamiento
 
 #Grafica----
 
 #Boxplot de los datos
 
boxplot(Obs$IE ~ Obs$Tratamiento,
xlab = "Factor = Fertilizante", 
ylab = "Indice (IE)",
col = "blue",
main = "Unidad experimental")

#Conocer la varianza de cada grupo

df_ctrl <- subset(Obs, Tratamiento == "Ctrl")
df_ctrl <- subset(Obs, Tratamiento != "Ctrl")
df_fert <- subset(Obs, Tratamiento == "Fert")

var(df_ctrl$IE
)
var(df_fert$IE)

mean(df_ctrl$IE
)
mean(df_fert$IE
)

#La varianza del grupo fertilizado es 3 veces mayor que la
#Varianza del grupo control
#Preguta
#¿Provienen de una distribucion normal ambos grupos?
shapiro.test(df_ctrl$IE)
#Grupo ctrl proviene de una distribucion normal
shapiro.test(df_fert$IE)
# Grupo fert sigue una distribucion normal

# ¿Seran las varianzas iguales o diferentes estadisticamente?

var.test(df_ctrl$IE, df_fert$IE)
# Las varianzas de ambos grupos son iguales

#Existen diferencias entre los tratamientos

t.test(df_ctrl$IE, df_fert$IE, var.equal = TRUE)

# Si la pregunta es que el Fert es mayor que Ctrl
t.test(df_ctrl$IE, df_fert$IE, var.equal = T,
       alternative = "greater")
   
   
## Semana 3 clase 4 Metodos Estadisticos 20/08/26





hhjsk






#Clase Metodos Estadisticos 09/09/26

+Realize tarea de examen parcial




#Clase Metodos Estadisticos 17/09/26}
+Correlacion
+Importar datos de altura y diametro

erupciones <- data("faithful")
erupciones <- faithful


#Crear un grafico base para revisar el comportamiento de las dos variables numericas

plot(erupciones$waiting, erupciones$eruptions
 xlab = "Tiempo de espera (min)",
     ylab = "Duracion de la erupcion (min)",
     pch = 19, col = "red")
     
#Conocer el rango del tiempo
range(erupciones$waiting)


#Conocer el rango de la erupcion
range(erupciones$eruptions)

boxplot(erupciones$eruptions)
fivenum(erupciones$eruptio

+Cachana


#Clase Metodos Estadisticos 23/09/26
#Datos sin valor extremo
x1 <- c(1.2, 1.5, 1.7, 1.8)

summary(x1)

mean(x1)

median(x1)

var(x1)

sd(x1)


#Datos con valor extremo
x2 <- c(1.2, 1.5, 1.7, 1.8)
summary(x2)
mean(x2)
median(x2)
var(x2)
sd(x2)


anillos <- data.frame(
  Arbol = 1:40,
  RW = c(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
)

mean(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
mean(anillos$AnchoAnillo_mm)

me

median.default(c1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)

sd(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
sd(x3)

RW = c(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
)
median.default(c(RW = c(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
)
median((RW = c(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)
range.Date(1.42, 1.58, 1.71, 1.63, 1.85, 1.94, 2.06, 1.76, 1.68, 1.89, 2.14, 1.53, 1.79, 1.97, 2.23, 1.61, 1.82, 2.08, 1.73, 1.87, 1.91, 2.04, 1.76, 1.83, 2.12, 1.69, 1.57, 1.88, 2.21, 1.95, 1.74, 1.81, 2.09, 1.66, 1.92, 2.17, 1.72, 1.86, 2.02, 3.48)


#Clase Metodos Estadisticos 30/09/26

#correlacion continuacion

#ingresar pares de datos

x3 <- c(10.0, 8.0, 13.0, 9.0, 11.0, 14.0, 6.0, 4.0, 12.0, 7.0, 5.0)
y3 <- c(7.46, 6.77, 12.74, 7.11, 7.81, 8.84, 6.08, 5.39, 8.15, 6.42, 5.73)

mean(x3)
mean(y3)

cor.test(x3, y3)


#Grafica de los datos

par(mfrow = c(2,2))
plot(x3, y3, col= "blue",
      main= "Conjunto 3")
      
plot(x3, y3, col = "red",
      main= "Conjunto 3")  
      
plot(x3, y3, col= "green",
      main= "Conjunto 3")
      
plot(x3, y3, col= "gray",
      main= "Conjunto 3") 
      
hwdjh      
      



     





















 
 

