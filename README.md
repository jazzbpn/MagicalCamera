[![alt tag](https://github.com/fabian7593/MagicalCamera/blob/master/cameraHighQ.png)](https://github.com/fabian7593/MagicalCamera)

A Magic library to take photos and select pictures in Android.
<br>
## SDK
* It requires **14+ API**.
<br>

## Getting Started

### Download Sources
use git (sourcetree or others)

```bash
git clone https://github.com/fabian7593/MagicalCamera.git
```

Download from [Here](https://github.com/fabian7593/MagicalCamera/zipball/master)

Another type download by Bintray from 
 

And you can add the jcenter bintray library in dependecies, like this:
```bash
  compile 'com.frosquivel:magicalcamera:1.0'
```
<br>
### What you need?
You need for usage the library in the best way, call any permissions in Android Manifest.xml
```bash
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
    <uses-permission android:name="android.permission.CAMERA"/>
```
<br>
### How to use
If you need to take photo or select picture, this is your solution.
This library give a magical solution for take a picture, you only need to download this and integrate this in your project, maybe downloading it or import in your gradle, like this.

```bash
repositories {
....
    jcenter()
}

dependencies {
....
    compile 'com.frosquivel:magicalcamera:1.0'
}
```
<br>
####Code Example to Use
You need to import the library
```bash
import com.frosquivel.magicalcamera.MagicalCamera;
```

You need to declare and constant or a simple int variable for the quality of the photo, while greater be, greater be the quality, and otherwise, worst be the quality, like this
```bash
//worst quality :( 
//private int RESIZE_PHOTO_PIXELS_PERCENTAGE = 50;

//a regular quality
private int RESIZE_PHOTO_PIXELS_PERCENTAGE = 1000;

//The best quality :D
//private int RESIZE_PHOTO_PIXELS_PERCENTAGE = 4000;
```

You need to instance the MagicalTakePhoto Class, like this:
```bash
 MagicalTakePhoto magicalTakePhoto =  new MagicalTakePhoto(this,RESIZE_PHOTO_PIXELS_PERCENTAGE);
```

You need to call the methods for take or select pictures:

```bash
magicalTakePhoto.takePhoto("my_photo_name");
magicalTakePhoto.selectedPicture("my_header_name");
```
<br>
######REMEMBER THAT
You need to override the method onActivityResult in your activity like this
```bash
 @Override
    public void onActivityResult(int requestCode, int resultCode, Intent data) {
        super.onActivityResult(requestCode, resultCode, data);
        magicalTakePhoto.resultPhoto(requestCode, resultCode, data);
        //If you need to obtain your photo you need to get this like that:
        imageView.setImageBitmap(magicalTakePhoto.getMyPhoto());
    }
```
<br>
######REMEMBER AGAIN
The photo only get in Bitmap Format and only when the  onActivityResult Event is shoot up.


<br><br>
##Documentation
All the code has a internal documentation for more explanation of this example.

<br><br>
##Preview of Example
![alt tag](https://github.com/fabian7593/MagicalTakePhoto/blob/master/image.gif)


<br><br>
## License
Source code can be found on [github](https://github.com/fabian7593/MagicalTakePhoto)<br>
Licenced under [APACHE 2.0](http://www.apache.org/licenses/LICENSE-2.0).
<br><br>

## About Developer
Developed by [Fabian Rosales](http://www.frosquivel.com)<br>
Known as [Frosquivel Developer](http://www.frosquivel.com)<br>
Web Page [www.frosquivel.com](http://www.frosquivel.com)<br>
Blog (Spanish) [www.frosquivel.com/blog](http://www.frosquivel.com/blog)<br>



