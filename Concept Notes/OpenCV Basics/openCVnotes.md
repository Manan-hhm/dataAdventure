<h3>OpenCV</h3>
-> A library in python for image processing. <br>
-> It can be used for several operations such as:
<ul>
  <li>Reading/Writing images</li>
  <li>Detecting face and its features</li>
  <li>Detecting shapes like circle, rectangles, etc. (e.g., detecting coin in an image)</li>
  <li>Detecting text in images (e.g., reading number plates)</li>
  <li>Modifying image quality and colors (e.g., instagram filters)</li>
  <li>and more...</li>
</ul>
-> We can also use matplotlib for some image operations like showing image in jupyter notebook itself instead of a new <br>
&nbsp&nbsp&nbsp&nbsp window like openCV.

<h3>Image color spaces</h3>
-> A color space is a specific organization of colors that allows us to consistently represent and reproduce colors. <br>
<h4>RGB - Red, Green, Blue color space</h4>
-> Each channel can have a value in the range [0, 255] <br>
-> Possibility of 256^3 = 16,777,216 colors depending on how much Red, Green and Blue we place into each bucket. <br>
-> OpenCV uses BGR while Matplotlib uses RGB order. <br>
<h4>BGR - Blue, Green, Red color space</h4>
-> Just a reverse version of RGB. <br>
<h4>HSV - Hue, Saturation, Value color space</h4>
-> HSV transforms the RGB color space, remodelling it as a cylinder rather than a cube. <br>
-> Saturation(radius): How deep the color is? <br>
-> Hue(Angle): Which color it is (from orange to blue, etc.)? <br>
-> Value(Height): What's the brightness? <br>
<h4>Grayscale color space</h4>
-> A grayscale representation of an image throws away its color information. <br>
-> 2D: How black is the pixel? + How white is the pixel? (Brightness) <br><br>

->Converting to RGB is ideal for displaying any image. <br>

<h3>Image manipulation</h3>
<h4>Brightness</h4>
-> Change value of each and every pixel by any constant. <br>
-> Value comes from HSV. It represents brightness. <br>
-> Convert RGB to HSV. Modify brightness value. Convert it back to RGB. <br>


