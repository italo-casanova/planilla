# Proceso de seleccion

1. Puestos de trabajo -> gestion de solicitudes para los puestos

    * calificacion inicial: Muestra correos de personas interesadas
    * solicitudes: vista kanban de las etapas de los candidatos
    * en caso el postulante pase a una segunda fase:.

        >* Se enviara un correo de felicitacion para programar una entrevista.
        >* se pueden iniciar entrevistas desde el mismo odoo(es un formulario)

    * Control sobre las publicaciones de los puestos desde el modulo web <br>
      y la etapa en la que se encuentra.

2. Contrato

Incluye toda la gestion del proceso de contratacion del empleado, asi como la
informacion personal de este.
**Informacion relacionada con el plame y el sistema de registro**

* Luego de contratar al empleado se debe ingresar su informacion en el modulo *Empleado*
* Se puede tener un registro de sus habilidades y experiencia (hoja de cv en modulo empleados)
* Odoo esta integrado con la contabilidad.
* Al llenar la informacion se necesita crear un contrato, donde se creara un registro <br>
  con la informacion de la nomina:

  >I. salario

  >II. fechas de inicio y fin

  >III. tipo de paga

* Los empleados pueden tener mas de un contrato
* se relaciona al empleado con su asistencia (tarjeta, biometrio, etc)



# Informacion de empleados

El modulo de empleados no solo contiene informacion de cada empleado sino permite llevar
un contro de la asistencia y los contratos (Incluye estados)

* Al generar un contrato nuevo este aparecera en el aparto *Nuevo* en el modulo de
 empleados vista **Contratos**
* Las boletas se encuentran visibles en el apartado de nomimas para cada emplado
![informacion_del_trabajo](./images/recibos.png)

**Nota: La informacion que se encuentra en el apartado de *Informacion del trabajo* es publica
para todos los empleados**

![informacion del trabajo](./images/informacion_personal.png)

![organigrama](./images/organigrama.png)

# Gestion de la nomina

Manejo de toda actividad e incidencia que afecten el calculo de la nomina de un empleado

```
tardanzas
bonos
faltas
vacaciones
etc
```

1. Control del vacaciones
    >* Generar control de vaaciones desde el menu de empleados
    ![generar vacaciones](./images/generar_vacaciones.png)

    >* Agregar empleados al registro y generar el control

    ![generar vacaciones](./images/generar_control.png)

    > tanto el empleado como el gestor de nominas tendra podra ver la infrmacion de las
    > vacaciones

>1.1. El sistema de forma automatica calcula los dias de vacaciones ganador por trabajar un perido
de tiempo determinado
![vaciones](./images/vacaciones.png)
>1.2. EL modulo avisara cuando se exceda la fecha limite del disfrute de vacaciones
![manejo vacaciones](./images/manejo_vacaciones.png)

2. Control de Asistencias

  - Asistencias

    a. si el empleado tiene los permisos puede marcar su asistencia directamente en el modulo
    **Asistencia**
    ![registro manual de asistencia](./images/registro_asistencia_manual.png)
    b. caso contrario, se activara el modo quiosco, donde los empleados marcaran tarjeta
    o biometrico en un unica maquina<br>
    **modulo Asistencias, submenu administrar asistencias**
    ![modo quiosco](./images/modo_quiosco.png)
    c. Se pueden integran diferentes dispositivos de control de asistencia,
    **odoo se conectara directamente con los dispositivos por medio de su ip**
    ![multiples dispositivos](./images/multiples_dispositivos.png)

En el caso de tardanzas se tiene un rango de tolarencia antes de comenzar a descontar.

Caso similar con las horas extra, primero se tendra que validar el parte de horas,

  - Ausencias
    ![modulo ausencias](./images/ausencias.png)

    a. Empleado

    Se podran generar solicitudes de ausencia por parte de los empleados, asi como mantener un regisr
    de estas, incluyendo vacaciones
    ![solicitud ausencia](./images/submenu_asuncias.png)

    en las solicitudes de ausencia es necesario indicar el tipo, motivo, descripcion y fehcas de ausencia
    ![llenado ausencia](./images/llenado_ausencia.png)


    b. responsable

    El responsable puede crear registros de asistencia de forma similar a la solicitud
    de los empleados

    **_modulo ausencias_ submenu _Responsable_**
    ![ausencias responsable](./images/ausencias_responsable.png)
    ![llenado responsable](./images/llenado_ausencia_empleador.png)

# Otras solicitudes
```
solicitud de prestamo
solicitud de adelanto
aporbaciones
```
![otra solicitudes](./images/otras_solicitudes.png)

* En el caso de prestamos odoo genera automaticamente las cuotas, basado
en el numero de estas y la periodicidad
![prestamo](./images/prestamo.png)

* Para el caso de adelanto se descuenta de manera automatica el monto del pago en la
fecha indicata
![adelanto sueldo](./images/adelanto_sueldo.png)

# Nomina
![modulo nomina](./images/modulo_nomina.png)

1. Creacion de nomia

    El modulo de nomina incluye un formulario para crear la nomina de un periado
    determinado
    ![formulario nomina](./images/formulario_nomina.png)

    Al crear una nomina se deben indicar a que empleados se le incluira en estas
    ![incluir empleados nomina](./images/incluir_empleados_nomina.png)

    luego seleccionar a los empleados se calcula de forma automatica la nomina de cada uno

    **Esto permite tener una nomina diferente para cada tipo de pago o area de la organizacion**

2. Procesamiento
![procesamiento](./images/procesamiento_nomina.png)

    a. Renta de quinta
    ![acceso renta quinta](./images/acceso_renta_5ta.png)
    Muestra los detalles de como se calculo la renta de 5ta segun la normativa vigente
    ![renta quinta](./images/renta_5ta.png)

    b. Generar renta de quinta
    ![generar quinta](./images/generar_renta.png)
    las opciones que brinda odoo para calcular la renta de quinta son
    ```
    * contrato: empleado nuevo, sin informacion previa en la empresa, se usa
    la informaion del contrato para el calculo de la renta de quinta del mes
    * mes actual: proyecta en base a la informacion del mes cuando se le
    deberia realizar el descuento al empleado
    * mes anterior: se pryecta en base a la informacion del mes anterior
    ```

    notese que el modulo permite el calculo de renta para todos lo empleados que
    conformen la nomina asi como para solo un grupo de esta.

