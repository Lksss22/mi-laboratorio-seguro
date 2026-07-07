
   # Hardening inicial de una Máquina Virtual

## Descripción
Este repositorio documenta la implementación de un proceso básico de **hardening inicial** sobre una máquina virtual, siguiendo una serie de buenas prácticas orientadas a mejorar su seguridad desde el primer momento de la instalación.

El trabajo se realizó sobre una máquina virtual creada en **VirtualBox**, configurando la red en modo **NAT**, verificando la instalación del sistema operativo, creando un **usuario con permisos limitados**, revisando el estado de las **actualizaciones del sistema**, deshabilitando componentes inseguros o innecesarios y generando una **instantánea (snapshot)** para conservar un punto seguro de restauración.

Además, se elaboró un **reporte en PDF** con las capturas y la explicación de cada paso realizado.

---

## Objetivo
Aplicar una configuración inicial de seguridad sobre una máquina virtual para reducir la superficie de ataque y dejar una base más segura para su uso posterior.

---

## Tecnologías y herramientas utilizadas
- **VirtualBox**
- **Sistema operativo virtualizado**
- **Configuración de red NAT**
- **Gestión de usuarios locales**
- **Actualización del sistema operativo**
- **Instantáneas / Snapshots**
- **Reporte técnico en PDF**

---

## Actividades realizadas

### 1. Creación de la máquina virtual
Se creó una máquina virtual en VirtualBox para realizar la práctica de hardening inicial.

### 2. Configuración de red en modo NAT
Antes de iniciar la máquina virtual, se configuró el adaptador de red en modo **NAT**.  
Esta configuración permite que la máquina virtual tenga acceso a internet sin quedar expuesta directamente a la red local, lo que representa una medida inicial de aislamiento y seguridad.

### 3. Instalación del sistema operativo
Se realizó la instalación del sistema operativo dentro de la máquina virtual para contar con un entorno funcional sobre el cual aplicar las medidas de seguridad solicitadas.

### 4. Creación de un usuario con permisos limitados
Se creó un usuario de tipo **estándar / no administrador** para evitar el uso cotidiano de una cuenta con privilegios elevados.  
Esta práctica reduce el riesgo de cambios no autorizados en el sistema y limita el impacto de posibles ejecuciones maliciosas.

### 5. Verificación y revisión de actualizaciones del sistema
Se accedió al centro de actualizaciones del sistema operativo con el objetivo de comprobar su estado y aplicar, cuando sea posible, las actualizaciones disponibles.  
Mantener el sistema actualizado es una de las medidas más importantes para corregir vulnerabilidades conocidas.

### 6. Deshabilitación de componentes inseguros o innecesarios
Como parte del hardening, se revisaron las características del sistema y se deshabilitó el protocolo **SMB 1.0/CIFS**, ya que se trata de una tecnología antigua con riesgos de seguridad conocidos.  
La eliminación o desactivación de componentes obsoletos ayuda a disminuir la superficie de ataque.

### 7. Creación de snapshot “hardening inicial”
Una vez aplicadas las configuraciones básicas de seguridad, se creó una instantánea llamada **“hardening inicial”**.  
Esto permite conservar un punto de restauración estable y seguro, útil para volver rápidamente al estado endurecido de la máquina en caso de errores o modificaciones futuras.

### 8. Elaboración del reporte final
Se compiló toda la evidencia en un **reporte PDF**, incluyendo capturas de pantalla y una breve explicación de cada paso realizado, justificando su importancia desde el punto de vista de la seguridad.

---

## Medidas de hardening aplicadas
Las principales acciones de endurecimiento implementadas fueron:

- Configuración de la red de la VM en **modo NAT**
- Creación de un **usuario estándar** con permisos limitados
- Revisión del estado de **actualizaciones del sistema**
- Desactivación de **SMB 1.0/CIFS**
- Generación de un **snapshot de respaldo seguro**

---

## Evidencias incluidas en el repositorio
El repositorio contiene:
- **Captura de la configuración de red NAT**
- **Captura del usuario estándar creado**
- **Captura de la desactivación de SMB 1.0/CIFS**
- **Captura del snapshot “hardening inicial”**
- **Reporte final en PDF**

---

## Estructura sugerida del repositorio
```text
hardening-vm/
├─ README.md
├─ Reporte_VM_Hardening_Completo_Lucas.pdf
└─ evidencias/
   ├─ red_nat_virtualbox.jpg
   ├─ usuario_estandar.jpg
   ├─ smb1_desactivado.jpg
   └─ snapshot_hardening_inicial.jpg
