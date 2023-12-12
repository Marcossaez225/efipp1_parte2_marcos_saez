# efipp1_parte2_marcos_saez
Un blog simple hecho en Flask

# Descripción:
Este sería mi proyecto de la efi, un blog en el que uno se puede registrar, iniciar sesión y realizar publicaciones 
(de ser el propio usuario que hizo dicha publicación podrás editarla y borrarla)

la aplicación se conecta a una base de datos que registra usuarios(id, nombre y contraseña)
y también registra las publicacione(id, titulo, contenido, autor y fecha de publicación)
# Tecnologías usadas:
* Python
* Flask
* SQLAlchemy
* MySQL Workbench
* HTML
* Docker
  
# Instrucciones de Set-Up:

#Corriendo el programa de manera local con Xampp:

Para correrlo local se necesita una versión actualizada de python y Xampp para simular la base de datos de manera local. Se deben seguir los siguientes pasos:

Primero debemos clonar el repositorio de manera local. Una vez lo tengamos, entramos a su carpeta y creamos un archivo que debe ser llamado ".env", y dentro pegaremos la siguiente línea:
+
```
    SQLALCHEMY_DATABASE_URI=mysql+pymysql://root:pass_word225@localhost:3306/blog_db
```

Cuando el archivo '.env' está creado, el siguiente paso es crearle un entorno virtual a la aplicación con python e instalarle los requerimientos provistos, que incluyen Flask y SQLAlchemy, Marshmallow, entre otros. Creamos el entorno virtual con el siguiente comando:
```
  python3 -m venv venv
```

Ahora debemos ingresar dentro del entorno para instalarle los requerimientos. Si estamos en LINUX, lo hacemos con el siguiente comando:
```
  source venv/bin/activate
```

En cambio, en WINDOWS es de la siguiente manera:
```
   venv/Scripts/activate
```

Una vez activado el entorno virtual, le vamos a instalar los requerimientos con el siguiente comando:
```
  pip install -r requirements.txt
```

Ahora, sin cerrar la terminal, abriremos Xampp e iniciaremos sus servicios. En windows puede ser abierto su acceso directo, pero en linux debemos ingresar el siguiente comando:
```
  sudo /opt/lampp/manager-linux-x64.run
```

Una vez abierto, y con sus servicios inicializados, queda crear e iniciar la base de datos. Ingresaremos al módulo de base de datos de Xampp y la creamos con el siguiente nombre:
```
  blog_db
```

de tener otro nombre la aplicación NO FUNCIONARÁ. Para iniciarla, volveremos a la terminal donde tenemos activado el entorno virtual e ingresaremos los siguientes comandos:
```
  flask db init
  flask db migrate -m "creacion de tablas"
  flask db upgrade
```

y finalmente, corremos el proyecto con un:
```
  flask run
```

y accedemos a localhost:5000. Con eso, estás listo para disfrutar el miniblog!

# Cosas que no pude añadir:
lamentablemente no pude implementar Marshmallow para la autenticación 

lo siento mucho.

# Integrantes:
Marcos Saez
2do comisión A 2023
