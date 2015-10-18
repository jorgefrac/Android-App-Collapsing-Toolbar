# Theme Material Design
Para crear o personalizar nuestro propio tema de nuestra app en android studio basandose en el diseño de [Material Design](https://www.google.com/design/spec/material-design/introduction.html) 
tenemos que crear o ir a nuestro archivo **colors.xml** dentro de la carpeta **values** de android studio y generar nuestros colores a utilizar en el tema.

Para crear temas personalizados existe un sitio web llamado [material palette](https://www.materialpalette.com/) en el cual puedes escoger la combinación de colores que gustes, simulando un estimado de como se vera dentro de tu aplicación de android.

# styles.xml

<resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <!--Toolbar actions-->
        <item name="windowNoTitle">true</item>
        <item name="windowActionBar">false</item>
        <!--Theme Colors-->
        <item name="colorPrimary">@color/primary</item> 
        <item name="colorPrimaryDark">@color/primary_dark</item> 
        <item name="colorAccent">@color/accent</item>
    </style>

    <style name="CustomActionBar" parent="@style/ThemeOverlay.AppCompat.Dark.ActionBar">
        <item name="android:windowActionBarOverlay">true</item>
        <!-- Support library compatibility -->
        <item name="windowActionBarOverlay">true</item>
    </style>

    <style name="Widget.CardContent" parent="android:Widget">
        <item name="android:paddingLeft">16dp</item>
        <item name="android:paddingRight">16dp</item>
        <item name="android:paddingTop">24dp</item>
        <item name="android:paddingBottom">24dp</item>
        <item name="android:orientation">vertical</item>
    </style>

</resources>

# Librerías archivo build.gradle
Las librerías requeridas para realizar esta app son dos. La primera es para la utilización de los elementos [CardView](https://developer.android.com/reference/android/support/v7/widget/CardView.html) y la segunda es [Android Design Support Library](http://android-developers.blogspot.mx/2015/05/android-design-support-library.html) la cual nos sirve es para la utilización de [CoordinatorLayout](https://developer.android.com/reference/android/support/v7/widget/CardView.html). Para estas dos librerías tenemos que añadirlas a nuestro archivo **build.gradle** en la sección de dependencias.
