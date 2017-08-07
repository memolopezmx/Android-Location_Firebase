Android Aplication: Localización y Conexión DB Firebase
========

<p align="center">
    <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img1.png" width="270" height="480">
    <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img2.png" width="270" height="480">
</p>

## Descripción

<p align="justify">
    La presente aplicación busca obtener la ubicación del usuario y compartirla en tiempo real.
</p>

<p align="justify">
    Para lograr esto hacemos uso de una DB No Relacional que nos provee <i>Firebase</i>.
</p>

## Desarrollo

<ol>
    <li>
    <p align="justify">
        Añadimos un nuevo proyecto en nuestra consola de <a href="https://firebase.google.com">Firebase</a>
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img3.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Agregamos una nueva aplicación para <i>Android</i>.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img5.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Nos pide que copiemos el <i>IDENTIFICADOR</i> de nuestra aplicación, vamos a <i>Android Studio</i>.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img6.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Project Structure
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img7.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        App > Flavors > Application Id copiamos y lo pegamos.
    </p>
    <p align="justify">
        NOTA: Podemos agregar un SHA-1 que podriamos obtener con un comando en la consola de Android Studio (en mi caso no funciono), con Grandles (en mi caso desconfiguro mi proyecto), Creando un Activity de Mapas y copiando lo. En mi caso aun que obtuve el SHA-1 me causo problemas y no me asocio correctamente con Firebase. Como es opcional yo lo omití pero para más información puedes consultar el siguiente <a href="https://stackoverflow.com/questions/15727912/sha-1-fingerprint-of-keystore-certificate">tutorial</a>.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img8.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Al terminar de pegar nuestro Id y seleccionar continuar, nos genera un archivo .JSON lo descargamos y cambiamos a <i>PROJECT</i> para ver la gerarquia de archivos de nuestro proyecto.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img9.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img10.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Una vez creado seleccionamos nuestro proyecto, nos vamos a <i>Database</i> y a <i>REGLAS</i> y las modificamos ambas a <i>TRUE</i<:
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img4.png" width="682" height="365">     
    </p>
    </li>                                                                    
        
</ol>

## Fuente

* <a href="https://www.youtube.com/watch?v=TN4W5Gjd38c">Curso de Firebase en Android #1 La implementación </a>
* <a href="https://www.youtube.com/watch?v=1nDfMSdu49U">Curso de Firebase en Android #2 Bases de datos </a>
* <a href="https://stackoverflow.com/questions/15727912/sha-1-fingerprint-of-keystore-certificate">SHA-1 fingerprint of keystore certificate</a>