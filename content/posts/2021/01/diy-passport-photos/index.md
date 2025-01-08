---
categories:
- Guides
- Tech
coverImage: Dummy.jpeg
date: "2021-01-25"
tags:
- gimp
- passport-photos
title: DIY Passport Photos
---

Here's a quick and simple way to make and print your own passport photos\[PP\]. I've used [GIMP](https://www.gimp.org/) - which is a fabulous photo editing tool. They have a nifty [installer](https://www.gimp.org/downloads/) irrespective of which OS you use and have stood the test of time. There are a slew of different ways to arrive at the final product. This method has worked well for me over the past and based on your specific needs, you might have to alter a few settings.

Now let's say you have the below image that you'd like to make PP's out of and you'd like them to be 2''x2'' with other constraints laid out [here](https://travel.state.gov/content/travel/en/passports/how-apply/photos.html). This one's obviously a bad image to start out with, but should be a good test subject!

![](images/Dummy-1-150x150.jpeg)

**Isolate and sanitize**:

Ideally, you'd want to get a good photo of the subject. Make sure s/he is standing against a light background and there's sufficient uniform lighting on the face. If you're not able to get that you'll have to 'sanitize' the image first. And here's how we go about doing that:

1. Open the image in GIMP and scale the image such that the distance between the top of the head and the bottom of the chin is about 1.1875 inch \[Midway between 1 inch and 1.375 inch - The specs that was mentioned in the Travel web portal\].
    - To measure: Press 'Shift+M' - This is the shortcut for the measure tool. Use the mouse pointer to measure distance. The measurements should be visible at the bottom.
    - To scale: Navigate to '_Image_' on the top navigation bar and then select '_Scale Image_'. Change the _Image size_ attribute to % and scale down to the requisite level. For instance, I had to scale down to 60% since my initial Head-chin length was about 50mm.
    - Finally measure the resulting image's head to chin length in pixels. In our test case this was 366 pixels after the scaling. So our DPI \[Dots (Pixels) per inch\] is 366/1.1875 ~=308. We'll use this later to crop our image.

- ![](images/Before-scaling-1200x652.png)
- ![](images/scale-image-1200x656.png)

2\. If your image does not have a uniform light background or has shadows \[Like in our case\] here's how you digitally make the background white. Do note that certain agencies/services do not accept digitally altered images - So make sure you have some great lighting!

- Select the Paths tool - Shortcut 'B'.
- Use your mouse and make a path around the subject. Make sure you close out the loop at the end by pressing Ctrl.
- Convert the path to a selection by pressing on the '_Selection from path_' on the **Path** sidebar

![](images/Selection-from-path-600x326.png)

- Press Ctrl+I to invert the selection and press Delete on your keyboard to erase the background.

Now that we've cleared the background, export the image as a jpeg and save for further processing.

**Create the 2''x2'' image**:

Since we have a 308 DPI image , The 2" x 2" image would be about \[308x2, 308x2\] pixels = 617x617 pixels. \[Your values would obviously be different based on where you started!\]

To crop out our 2"x2" image, click on the '_Rectangular Select tool_' - \[Shortcut R\]. Then on the '**Rectangular Select**' sidebar, check the _Fixed_ checkbox and set the parameter to '_size_'. Also further below switch the '_No guides_' drop-down to '_Center Lines_'. Now click on the image and you should see a square box with central guide lines.

![](images/2x2-grab-600x326.png)

Move the box and center it so as to fit the image well within the box. Finally, Right-click on the Image, select '_Image_' and then '_Crop to Selection_'.

**Build the 4"x6" canvas:**

Lets create a new image canvas to hold our 6 PP photos. Use the shortcut Ctrl+N to create a new image. Set the image size as 4"x6". Open the advanced options and set the X and Y resolution to 308 pixels/in. While here you might also want to set the _Fill_ option to _White_. Now that we have the base canvas ready, navigate to Image>Guides>New Guide(By Percent) and create two horizontal (33.33%,66.66%) and one vertical(50.00%) guide.

- ![](images/Canvas-1200x675.png)
- ![](images/Guides-1200x675.png)

Now switch back to the previous GIMP window that has the 2"x2" image. Select all with Ctrl+A, Copy with Ctrl+C, switch over to the 4"x6" canvas and paste it over six times with Ctrl+V. Move the pasted images to the individual boxes. The guides will help snap the the images correctly.

![](images/Final-4x6-1-1200x652.png)

That's it! You now have a stellar looking 4"x6" canvas that you can export to a jpeg/jpg format and print out on a matte photo card either at home or any of the external printing centers.
