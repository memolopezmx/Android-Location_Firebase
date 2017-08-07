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
        Copiaremos el archivo .JSON en la carpeta <i>APP</i>. Seleccionamos la ésta carpeta, clic derecho y SHOW IN EXPLORER.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img10.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Entramos a la carpeta App.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img11.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Pegamos nuestro archivo .JSON
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img12.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        Regresamos y seleccionamos <i>Android</i>
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img13.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        En Android Studio seleccionamos Grandle Scripts > Build Grandle Project y pegamos: <i>classpath 'com.google.gms:google-services:3.1.0'</i> (o el que nos idique Firebase) dentro de buildscript > dependencies
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img15.png" width="682" height="365">     
    </p>
    </li>
    <li>
    <p align="justify">
        En Android Studio seleccionamos Grandle Scripts > Build Grandle APP y pegamos: <i>classpath 'apply plugin: 'com.google.gms.google-services'</i> (o el que nos idique Firebase) en la última linea de códig. Así mismo agregamos dentro de dependencies las dependencas que vayamos a usar las podemos consultar en <a href="https://firebase.google.com/docs/android/setup">la documentación oficial</a>.
    </p>
    <p align="justify">
        NOTA: En mi caso tuve problemas importando dependencias por las versiones que me marcaba este <a href="https://www.youtube.com/watch?v=TN4W5Gjd38c">tutorial</a> con las versiones de la documentación oficial (10.2.1) no tuve ningun problema, pero tuve problema cuando lo integre con Google Maps ya que la versión de mis mapas es (11.0.2) entonces a todas las dependencias les puse 11.0.2 y no tuve ningun problema.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img16.png" width="682" height="365">     
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
* <a href="https://www.youtube.com/watch?v=TN4W5Gjd38c">Dependencias - Agregando Firebase a tu proyecto Android</a>
