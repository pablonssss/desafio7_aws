# desafio7_aws
Documentación sobre el desafío 7 del Bootcamp_Devops_Engineer de Educacion IT

**Crear una Cuenta de AWS:**

Entro a aws.amazon.com y presiono el botón "Create an AWS Account". Ingreso los datos solicitados, por seguridad Amazon envía un correo con un código, el cual obtengo el correo de verificación.

**Verificar la Cuenta:**

Finalizo de realizar el registro y selecciono el Plan de Soporte “free”.

**Acceder a la Consola de AWS:**

Ingreso a la URL aws.amazon.com/console 

**Crear un Grupo con Rol de Administrador:**

En la barra de búsqueda arriba se busca “IAM” --> A la izquierda, se selecciona la opción “User groups” --> Se selecciona el botón “Create New Group”, Se crea un nuevo “user group”, lo llamaremos “PNAminGroup”

En “Attach permissions policies” se busca la política “AdministratorAccess”, seleccionándose la casilla --> Se presiona en “Create user group” y queda creado

**Crear un Usuario con Rol de Administrador:**

Dentro de IAM, vamos ahora a la opción “Users” --> Se presiona el botón “Create user”, se ingresa un nombre (en este caso “pablonssss”) 

Selecciono las opciones “Provide user Access to the AWS Management Console” y debajo selecciono “I want to create an IAM user”, posteriormente le ingreso una contraseña 

En “Set permissions” se selecciona “Add user to group” y debajo seleccionamos la casilla del grupo creado anteriormente.

Luego de clickear en “Next”, revisamos los datos y presionamos en “Create User”

**Crear un Usuario con Rol de Billing**

El usuario con rol de “Billing”, es quien tiene los permisos para gestionar la información de la facturación de los servicios y los costos de lo contratado. La idea es que sea un usuario específico para esto y no tenga otro permiso de gestión sobre los recursos de AWS.

Dentro de IAM, seleccionamos nuevamente users y damos también el permiso a manejo de consola y lo configuramos como usuario IAM.

Posteriormente le configuramos una clave.

Lo distinto es que en la sección “Set permissions” vamos a seleccionar la opción “Attach policies directly”, debajo buscamos la política “Billing” y seleccionamos la casilla correspondiente a la misma.

Con esos pasos ya tenemos el usuario solamente con la opción “Billing” que es facturación.

**Asignar Permisos de Billing al Usuario BillingUser:**

Se ingresa a “My Account” y nos dirigimos a la sección “IAM User and Role Access to Billing Information”  -->  Seleccionamos “Edit” 

Marca la casilla que dice “Activate IAM Access”

El usuario “Pagos” con política “Billing” podrá ver y gestionar la información de facturación, costos y pagos.


