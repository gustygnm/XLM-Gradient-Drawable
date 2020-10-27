# XLM Gradient Drawable

### Boilerplate
In order to create a gradient, you create an xml file in res/drawable. I am calling mine gradient.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
    <gradient
        android:type="linear"
        android:angle="0"
        android:startColor="#f6ee19"
        android:endColor="#115ede" />
</shape>
```

You set it to the background of some view. For example:
```
<View
    android:layout_width="200dp"
    android:layout_height="100dp"
    android:background="@drawable/my_gradient_drawable"/>
```

## type="linear"
Set the ```angle``` for a ```linear``` type. It must be a multiple of 45 degrees.
```
<gradient
    android:type="linear"
    android:angle="0"
    android:startColor="#f6ee19"
    android:endColor="#115ede" />
```

![Image](https://i.stack.imgur.com/zv2Ap.png)

## type="radial"
Set the ```gradientRadius``` for a ```radial``` type. Using ```%p``` means it is a percentage of the smallest dimension of the parent.
```
<gradient
    android:type="radial"
    android:gradientRadius="10%p"
    android:startColor="#f6ee19"
    android:endColor="#115ede" />
```
![Image](https://i.stack.imgur.com/xjWvp.png)

## type="sweep"
I don't know why anyone would use a sweep, but I am including it for completeness. I couldn't figure out how to change the angle, so I am only including one image.
```
<gradient
    android:type="sweep"
    android:startColor="#f6ee19"
    android:endColor="#115ede" />
```

![Image](https://i.stack.imgur.com/D6yg3.png)

## center
You can also change the center of the sweep or radial types. The values are fractions of the width and height. You can also use ```%p``` notation.
```
android:centerX="0.2"
android:centerY="0.7"
```
![Image](https://i.stack.imgur.com/JVicL.png)
