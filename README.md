# FalabellaFinQaTest

Instrucciones

•	Descargar el código fuente desde https://github.com/JoseLContreras/FalabellaFinQaTest e importar en Postman la colección incluida en el repositorio con el nombre
de Transbank Test.postman_collection_JLC.json

•	Para ejecutar el código como requisito la máquina debe tener instalado
node.js luego los comandos `npm install` y `npm start` dejarán corriendo un
servidor local, el cual levanta una API REST.

El objetivo de la prueba es realizar un test automatizado que cree un usuario y luego verifique que dicho usuario fue creado con un campo adicional uuid. Dicho test fue creado con la funcionalidad de test Postman, se incluye una imagen de la colección con la entrada y la salida a testear, la cual ya esta incluida en el código.
Poner atención de que se debe dejar corriendo el método POST con el firstname, lastname y age  a incluir y luego hacer la misma consulta en el método GET (es indiferente si sigue haciendo “sending” el método POST), vienen incluidas las siguientes pruebas (con assertions en javascript):

1.	Status OK
2.	El tiempo de Response es menor de 1000ms
3.	Existe propiedad lastName
4.	Existe propiedad firstMame
5.	Existe propiedad age
6.	Existe propiedad id
7.	Estado 200

![image](https://user-images.githubusercontent.com/39358933/127357504-e4072191-4a0d-4453-9c56-8a873470c325.png)

Paso 1: Insertar (POST) datos requeridos en JSON.

![1step](https://user-images.githubusercontent.com/39358933/127359553-1264578e-027e-4ec8-9d62-3a0a14a7e835.PNG)

Paso 2: Validación de escritura eb BD.

![2step](https://user-images.githubusercontent.com/39358933/127359618-0fc741d5-acdc-4165-845a-e96ce1ef63c8.PNG)

Paso 3: Obtener (GET) datos con el uuid incluido en el response del body, inyectando JSON anterior.

![3step](https://user-images.githubusercontent.com/39358933/127359639-d6f0e441-69c2-47bb-b048-08fb34dc4f85.PNG)

Paso 4: Validación de los test contemplados en el GET.

![4step-test](https://user-images.githubusercontent.com/39358933/127359749-e107ee5a-7375-462d-baf5-144f24c3439d.PNG)


