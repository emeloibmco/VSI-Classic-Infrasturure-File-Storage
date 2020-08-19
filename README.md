# VSI-Classic-Infrastructure-File-Storage

# GUIA DE INSTALACIÓN Y CONFIGURACIÓN DE UN FILE STORAGE EN UNA VSI 🚀

_Para el desarrollo de este proyecto se tiene como base el desarrollo de una aplicación basada en el lenguaje de programación angular y su posterior despliegue en un **Cluster de OpenShift** que se encuentra alojado en **IBM Cloud**._

### Indice
1. [Despliegue en OpenShift desde IBM Cloud shell](#Despliegue-en-OpenShift-desde-IBM-Cloud-shell-)
2. [Despliegue Aplicación Hello World en Angular](#despliegue-aplicación-hello-world-en-angular-🅰️)
3. [Despliegue Aplicación Listas en Angular](#despliegue-aplicación-listas-en-angular-🅰️)
4. [Despliegue Aplicación Hello World en Nodejs Desde la consola web de OpenShift ](#Despliegue-Aplicación-Hello-World-en-Nodejs-Desde-la-consola-web-de-OpenShift-)
5. [Despliegue de una imagen Docker en un contenedor de Opeshift](#Despliegue-de-una-imagen-Docker-en-un-contenedor-de-Opeshift-)
6. [Despliegue Aplicación CRUD en Angular](#Despliegue-Aplicación-CRUD-en-Angular-)
7. [Anexos](#ANEXOS)
8. [Pre-requisitos](#Pre-requisitos-)
9. [Referencias](#Referencias)

### Despliegue de los recursos 📦

## Despliegue de la vsi 📦
**PASOS:**
_1. Ingrese a IBM cloud desde el siguiente link:_
```
https://cloud.ibm.com/login
```
_2. Realice el login con sus credenciales de ingreso._


<p align="center">
![Captura de pantalla de 2020-03-26 17-25-55](https://user-images.githubusercontent.com/60987042/77702638-f8482580-6f86-11ea-9a83-9714df69ec38.png)
</p>


_3. Dirijase al catalogo de IBM Cloud y busque el recurso **Virtual Server**._

<p align="center">
<img width="960" alt="VSI-Catalogo" src="https://user-images.githubusercontent.com/60987042/90690094-bb7f1280-e236-11ea-8d20-52e5a3ef7393.PNG">
</p>

_4. Al dar clic en Virtual Server, se va a abrir una ventana en la cual debemos configurar las diferentes caracteristicas que queremos para nuestra maquina y al final damos clic en **create**._

<p align="center">
<img width="960" alt="carac-vsi" src="https://user-images.githubusercontent.com/60987042/90690127-c3d74d80-e236-11ea-84d5-4718ac0d47a4.PNG">
</p>

## Despliegue del File Storage 📦
**PASOS:**
_1. Ingrese a IBM cloud desde el siguiente link:_
```
https://cloud.ibm.com/login
```
_2. Realice el login con sus credenciales de ingreso._

<p align="center">
![Captura de pantalla de 2020-03-26 17-25-55](https://user-images.githubusercontent.com/60987042/77702638-f8482580-6f86-11ea-9a83-9714df69ec38.png)
</p>


_3. Dirijase al catalogo de IBM Cloud y busque el recurso **File Storage**._

<p align="center">
<img width="959" alt="file-Catalogo" src="https://user-images.githubusercontent.com/60987042/90690214-ebc6b100-e236-11ea-9c7f-e78cccbfd881.PNG">
</p>

_4. Al dar clic en File Storage, se va a abrir una ventana en la cual debemos configurar las diferentes caracteristicas que queremos para nuestro recurso y al final damos clic en **create**._

<p align="center">
<img width="959" alt="carac-file" src="https://user-images.githubusercontent.com/60987042/90690229-f3865580-e236-11ea-81ce-2ac22cd81401.PNG">
</p>

### Configuración file storage 📦

**PASOS:**
_1. Ingrese a IBM cloud desde el siguiente link:_
```
https://cloud.ibm.com/login
```
_2. Realice el login con sus credenciales de ingreso._

<p align="center">
![Captura de pantalla de 2020-03-26 17-25-55](https://user-images.githubusercontent.com/60987042/77702638-f8482580-6f86-11ea-9a83-9714df69ec38.png)
</p>

_3. Dirijase al resource list._

<p align="center">
<img width="696" alt="7" src="https://user-images.githubusercontent.com/60987042/76996077-da434b00-691e-11ea-92be-558da48f7d97.PNG">
</p>

_4. Dirigirse a la sección de **Storage**, y seleccione el que se desea._

<p align="center">
<img width="959" alt="FileStorage-resou" src="https://user-images.githubusercontent.com/60987042/90690340-2597b780-e237-11ea-95e4-8ed8ead3239f.PNG">
</p>

_5. Cuando estamos dentro del File Storage debemos dirigirnos a la seccion Authorized Hosts._

<p align="center">
<img width="960" alt="Authorized-Hosts" src="https://user-images.githubusercontent.com/60987042/90690349-29c3d500-e237-11ea-9957-4e5846e4ad4d.PNG">
</p>

_6. Cuando ingresamos a la seccion Authorized Hosts debemos dar clic en **Authorize Host**, y seleccionamos el virtual server al que queremos adicionarle el file Storage._

<p align="center">
<img width="960" alt="Authorize-Host" src="https://user-images.githubusercontent.com/60987042/90690352-2c262f00-e237-11ea-83bc-19ad9b32b5f6.PNG">
</p>

### Configuración VSI con el File Storage 📦

**PASOS:**

_1. Lo primero que debemos hacer es ingresar al virtual server por medio de SSH, mediante el siguiente comando._
```
ssh root@<Dirección Ip>
```

_2. Una vez ingresemos a la maquina ._

<p align="center">

</p>


_3. Una vez estemos en OpratorHub debemos buscar mediante el **Filter by keyword...** el operador correspondiente a **Eclipse-che**._

<p align="center">

</p>

_4. Al dar clic sobre Eclipse-che se nos va desplegar una nueva ventana en la cual debemos instalar el operador sin modificar ningun campo._


_5. Una vez instalado el operador, ingresamos y le damos clic en **Create CheCluster**._

<p align="center">
<img width="700" alt="create" src="https://user-images.githubusercontent.com/60987042/89837718-280b5a80-db2f-11ea-8201-867f97450fe3.PNG">
</p>


## Autores ✒️

_Equipo IBM Cloud Tech sales Colombia._
