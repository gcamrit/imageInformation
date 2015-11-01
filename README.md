#The ImageInformation PHP class
--------

*By Prakash Bhandari
(http://www.prakashbhandari.com.np/)*

*Licensed under the MIT license: http://opensource.org/licenses/MIT*

*Demo : http://demo.prakashbhandari.com.np/imageInformation/example*

Overview
--------
The ImageInformation PHP class is used to get image information generated by digital cameras.



### An example of it's use follows:

Images must be saved after you manipulate them. To save your changes to
the original file, simply call:

```php
$img = new ImageInformation();
$imageInfo = $img->getInformation("../assets/img/test.jpg");
if ($camera) {
    echo '<img src="../assets/img/test.jpg" alt="" height="250" /> <br />';
    echo "Maker: " . $imageInfo['maker'] . "<br />";
    echo "Camera Used: " . $imageInfo['model'] . "<br />";
    echo "Exposure Time: " . $imageInfo['exposure'] . "<br />";
    echo "Aperture: " . $imageInfo['aperture'] . "<br />";
    echo "ISO: " . $imageInfo['iso'] . "<br />";
    echo "FocalLength: " . $imageInfo['focalLength'] . "<br />";
    echo "Date Taken: " . $imageInfo['date'] . "<br />";
} else {
    echo '<span style="color: red;">Image not found</span>';

}
```

Will display the following, depending on the data:

-   Maker: NIKON CORPORATION
-   Camera Used: NIKON D5200
-   Exposure Time: 10/300
-   Aperture: f/4.5
-   ISO: 1400
-   FocalLength: 300/10
-   Date Taken: 2014:07:30 06:59:22

If the image has been re-sized and the information is no longer available then you should receive the following when echoing the same:

-   Maker: Info. Unavailable
-   Camera Used: Info. Unavailable
-   Exposure Time: Info. Unavailable
-   Aperture: Info. Unavailable
-   ISO: Info. Unavailable
-   FocalLength: Info. Unavailable
-   Date Taken: Info. Unavailable

Some digital cameras do not capture all the information, Not captured information will display "Info. Unavailable".

*Note:- The image should be a original and should not be edited or re-sized. If we edit or resize the image, all the image information will be lost. If you want the resize the image, first of all you need to save all the information to the database  *

