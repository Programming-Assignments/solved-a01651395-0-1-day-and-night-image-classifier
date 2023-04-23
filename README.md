Download Link: https://assignmentchef.com/product/solved-a01651395-0-1-day-and-night-image-classifier
<br>
The day/night image dataset consists of 200 RGB color images in two categories: day and night. There are equal numbers of each example: 100 day images and 100 night images.

We’d like to build a classifier that can accurately label these images as day or night, and that relies on finding distinguishing features between the two types of images!

<em>Note: All images come from the</em><em> AMOS dataset</em><em> (Archive of Many Outdoor Scenes). </em><strong>0.1.1 Import resources</strong>

Before you get started on the project code, import the libraries and resources that you’ll need.

<table>

 <tbody>

  <tr>

   <td width="625"><strong>import</strong><strong> cv2</strong><em> # computer vision library </em><strong>import</strong><strong> helpers</strong><strong>import</strong><strong> numpy</strong><strong> as</strong><strong> np</strong><strong>import</strong><strong> matplotlib.pyplot</strong><strong> as</strong><strong> plt</strong>%<strong>matplotlib</strong> inline</td>

  </tr>

 </tbody>

</table>

<strong>0.2 Training and Testing Data</strong>

The 200 day/night images are separated into training and testing datasets.

<ul>

 <li>60% of these images are training images, for you to use as you create a classifier.</li>

 <li>40% are test images, which will be used to test the accuracy of your classifier.</li>

</ul>

First, we set some variables to keep track of some where our images are stored:

image_dir_training: the directory where our training image data is stored image_dir_test: the directory where our test image data is stored

[2]: <em># Image data directories</em>

image_dir_training = “day_night_images/training/” image_dir_test = “day_night_images/test/”

<strong>0.3 Load the datasets</strong>

These first few lines of code will load the training day/night images and store all of them in a variable, IMAGE_LIST. This list contains the images and their associated label (“day” or “night”).