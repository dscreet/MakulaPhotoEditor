# Makula Photo Editor

#### How to use the MakImage Class
```
String src = "file path goes here";
MakImage image = new MakImage(src);

image.getBuffImg() // returns java.awt.image.BufferedImage
image.getDisplayImg() // returns javafx.scene.image.Image
image.getWidth() // returns int
image.getHeight() // returns int

// once changes made to BufferedImage object (called buffImg in this case) - TODO: perhaps implement a change listner to call this in editor class
image.updateImage(buffImg)
```

**NOTE: Editor class must then call ```renderImage()``` to display changes**


#### Applying filters to BufferedImage

```
Color[][] pix = new Color[width][height];

for (int i = 0; i < width; i++) {
    for (int j = 0; j < height; j++) {
        Color c = new Color(BuffImg.getRGB(i, j));
        
        /*Change colour here*/

    }
}
```