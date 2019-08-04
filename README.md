# Proyecto Platzi

## Despliegue del proyeto

### Pre-Requisitos
Acá se deben desplegar todos los pre-requisitos para el proyecto, los cuales incluyen lo siguiente: 
*  Buckets.
*  Roles del pipeline.
*  Llaves KMS.
Para esta fase se debe desplegar primero --> https://github.com/czam01/cloudformation/tree/master/codepipeline 
*  Se puede crear una instancia de Cloud9 y se ejecuta el .sh, este ejecutará el template YML el cual desplegará todos los recursos necesarios de ahora en adelante para el proyecto.

### DynamoDB
Se debe realizar el despliegue de la BD DynamoDB la cual almacenará el registro de los votantes con la siguiente información:
*  DNI/CC
*  Nombre
*  Apellido
*  Dirección
*  Puesto de votación

Esta BD se debe desplegar con el siguiente template --> https://github.com/czam01/cloudformation/blob/master/nested/dynamo.yml 
Recuerden los parámetros de este template como Nombre y Key de la tabla, adicionalmente los datos de usuarios se deben ingresar de forma manual, en este despliegue solo se crea la tabla no la data dentro de ella.

### Pipeline y Lambda
Ahora debemos desplegar el pipeline que tendrá la función de automatizar el despliegue de nuestra serverless function.

1.  **Estructura del Repo:** Se debe dejar la estructura del repo con template.yml en la raiz y el código de la lambda igualmente, ver --> https://github.com/czam01/lambda-serverless

2.  **Creación manual del Pipeline:** Se debe crear el pipeline dentro de codepipeline siguiendo los siguientes pasos:

2.1  Crear el pipeline y seleccionar el role creado en los pre-requisitos.
![](https://github.com/czam01/lambda-payu/blob/master/images/i1.png)

2.2  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i2.png)
2.3  Agregar  codebuild como fase.
![](https://github.com/czam01/lambda-payu/blob/master/images/i3.png)
2.4  Crear proyecto de Codebuild.
![](https://github.com/czam01/lambda-payu/blob/master/images/i4.png)
2.5  Seleccionar la imagen del contenedor que se ejecutará en el Codebuild y también el role de codebuild creado en los pre-requisitos atenriormente.
![](https://github.com/czam01/lambda-payu/blob/master/images/i5.png)
2.6  Setear como variable de entorno el bucket creado en pre-requisitos.
![](https://github.com/czam01/lambda-payu/blob/master/images/i6.png)
2.7  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i7.png)
2.8  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i8.png)
2.9  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i9.png)
2.10  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i10.png)
2.11  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i11.png)
2.12  Agregar como source el repositorio en Github y autorizar la aplicación. Seleccionar el repo y la branch.
![](https://github.com/czam01/lambda-payu/blob/master/images/i12.png)








