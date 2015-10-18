# Theme Material Design
Para crear o personalizar nuestro propio tema de nuestra app en android studio basandose en el diseño de [Material Design](https://www.google.com/design/spec/material-design/introduction.html) 
tenemos que crear o ir a nuestro archivo **colors.xml** dentro de la carpeta **values** de android studio y generar nuestros colores a utilizar en el tema.

Para crear temas personalizados existe un sitio web llamado [material palette](https://www.materialpalette.com/) en el cual puedes escoger la combinación de colores que gustes, simulando un estimado de como se vera dentro de tu aplicación de android.

(https://raw.githubusercontent.com/jorgefrac/Android-App-Collapsing-Toolbar/master/Screenshots/colors_1.png)

(https://raw.githubusercontent.com/jorgefrac/Android-App-Collapsing-Toolbar/master/Screenshots/colors_2.png)

#colors.xml

```
<?xml version="1.0" encoding="utf-8"?>
 <resources>
    <!--THEME COLORS-->
    <color name="primary">#00BCD4</color>
    <color name="primary_dark">#0097A7</color>
    <color name="primary_light">#B2EBF2</color>
    <color name="accent">#FF4081</color>
    <color name="primary_text">#212121</color>
    <color name="secondary_text">#727272</color>
    <color name="icons">#FFFFFF</color>
    <color name="divider">#B6B6B6</color>
 </resources>
```

# styles.xml

```
<resources>
    <!-- Base application theme -->
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
```

# Librerías archivo build.gradle
Las librerías requeridas para realizar esta app son dos. La primera es para la utilización de los elementos [CardView](https://developer.android.com/reference/android/support/v7/widget/CardView.html) y la segunda es [Android Design Support Library](http://android-developers.blogspot.mx/2015/05/android-design-support-library.html) la cual nos sirve es para la utilización de [CoordinatorLayout](https://developer.android.com/reference/android/support/v7/widget/CardView.html). Para estas dos librerías tenemos que añadirlas a nuestro archivo **build.gradle** en la sección de dependencias.

```
dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile 'com.android.support:appcompat-v7:22.2.1'
    compile 'com.android.support:cardview-v7:22.2.1'
    compile 'com.android.support:design:22.2.1'
}
```

