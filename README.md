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
        <p align="center">
            <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img18.png" width="682" height="365">     
        </p>
            <p align="center">
                <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img19.png" width="682" height="365">     
            </p>
    </li>
    <li>
    <p align="justify">
        Una vez terminado estas configuraciones damos Async y ya podremos hacer uso de Firebase y sus librerias.
    </p>
    <p align="center">
        <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img20.png" width="682" height="365">     
    </p>
        <p align="center">
            <img src="https://github.com/ginppian/Android-Location_Firebase/blob/master/imgs/img21.png" width="682" height="365">     
        </p>
    </li>
</ol>

Para usar la DB basta con conseguir una instancia, pasar la referencia o ruta que queramos modificar:

```
    private void actualizarUbicacion(Location location) {
        if (location != null) {

            lat = location.getLatitude();
            lng = location.getLongitude();
            agregarMarcador(lat, lng);

            FirebaseDatabase database = FirebaseDatabase.getInstance();

            String sLat = String.format("%f", lat);
            String sLng = String.format("%f", lng);

            database.getReference("usr3/lat").setValue(sLat);
            database.getReference("usr3/lng").setValue(sLng);
        }
    }
```

Todo el código:

```
package mx.paracrecer.paracrecer1;

import android.Manifest;
import android.content.Context;
import android.content.pm.PackageManager;
import android.location.Location;
import android.location.LocationListener;
import android.location.LocationManager;
import android.os.Bundle;
import android.support.v4.app.ActivityCompat;
import android.support.v4.app.FragmentActivity;
import android.view.KeyEvent;

import com.google.android.gms.maps.CameraUpdate;
import com.google.android.gms.maps.CameraUpdateFactory;
import com.google.android.gms.maps.GoogleMap;
import com.google.android.gms.maps.OnMapReadyCallback;
import com.google.android.gms.maps.SupportMapFragment;
import com.google.android.gms.maps.model.BitmapDescriptorFactory;
import com.google.android.gms.maps.model.LatLng;
import com.google.android.gms.maps.model.Marker;
import com.google.android.gms.maps.model.MarkerOptions;
import com.google.firebase.database.FirebaseDatabase;

public class MapsActivity extends FragmentActivity implements OnMapReadyCallback {

    // Share Info
    private Bundle bundle;

    // Google Maps
    private GoogleMap mMap;
    private Marker marcador;
    double lat = 0.0;
    double lng = 0.0;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_maps);

        // Obtain the SupportMapFragment and get notified when the map is ready to be used.
        SupportMapFragment mapFragment = (SupportMapFragment) getSupportFragmentManager()
                .findFragmentById(R.id.map);
        mapFragment.getMapAsync(this);

        loadView();
    }

    private void loadView(){

        // Get Var MainActivity
        bundle = getIntent().getExtras();
        String correo = bundle.getString("miCorreo").toString();

        // Set title ActionBar
        //getActionBar().setTitle(correo);
        //getSupportActionBar().setTitle(correo);
    }

    // Block Back Button
    @Override
    public void onBackPressed() {
        moveTaskToBack(false);
    }

    // Block Back
    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if(keyCode== KeyEvent.KEYCODE_BACK) {
            return false;
        }
        return super.onKeyDown(keyCode, event);
    }

    /**
     * Manipulates the map once available.
     * This callback is triggered when the map is ready to be used.
     * This is where we can add markers or lines, add listeners or move the camera. In this case,
     * we just add a marker near Sydney, Australia.
     * If Google Play services is not installed on the device, the user will be prompted to install
     * it inside the SupportMapFragment. This method will only be triggered once the user has
     * installed Google Play services and returned to the app.
     */
    @Override
    public void onMapReady(GoogleMap googleMap) {
        mMap = googleMap;
        /*
        // Add a marker in Sydney and move the camera
        LatLng sydney = new LatLng(-34, 151);
        mMap.addMarker(new MarkerOptions().position(sydney).title("Marker in Sydney"));
        mMap.moveCamera(CameraUpdateFactory.newLatLng(sydney));
        */
        miUbicacion();
    }

    private void agregarMarcador(double lat, double lng) {
        LatLng coordenadas = new LatLng(lat, lng);
        CameraUpdate miUbicacion = CameraUpdateFactory.newLatLngZoom(coordenadas, 16);
        if (marcador != null) marcador.remove();
        marcador = mMap.addMarker(new MarkerOptions()
                .position(coordenadas)
                .title("Mi posición actual")
                .icon(BitmapDescriptorFactory.fromResource(R.mipmap.ic_launcher)));
        mMap.animateCamera(miUbicacion);
    }

    public static String locationStringFromLocation(final Location location) {
        return Location.convert(location.getLatitude(), Location.FORMAT_DEGREES) + " " + Location.convert(location.getLongitude(), Location.FORMAT_DEGREES);
    }

    private void actualizarUbicacion(Location location) {
        if (location != null) {

            lat = location.getLatitude();
            lng = location.getLongitude();
            agregarMarcador(lat, lng);

            FirebaseDatabase database = FirebaseDatabase.getInstance();

            String sLat = String.format("%f", lat);
            String sLng = String.format("%f", lng);

            database.getReference("usr3/lat").setValue(sLat);
            database.getReference("usr3/lng").setValue(sLng);
        }
    }

    LocationListener locListener = new LocationListener() {
        @Override
        public void onLocationChanged(Location location) {
            actualizarUbicacion(location);
        }

        @Override
        public void onStatusChanged(String s, int i, Bundle bundle) {

        }

        @Override
        public void onProviderEnabled(String s) {

        }

        @Override
        public void onProviderDisabled(String s) {

        }
    };

    private void miUbicacion() {
        if (ActivityCompat.checkSelfPermission(this, Manifest.permission.ACCESS_FINE_LOCATION) != PackageManager.PERMISSION_GRANTED && ActivityCompat.checkSelfPermission(this, Manifest.permission.ACCESS_COARSE_LOCATION) != PackageManager.PERMISSION_GRANTED) {
            // TODO: Consider calling
            //    ActivityCompat#requestPermissions
            // here to request the missing permissions, and then overriding
            //   public void onRequestPermissionsResult(int requestCode, String[] permissions,
            //                                          int[] grantResults)
            // to handle the case where the user grants the permission. See the documentation
            // for ActivityCompat#requestPermissions for more details.
            return;
        }

        LocationManager locationManager = (LocationManager) getSystemService(Context.LOCATION_SERVICE);
        Location location = locationManager.getLastKnownLocation(LocationManager.GPS_PROVIDER);
        actualizarUbicacion(location);
        locationManager.requestLocationUpdates(LocationManager.GPS_PROVIDER, 15000,0,locListener);
    }
}
```

## Fuente

* <a href="https://www.youtube.com/watch?v=TN4W5Gjd38c">Curso de Firebase en Android #1 La implementación </a>
* <a href="https://www.youtube.com/watch?v=1nDfMSdu49U">Curso de Firebase en Android #2 Bases de datos </a>
* <a href="https://stackoverflow.com/questions/15727912/sha-1-fingerprint-of-keystore-certificate">SHA-1 fingerprint of keystore certificate</a>
* <a href="https://www.youtube.com/watch?v=TN4W5Gjd38c">Dependencias - Agregando Firebase a tu proyecto Android</a>
