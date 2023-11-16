# efipp1_parte2_marcos_saez
Un blog simple hecho en Flask

# Descripción:
Este sería mi proyecto de la efi, un blog en el que uno se puede registrar, iniciar sesión y realizar publicaciones 
(de ser el propio usuario que hizo dicha publicación podrás editarla y borrarla)

la aplicación se conecta a una base de datos que registra usuarios(id, nombre y contraseña)
y también registra las publicacione(id, titulo, contenido, autor y fecha de publicación)

# Instrucciones:
Una vez que tengamos la carpeta con el archivo habría que instalar las dependencias
para esto abrimos la terminal en el proyecto
`pip install -r requirements.txt`

tras eso escribe:
`flask run`

y te aparecerá lo siguiente:
`Running on http://127.0.0.1:5000`
(solo debes ingresar hhttp://127.0.0.1:5000 en tu buscador predilecto)

si quieres parar el proyecto solo utiliza "Ctrl+C"

# Cosas que no pude añadir
lamentablemente no pude implementar Marshmallow para la autenticación 
ni tampoco pude refactorizar con methodview() como se me pedía

Integrantes:
Marcos Saez
2do comisión A 2023
