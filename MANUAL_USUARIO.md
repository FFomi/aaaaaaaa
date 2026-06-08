# Manual de usuario

## Proyecto: Gestion de Bruxismo

Este manual explica como utilizar la aplicacion web desde el punto de vista de los dos tipos de usuario disponibles:

- Medico.
- Paciente.

La aplicacion permite registrar usuarios, iniciar sesion, gestionar citas, consultar datos personales y asignar ejercicios o medicaciones.

---

## 1. Acceso a la aplicacion

Para entrar en la aplicacion, abrir el navegador y acceder a:

```text
http://localhost:5173
```

En la pantalla inicial aparece el formulario de inicio de sesion y la opcion de registro.

---

## 2. Registro de usuario

La aplicacion permite registrar dos tipos de usuario: paciente y medico.

### 2.1. Registro como paciente

1. Pulsar en la opcion de registro.
2. Seleccionar `Paciente`.
3. Completar los datos solicitados:
   - Nombre.
   - Apellido.
   - Email.
   - Password.
   - Fecha de nacimiento.
   - Sexo.
   - Telefono.
4. Pulsar `Registrarme`.

Si el email no existe previamente, el sistema mostrara un mensaje de registro correcto.

### 2.2. Registro como medico

1. Pulsar en la opcion de registro.
2. Seleccionar `Medico`.
3. Completar los datos solicitados:
   - Nombre.
   - Apellido.
   - Email.
   - Password.
   - Numero de colegiado.
   - Especializacion.
   - Centro medico.
   - Anos de experiencia.
4. Pulsar `Registrarme`.

Si los datos son correctos, el medico quedara registrado en el sistema.

---

## 3. Inicio de sesion

1. Introducir el email.
2. Introducir la password.
3. Pulsar `Entrar`.

Si las credenciales son correctas, la aplicacion abrira el panel correspondiente:

- Panel de medico, si el usuario registrado es medico.
- Panel de paciente, si el usuario registrado es paciente.

Si las credenciales no son correctas, se mostrara un mensaje de error.

---

# 4. Uso del panel de medico

El medico puede gestionar pacientes, citas, ejercicios y medicaciones.

## 4.1. Consultar agenda

Desde el panel de medico se puede consultar la agenda de proximas citas asociadas al medico que ha iniciado sesion.

La agenda muestra las citas futuras que estan en estado:

- `Programada`
- `Confirmada`

## 4.2. Crear una cita

Para crear una cita:

1. Acceder al apartado de agenda o gestion de citas.
2. Seleccionar el paciente.
3. Seleccionar el medico.
4. Introducir fecha y hora.
5. Seleccionar el tipo de cita.
6. Indicar el estado de la cita.
7. Guardar.

Tipos de cita disponibles:

- Consulta inicial.
- Seguimiento.
- Emergencia.
- Rutinaria.

Estados disponibles:

- Programada.
- Confirmada.
- Realizada.
- Cancelada.
- No se presenta.

Si ya existe una cita para el mismo medico en la misma fecha y hora, el sistema mostrara un error.

## 4.3. Cancelar una cita

Para cancelar una cita:

1. Localizar la cita.
2. Pulsar la opcion de cancelar.
3. Introducir el motivo de cancelacion.
4. Confirmar la accion.

El sistema no permite cancelar una cita sin indicar un motivo.

## 4.4. Gestionar pacientes

El medico puede acceder al listado de pacientes registrados.

Desde este apartado puede:

- Consultar pacientes.
- Abrir la gestion de un paciente concreto.
- Ver el resumen del paciente.
- Asignar ejercicios.
- Asignar medicacion.

## 4.5. Asignar un ejercicio a un paciente

Para asignar un ejercicio:

1. Entrar en la gestion de un paciente.
2. Seleccionar un ejercicio del catalogo.
3. Indicar la frecuencia.
4. Seleccionar la dificultad.
5. Indicar la fecha de inicio.
6. Guardar la asignacion.

El ejercicio quedara asociado al paciente y este podra verlo desde su panel.

## 4.6. Eliminar un ejercicio asignado

Para eliminar un ejercicio asignado:

1. Entrar en la gestion del paciente.
2. Buscar el ejercicio asignado.
3. Pulsar la opcion de eliminar.

La asignacion desaparecera del resumen del paciente.

## 4.7. Asignar una medicacion a un paciente

Para asignar una medicacion:

1. Entrar en la gestion de un paciente.
2. Seleccionar un medicamento del catalogo.
3. Indicar dosis, si procede.
4. Indicar frecuencia.
5. Indicar razon o motivo.
6. Seleccionar fecha de inicio.
7. Guardar.

La medicacion quedara asociada al paciente.

## 4.8. Eliminar una medicacion

Para eliminar una medicacion:

1. Entrar en la gestion del paciente.
2. Buscar la medicacion asignada.
3. Pulsar la opcion de eliminar.

---

# 5. Uso del panel de paciente

El paciente puede consultar sus citas, modificar sus datos y revisar ejercicios o medicaciones asignadas.

## 5.1. Consultar proximas citas

Desde el panel de paciente se puede acceder a la seccion de citas.

En esta pantalla se muestran las proximas citas del paciente, siempre que esten programadas o confirmadas.

## 5.2. Cancelar una cita

Para cancelar una cita:

1. Seleccionar la cita.
2. Pulsar la opcion de cancelar.
3. Escribir el motivo de cancelacion.
4. Confirmar.

La cita pasara a estado `Cancelada`.

## 5.3. Consultar datos personales

El paciente puede ver sus datos personales:

- Nombre.
- Apellido.
- Email.
- Telefono.
- Sexo.
- Fecha de nacimiento.

## 5.4. Modificar datos personales

Para modificar los datos:

1. Entrar en `Datos Paciente`.
2. Pulsar `Modificar datos`.
3. Cambiar los campos necesarios.
4. Pulsar `Guardar cambios`.

Los cambios se guardaran en la base de datos.

## 5.5. Consultar ejercicios asignados

El paciente puede ver los ejercicios que el medico le ha asignado.

La informacion mostrada puede incluir:

- Nombre del ejercicio.
- Estado.
- Frecuencia.
- Duracion.
- Instrucciones.

## 5.6. Consultar medicaciones

El paciente puede consultar las medicaciones asociadas.

La informacion mostrada puede incluir:

- Nombre del medicamento.
- Dosis.
- Frecuencia.
- Razon.
- Fecha de inicio.

---

# 6. Mensajes y errores frecuentes

## Email ya registrado

Aparece cuando se intenta registrar un usuario con un email que ya existe.

Solucion:

- Usar otro email.
- Iniciar sesion con el usuario ya creado.

## Email o password incorrectos

Aparece cuando las credenciales de inicio de sesion no son validas.

Solucion:

- Revisar que el email este bien escrito.
- Revisar la password.

## Paciente no encontrado

Aparece cuando se intenta gestionar un paciente que no existe.

Solucion:

- Actualizar la lista de pacientes.
- Comprobar que el paciente sigue registrado.

## Cita duplicada

Aparece cuando se intenta crear una cita para el mismo medico en la misma fecha y hora.

Solucion:

- Cambiar la hora.
- Seleccionar otro medico.

## Debe indicar razon de cancelacion

Aparece cuando se intenta cancelar una cita sin escribir motivo.

Solucion:

- Escribir el motivo antes de confirmar.

---

# 7. Recomendaciones de uso

- Crear primero al menos un medico y un paciente.
- Cargar los catalogos de ejercicios y medicamentos antes de probar asignaciones.
- Usar fechas futuras para comprobar correctamente las proximas citas.
- Revisar los mensajes de error que aparecen en pantalla.
- Cerrar sesion al terminar de usar la aplicacion.

---

# 8. Resumen de funcionalidades por rol

| Funcion | Medico | Paciente |
|---|---:|---:|
| Registrarse | Si | Si |
| Iniciar sesion | Si | Si |
| Consultar agenda/citas | Si | Si |
| Crear citas | Si | No |
| Cancelar citas | Si | Si |
| Consultar pacientes | Si | No |
| Modificar datos personales | No | Si |
| Asignar ejercicios | Si | No |
| Ver ejercicios asignados | Si | Si |
| Asignar medicacion | Si | No |
| Ver medicaciones | Si | Si |
