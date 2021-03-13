# ZXing.Net 
![ZXing.Net.Mobile Logo](https://raw.githubusercontent.com/micjahn/ZXing.Net/master/Icons/logo.jpg)

## Project Description
A library which supports decoding and generating of barcodes (like QR Code, PDF 417, EAN, UPC, Aztec, Data Matrix, Codabar) within images.

The project is a port of the java based barcode reader and generator library ZXing.  
https://github.com/zxing/zxing  
It has been ported by hand with a lot of optimizations and improvements.

The following barcodes are supported by the decoder:
UPC-A, UPC-E, EAN-8, EAN-13, Code 39, Code 93, Code 128, ITF, Codabar, MSI, RSS-14 (all variants), QR Code, Data Matrix, Aztec and PDF-417.
The encoder supports the following formats:
UPC-A, EAN-8, EAN-13, Code 39, Code 128, ITF, Codabar, Plessey, MSI, QR Code, PDF-417, Aztec, Data Matrix

#### Assemblies are available for the following platforms:

* .Net 2.0, 3.5, 4.0, 4.5, 4.6 and 4.7
* Silverlight 4 and 5
* Windows Phone 7.0, 7.1 and 8.0
* Windows CE
* Windows RT Class Library and Runtime Components (winmd)
* .NET Standard / .NET Core / UWP
* Portable Class Library
* Unity3D (.Net 2.0 built without System.Drawing reference)
* Xamarin.Android (formerly Mono for Android)
* bindings to CoreCompat.System.Drawing, ImageSharp, SkiaSharp, OpenCVSharp, Magick, Kinect V1 and V2
* support COM interop, can be used with VBA

The library is available in the release section [release section](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046ee364a914201738c627d740169a3212be7d33324c01b5bbd27e0bedb71de7330)  and as [NuGet package](http://u.720life.cn/g/fc22af1986001aaffae545db699770d852893f8e1aff66920a31a8598f341833c1bb3ea1b371c6e839d68307af01805d  too.

[![N|NuGet](https://img.shields.io/nuget/v/Nuget.Core.svg)](https://www.nuget.org/packages/ZXing.Net/)

#### Additional platform support without pre-built binaries
The library can be built for Xamarin.iOS (formerly MonoTouch). The project file and solution are available in the source code repository.

A special version for the [.Net Micro Framework](http://u.720life.cn/g/43d8d3d99c8fd8af6c240816f866ce0caac366b8a08d3a38dd28cc0d8bae05cc)  can be found in a separate branch in the source code repository.

#### The following demo clients are available:

* decoder for the command line
* encoder for the command line
* Windows Forms demo (demonstrates decoding and encoding of static images and from a camera)
* Windows Phone demo (demonstrates decoding of static images and from a camera)
* Windows Service demo (demonstrates decoding of static images)
* Windows Presentation Framework demo (demonstrates decoding of static images)
* Windows CE demo (demonstrates decoding of static images)
* Windows RT demo (demonstrates decoding of static images)
* Windows Store App with HTML5/JS (demonstrates decoding of static images)
* Unity3D and Vuforia demo (demonstrates encoding of barcodes and decoding of images from a camera with [Unity3D](http://u.720life.cn/g/5014c628da22f89da8236145556ff4a170ee55224a349dad35290ea0cbe30c0c) 
* Silverlight demo (demonstrates decoding and encoding of static images)
* EmguCV demo (demonstrates decoding of images from a camera and uses the [EmguCV framework](http://u.720life.cn/g/003f1d6c8e6c81ef760c9ac95e9bab6041dca16442ab2e8f66900dab54d9ce73) 
* OpenCV demo (demonstrates decoding of images from a camera and uses the [OpenCVSharp framework](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cbb95843d59e6ecd398e4cdb9c63c81cabd2e6f66ed1f3b44ee11060a4691dd0) 
* AForge demo (demonstrates decoding of images from a camera and uses the [AForge framework](http://u.720life.cn/g/0e0c130d0424b24bb33e7bd9954f191cbcc126a9b92243e727a77b1a1241adcc) 

## Thanks
Many thanks to the team of the [zxing project](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bedc2941f2a7b389f9bf19f6bba663d9)  for their great work. ZXing.Net would not be possible without your work!
## Usage examples
The source code repository includes small examples for Windows Forms, Silverlight, Windows Phone and other project types.

#### small example decoding a barcode inside a bitmap (.Net 2.0/3.5/4.x)
```csharp
// create a barcode reader instance
IBarcodeReader reader = new BarcodeReader();
// load a bitmap
var barcodeBitmap = (Bitmap)Image.LoadFrom("C:\\sample-barcode-image.png");
// detect and decode the barcode inside the bitmap
var result = reader.Decode(barcodeBitmap);
// do something with the result
if (result != null)
{
   txtDecoderType.Text = result.BarcodeFormat.ToString();
   txtDecoderContent.Text = result.Text;
}
```
## Help wanted
All help is welcome!
## Feedback
You use the library?
We would be happy if you give us a short note on the use of the library.

You found a bug?
Please create a new issue here or start a discussion about it if you are not sure.

You use the library and you are not happy with it?
Write us an email please or start a discussion about your problems with it. We will try to help you.

And you can find me on [Twitter](http://u.720life.cn/g/872672d0e23e2eaceaf26c6fd3ebbc6d5d118b74e8118fdd88e41cb21628bc5c 
[![N|http://twitter.com/micjahn](https://img.shields.io/twitter/follow/espadrine.svg?style=social&label=Follow)](http://twitter.com/micjahn)
## Support it
If you find the project useful and you wish to support the future development feel free to support it with a donation.

## Donate

[![N|Donate](https://www.paypal.com/en_US/i/btn/btn_donateCC_LG_global.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=BYHN42UHPA86E)

Beside a donation patches, bug reports, feedback and other useful help are always welcome!
## Donation WITHOUT money
It would be really, really great if you could support one of my social projects. You can support it WITHOUT paying money.
You only have to go to the following url before you buy anything from a supported online shop (like Amazon or eBay):  
http://www.bildungsspender.de/kitadorfhain  
Select you prefered online shop and go shopping like everytime. The online shop will pay a provision to our Kindergarten for your purchase. No extra costs for you. There are 85 thankful kids.
(and one thankful developer of ZXing.Net ;) )


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)