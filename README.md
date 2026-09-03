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












#Semana 5 Clase Metodos Estadisticos 03/09/26





















 
 

