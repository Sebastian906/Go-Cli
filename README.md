# Aplicación de lista de tareas hecha en Golang con interfaz en la terminal de consola

## ¿Como funciona?
1. Abrir la terminal de usuario en cualquier ambiente de programación
2. Ejecutar el comando de ejecución "go run ./ -list" (muestra la lista de tareas en la interfaz)
3. Para agregar una nueva tarea escribir: go run ./ -add "Nueva tarea"
4. Para editar esta nueva tarea escribir: go run ./ -edit "#id:Nueva tarea editada"
5. Para marcar la tarea como hecha escribir: go run ./ -toggle #id (#id --> identificador de tarea en especifico)
6. Para borrar una tarea de la tabla: go run ./ -del #id

## Clases principales
### 1. main.go

  Crea la lista de tareas 
  
  Llama a la clase storage para revisar y cargar las tareas creadas o guardadas 
  
  Recibe los comandos de la clase command para realizar el procedimiento
  
  Ejecuta el comando y guarda los datos en el storage

### 2. todo.go

  Define la estructura de la tarea (su nombre, si se ha terminado, cuando se creo, cuando se termino)
  
  Define los métodos para usarla en la aplicación (agregarla, borrarla, editarla, marcar como terminada, imprimirla)

### 3. command.go

  Define los comandos usados en la terminal para gestionar las tareas
  
  -add (Agregar tarea)
  
  -list (Ver todas las tareas)
  
  -toggle #id (Marcar tarea como completada)
  
  -del #id (Eliminar tarea)
  
  -edit "#id:Editar tarea" (Editar tarea de acuerdo a su identificador)

### 4. storage.go

  Guarda todas las tareas y las carga en un archivo todos.json

## Instalación

  git clone [link_del_repositorio]

  cd [dirección donde quedo el repositorio]

  go build -o [aplicación]

## Diagrama de clases:
![image](https://github.com/user-attachments/assets/496e46e4-673e-47a5-ba39-83aaf2f8adfe)
