# Gradient-Artist - Android ImageView Library

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/Hariofspades/IncDec/blob/master/LICENSE)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-IncDec-blue.svg?style=flat)](https://android-arsenal.com/details/1/4784)

<img src=https://raw.githubusercontent.com/Hariofspades/Gradient-Artist/master/assets/wallpaper.png >

### Gradient ImageView 

Gradient-Artist library will allow you to use gradient overly on top of the image. It uses Glide for network image loading


### Usecase of Gradient-Artist ?
* Entertainment Apps to insert cover image and wallpapers
* Travel Apps to display locations 

### Why Gradient-Artist ?
* Take full control of the gradient creation
* Load image from URL, drawable and other resources

### Find this project useful ? :heart:
* Support it by clicking the :star: button on the upper right of this page. :v:

## Requirements

Gradient-Artist Library can be included in any Android application. 

Gradient-Artist Library supports Android 2.3 (Gingerbread) and later. 

## Using Gradient-Artist Library in your application

Add this in your build.gradle
```groovy
compile 'com.hariofspades.gradientartist:gradientartist:0.0.1'
```
Creating Gradient (drawable/alpha_gradient.xml)
```xml
<?xml version="1.0" encoding="UTF-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android" android:shape="rectangle" >

    <gradient
        android:angle="270"
        android:endColor="#DD8E54E9"
        android:startColor="#CC225AE0"
        android:type="linear" />

    <corners
        android:radius="0dp"/>

</shape>
```

Adding Gradient-Artist FAB in to the XML
```xml
<com.hariofspades.gradientartist.GradientArtistBasic
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:id="@+id/gradientImage"
    app:gradient="@drawable/alpha_gradient"
    app:imagePlaceholder="@drawable/weather"
    app:imageError="@drawable/weather"/>
```
Breaking down the attributes

app:gradient - gradient drawable
app:imagePlaceholder - Placeholder  for network image
app:imageError - Error placeholder for network  image

Load from Network - Java
```java
GradientArtistBasic gradient=(GradientArtistBasic) findViewById(R.id.gradientImage);
gradient.setUrlImage("https://img1.etsystatic.com/002/0/6449624/il_fullxfull.382134677_so6e.jpg",R.drawable.weather,
                R.drawable.weather, ImageView.ScaleType.CENTER_CROP);
```
Load from Drawable - Java
```java
GradientArtistBasic gradient=(GradientArtistBasic) findViewById(R.id.gradientImage);
gradient.setDrawableImage(R.drawable.me,R.drawable.weather,R.drawable.weather,
                ImageView.ScaleType.CENTER_CROP);
```
Load from Resource - Java
```java
GradientArtistBasic gradient=(GradientArtistBasic) findViewById(R.id.gradientImage);
gradient.setResImage(R.mipmap.ic_launcher,ImageView.ScaleType.CENTER_CROP);
```
Setting Gradient
```java
 Drawable myGradient = ContextCompat.getDrawable(this,R.drawable.alpha_gradient);
 gradient.setGradient(myGradient);
```

# Decoding the above function parameters

setUrlImage - image url, image error, image placeholder, ScaleType

setDrawableImage - Drawable, image error, image placeholder, ScaleType

setResImage - Res ID, ScaleType


##Happy Coding!!

### Let's get connected
- [Twitter](https://twitter.com/HariOfSpades)
- [Github](https://github.com/Hariofspades)
- [Medium](http://medium.com/@harivigneshjayapalan)
- [Facebook](http://facebook.com/Hari.Vignesh.J)

### License
```
   Copyright (C) 2016 Hari Vignesh Jayapalan
   Copyright (C) 2011 Android Open Source Project

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```
