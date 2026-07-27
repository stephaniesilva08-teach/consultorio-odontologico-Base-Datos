# consultorio-odontologico-Base-Datos
Resultado prompt caso estudio:

prompt:

Generame un  caso de estudio de un consultorio odontologico , que permita usarla como contexto para realizar un modelo entidad-relacion


resultado:

## 🦷 Caso de Estudio: Consultorio Odontológico “Sonrisa Vital”

### 📌 Contexto General

El consultorio odontológico **“Sonrisa Vital”** es un centro de atención dental que ofrece servicios como limpiezas, ortodoncia, endodoncia, cirugías y estética dental. El consultorio cuenta con varios odontólogos especializados, asistentes y personal administrativo.

El objetivo del sistema es **gestionar pacientes, citas, tratamientos, pagos e historial clínico**, optimizando la atención y el control de la información.

---

## 👥 Actores principales

1. **Pacientes**

   * Se registran con: documento, nombre, fecha de nacimiento, teléfono, dirección y correo.
   * Un paciente puede tener múltiples citas.
   * Tiene un historial clínico asociado.

2. **Odontólogos**

   * Tienen: ID, nombre, especialidad (ortodoncia, cirugía, etc.), teléfono y correo.
   * Atienden múltiples pacientes.
   * Pueden realizar diferentes tratamientos.

---

## 📅 Gestión de Citas

* Cada **cita** tiene:

  * ID
  * Fecha y hora
  * Estado (programada, cancelada, completada)
  * Motivo de consulta

* Relaciones:

  * Un paciente puede tener muchas citas.
  * Una cita es atendida por un odontólogo.

---

## 🩺 Tratamientos

* Los tratamientos incluyen:

  * Limpieza
  * Blanqueamiento
  * Ortodoncia
  * Endodoncia
  * Extracciones

* Cada tratamiento tiene:

  * ID
  * Nombre
  * Descripción
  * Costo

* Relaciones:

  * Una cita puede incluir uno o varios tratamientos.
  * Un tratamiento puede aplicarse en múltiples citas.

---

## 📋 Historial Clínico

* Cada paciente tiene un historial clínico que incluye:

  * Diagnósticos
  * Observaciones
  * Tratamientos realizados
  * Fecha de registro

* Relación:

  * Un paciente tiene un único historial clínico.
  * El historial se actualiza en cada cita.

---

## 💰 Facturación y Pagos

* Cada cita genera una **factura**:

  * ID factura
  * Fecha
  * Total
  * Estado de pago

* Los pagos incluyen:

  * Método (efectivo, tarjeta, transferencia)
  * Monto
  * Fecha

* Relaciones:

  * Una factura pertenece a una cita.
  * Una factura puede tener uno o varios pagos.

---

## 🧩 Posibles Entidades para el Modelo ER

Puedes construir tu modelo con estas entidades:

* Paciente
* Odontólogo
* Cita
* Tratamiento
* Historial Clínico
* Factura
* Pago

---

## 🔗 Relaciones clave (muy importante para tu ER)

* Paciente **1:N** Cita
* Odontólogo **1:N** Cita
* Cita **N:M** Tratamiento
* Paciente **1:1** Historial Clínico
* Cita **1:1** Factura
* Factura **1:N** Pago

