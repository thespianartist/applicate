


Uriel Ramirez @thespianartist
u@platzicom


1) Agregando Librerias:



    //Libreria para agregar un Floating Action Button
    compile 'com.android.support:design:22.2.0'


http://www.materialpalette.com/green/amber


2) Agregando Color.xml:

    <?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="primary_color">#E91E63</color>
    <color name="primary_dark_color">#AD1457</color>
    <color name="accent_color">#69F0AE</color>
</resources>


3) Importanto Colors en Theme:

<resources>

    //Darle el aspecto material, necesitamos configirar
    <style name="AppTheme" parent="Theme.AppCompat.NoActionBar">

        <item name="colorPrimary">@color/primary_color</item>
        <item name="colorPrimaryDark">@color/primary_dark_color</item>
        <item name="colorAccent">@color/accent_color</item>

    </style>

</resources>

4) Creando un Toolbar.xml


<android.support.v7.widget.Toolbar 
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/activity_my_toolbar"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:minHeight="?attr/actionBarSize"
    android:background="@color/primary_color"
    app:theme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"
    app:popupTheme="@style/ThemeOverlay.AppCompat.Dark.ActionBar"/>


    Toolbar toolbar = (Toolbar) findViewById(R.id.activity_my_toolbar);

    setSupportActionBar(toolbar);


    <include
        layout="@layout/toolbar"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />


5) Agregando FloatButton


    <android.support.design.widget.FloatingActionButton
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        app:layout_anchor="@id/appbar"
        app:layout_anchorGravity="bottom|right|end"
        app:fabSize="normal"
        app:elevation="2dp"
        android:src="@mipmap/ic_share_white_24dp"
        android:layout_margin="16dp"
        android:clickable="true"/>


Donde se guarda el APK:

mobile > build > outputs > apk





