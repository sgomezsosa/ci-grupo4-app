#Continuous Integration Grupo4 Application REST Api
	Este archivo prentende ser una guia útil para quienes deseen levantar y usar la aplicación.

#Contenido
	A través de esta aplicación es posible registrar empleados y posteriormente modificar sus datos.

# Pre-requisitos
	A continuación se enumera una lista de requisitos necesarios para poder clonar y finalmente hacer delpoy del proyecto:

		1.- JDK Java 1.8 o superior.
		2.- Gradle 6.6.x o superior.
        3.- IDE IntelliJ versión 2019 o superior.

	Una vez descargadas e instaladas estas aplicaciones asegurese de agregar las rutas tanto de su versión de Java cómo de Gradle al classpath, de la siguiente manera: 

	$ Para usuarios GNU/Linux/Mac:
		export PATH=$PATH:/opt/java/jre1.8.0_171/bin
		export PATH=$PATH:/opt/gradle/gradle-6.0.1/bin

	$ Para usuarios Windows:
		En Explorador de Archivos, haga click derecho sobre el icono Este Equipo, luego Propiedades -> Configuración Avanzada del Sistema -> Variables de Entorno.

		En Variables de Entorno seleccione Path, luego click Editar y agregue una línea tanto para Java (ej: C:\Program Files\Java\jre1.8.0_171\bin), cómo Gradle (ej: C:\Gradle\gradle-6.6.1\bin)

		Finalmente haga click en Aceptar para finalizar.


	Finalmente verifique la instalación ejecutando los siguientes comandos en una Temrinal:
		Para Java: 
			java -version

		Para Gradle:
			gradle -v		

#Clonar Repositorio
	Para obtener el repositorio a través de git, debe seguir los pasos que comentan a continuación:

		1.- Clonar el proyecto desde la url: https://github.com/sgomezsosa/ci-grupo4-app.git mediante el comando:
		    git clone https://github.com/sgomezsosa/ci-grupo4-app.git

	Una vez realizado estos dos pasos debe esperar a que el proyecto se descargue en su totalidad y ya estaría listo para hacer deploy o importarlo a un editor de texto para realizar algún tipo de modificación.

# Deploy
	Una vez descargado el proyecto vaya a la ubicación donde se clono el repositorio y habra una consola Windows para ejecutar los siguientes comandos:
		
		1.- Descargar todas las librerías y realizar las compilación:
		    gradle build

		2.- Finalmente para correr el proyecto debe ejecutar:
		    gradle bootRun

# Uso del Proyecto
	Cabe destacar que el proyecto integra una versión de base de datos in memory de H2, la cual sólo está disponible una vez que la aplicación está corriendo, lo que implica que al cerrar la aplicación se perderán todos los datos. 

        1.- Para acceder a la aplicación: 
			En su navegafor ir a la URL: http://localhost:8080/

        2.- Para acceder a la consola de H2: 
			En su navegafor ir a la URL: http://localhost:8080/h2

			Debe hacer sólo click en aceptar para ingresar y poder visualizar las tablas disponibles. En caso de duda, los datos para ingresar a la consola H2 son los siguientes:
			Saved Settings: Generic H2 (Embebed)
			Setting Name: Generic H2 (Embebed)
			Driver Class: org.h2.Driver
			JDBC URL: jdbc:h2:mem:memDb
			User Name: sa
			Password: (vacío)