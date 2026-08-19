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
# Declarar la columna tratamiento como factor y sus 2 niveles
# utilice la funcion #as.factor#

 Obs <- read.csv("VIVERO.csv", header= TRUE)
 Obs$IE
 Obs$Tratamiento <- as.factor (Obs$Tratamiento)
 Obs$Tratamiento
 
 #Grafica----
 
 #Boxplot de los datos
 
 boxplot(Obs$IE )
 #cACHANA

