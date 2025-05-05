**# LABORATORIO 1 CVDS 2025

## Primer Laboratorio de CVDS

**Objetivo:**  
El objetivo de este laboratorio es adquirir y reforzar los conocimientos fundamentales sobre Git y su uso en proyectos colaborativos. A través de la práctica de comandos básicos, los estudiantes aprenderán a gestionar versiones de código de manera eficiente, mejorando el trabajo en equipo y la colaboración en el desarrollo de software.

---

## PARTE I: Comandos Básicos de Git

### **`git add`**
Este comando se utiliza para **incluir cambios en el área de preparación (staging area)** antes de que se registren en el repositorio.  
Permite seleccionar qué modificaciones específicas del proyecto deseas incluir en tu próximo commit.

### **`git commit`**
Este comando se emplea para **guardar los cambios** que han sido añadidos al área de preparación en el repositorio local, creando una instantánea del estado actual del proyecto con un mensaje que describe los cambios realizados.

---

## Imágenes del Proceso


### Creación de directorios
1.Crea un repositorio localmente.

![Creación de directorios](Imagenes/Creacion%20de%20directorios.png)

### Agregando el archivo `README.md` 
2. Agrega un archivo de ejemplo al repositorio, el README.md 
![Agregando README](Imagenes/Agregando%20REAME.png)

### Creacion nuevo repositorio
![Nuevorepositorio](Imagenes/new%20repositorio.png)


### Configuración global de Git
Configura el correo en git local de manera correcta
![Configuración global](Imagenes/configuracion%20global.png)

### Realizando el push del `README.md`
Configura el repositorio local con el repositorio remoto.
![Push del README](Imagenes/push%20del%20README.png)

---

## Resumen

En este laboratorio hemos aprendido a usar los comandos básicos de Git para gestionar los cambios de un proyecto, incluyendo cómo agregar archivos al área de preparación, hacer commits y finalmente subir esos cambios al repositorio remoto.

---
**

### 2. Gestión de Elementos (Item Management)

| Método | Endpoint | Descripción | Parámetros | Cuerpo (Body) | Respuestas |
|--------|----------|-------------|------------|---------------|------------|
| GET | /api/items/{id} | Obtener elemento por ID | id: ID del elemento | - | 200: Elemento encontrado |
| PUT | /api/items/{id} | Actualizar elemento | id: ID del elemento | Objeto ItemEntity | 200: Elemento actualizado |
| DELETE | /api/items/{id} | Eliminar elemento | id: ID del elemento | - | 200: Elemento eliminado |
| POST | /api/items | Añadir nuevo elemento | - | Objeto ItemEntityRequest | 200: Elemento creado |
| GET | /api/items/search | Buscar elementos por nombre | name: Nombre a buscar | - | 200: Elementos encontrados |
| GET | /api/items/hall/{id} | Obtener elementos por sala | id: ID de la sala | - | 200: Elementos de la sala |
| GET | /api/items/category/{name} | Buscar elementos por categoría | name: Nombre de categoría<br>available: Filtro disponibilidad (opcional) | - | 200: Elementos de la categoría |
| GET | /api/items/all | Obtener todos los elementos | - | - | 200: Lista de elementos |

### 3. Gestión de Reservas (Booking Management)

| Método | Endpoint | Descripción | Parámetros | Cuerpo (Body) | Respuestas |
|--------|----------|-------------|------------|---------------|------------|
| GET | /api/bookings | Obtener todas las reservas | - | - | 200: Lista de reservas |
| POST | /api/bookings | Crear nueva reserva | - | Objeto BookingRequestDTO | 200: Reserva creada |
| POST | /api/bookings/{id}/return | Devolver una reserva | id: ID de la reserva | - | 200: Reserva devuelta |
| POST | /api/bookings/{id}/cancel | Cancelar una reserva | id: ID de la reserva | - | 200: Reserva cancelada |
| GET | /api/bookings/{id} | Obtener reserva por ID | id: ID de la reserva | - | 200: Detalles de la reserva |
| GET | /api/bookings/{id}/loans | Obtener préstamos por ID de reserva | id: ID de la reserva | - | 200: Préstamos asociados |
| GET | /api/bookings/user/{id} | Obtener reservas por ID de usuario | id: ID del usuario | - | 200: Reservas del usuario |

