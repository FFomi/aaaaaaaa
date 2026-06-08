# Manual de instalacion

## Proyecto: Gestion de Bruxismo

Este manual explica como preparar y ejecutar la aplicacion en local. El proyecto esta formado por:

- Backend: FastAPI + SQLAlchemy.
- Frontend: React + Vite.
- Base de datos: MySQL.

---

## 1. Requisitos previos

Antes de iniciar el proyecto es necesario tener instalado:

- Python 3.
- Node.js y npm.
- MySQL Server.
- Un cliente para ejecutar scripts SQL, por ejemplo MySQL Workbench.

---

## 2. Preparar la base de datos

1. Abrir MySQL Workbench o el cliente MySQL usado habitualmente.

2. Crear la base de datos:

```sql
create database bruxismo;
```

3. Ejecutar el script principal:

```text
bbdd/creacion_database.sql
```

Este script crea las tablas principales del sistema: pacientes, medicos, citas, tratamientos, ejercicios y medicaciones.

4. Ejecutar el script de datos iniciales:

```text
bbdd/insert_catalogos_bruxismo.sql
```

Este script carga ejercicios y medicamentos de ejemplo para poder probar la aplicacion.

---

## 3. Configurar el backend

El backend utiliza las credenciales definidas en los archivos `.env` del proyecto. Revisar que la URL de conexion apunte a la base de datos local:

```text
mysql+pymysql://usuario:password@127.0.0.1:3306/bruxismo
```

La configuracion debe coincidir con el usuario y contrasena de MySQL.

---

## 4. Instalar dependencias del backend

Desde la raiz del proyecto, abrir una terminal y ejecutar:

```bash
pip install -r requirements.txt
```

Dependencias principales:

- `fastapi`
- `uvicorn`
- `sqlalchemy`
- `pymysql`
- `pydantic`
- `pydantic-settings`

---

## 5. Ejecutar el backend

Entrar en la carpeta del backend:

```bash
cd backend/bruxismo
```

Arrancar la API:

```bash
uvicorn app.main:app --reload --port 8000
```

Si todo esta correcto, la API quedara disponible en:

```text
http://127.0.0.1:8000
```

La documentacion automatica de FastAPI se puede abrir en:

```text
http://127.0.0.1:8000/docs
```

---

## 6. Instalar dependencias del frontend

Abrir otra terminal y entrar en la carpeta del frontend:

```bash
cd frontend
```

Instalar dependencias:

```bash
npm install
```

---

## 7. Ejecutar el frontend

Desde la carpeta `frontend`, ejecutar:

```bash
npm run dev
```

La aplicacion web quedara disponible normalmente en:

```text
http://localhost:5173
```

---

## 8. Comprobacion rapida

Para comprobar que todo funciona:

1. Abrir `http://localhost:5173`.
2. Registrar un medico.
3. Registrar un paciente.
4. Iniciar sesion.
5. Crear una cita.
6. Asignar un ejercicio o una medicacion a un paciente.

---

## 9. Problemas frecuentes

### Error de conexion con la base de datos

Comprobar:

- Que MySQL este iniciado.
- Que exista la base de datos `bruxismo`.
- Que el usuario y password del `.env` sean correctos.
- Que el puerto sea `3306`.

### El frontend no conecta con el backend

Comprobar que el backend este levantado en:

```text
http://127.0.0.1:8000
```

El frontend llama a la API mediante:

```text
http://127.0.0.1:8000/api/v1
```

### No aparecen ejercicios o medicamentos

Ejecutar el script:

```text
bbdd/insert_catalogos_bruxismo.sql
```

### Cambios que no se ven en pantalla

Refrescar el navegador con:

```text
Ctrl + F5
```

Si sigue igual, parar y volver a iniciar:

```bash
npm run dev
```

---

## 10. Comandos resumen

Backend:

```bash
pip install -r requirements.txt
cd backend/bruxismo
uvicorn app.main:app --reload --port 8000
```

Frontend:

```bash
cd frontend
npm install
npm run dev
```
