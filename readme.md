# Project Name

 Add short description of project here > 
 This is a system that will take mulitple photos during a bicycle journey, then using detectnet and segnet it will highlight people and highlight the bike route. The segnet and detectnet are then merged and every merged photo is chained together to make a video that can then be output. With high computation power the program can be run to almost output live video. This will help make biking safe, by highlighting obstacles in the path avoiding accidents. 



## The Algorithm

Add an explanation of the algorithm and how it works. Make sure to include details about how the code works, what it depends on, and any other relevant info. Add images or other descriptions for your project here. 
The algorithm first works by using a python program to take a burst of 50 images, it will then run it throught pretrained models detect net and seg net which will highlight obstacles and paths. The will merge the two photos together for each of the 50 images, the images will then be chained and outputed as one video

## Running this project

1. Add steps for running this project.
2. Make sure to include any required libraries that need to be installed for your project to run.
need to download open cv, pillow and os for python
first run the photo-detection file in python in an image folder in jetson-inference - this will take multiple photos
Run docker in jetson-inference
Then into aarch64/bin run
./segnet --network=fcn-resnet18-cityscapes-1024x512 "images/frame_*.jpg" images/test/frames_%i.jpg


./detectnet "images/frame_*.jpg" images/test/framed_%i.jpg

this will run the networks and save in a test folder
then run the merge python file where all the images run through the network are stored to merge images
finally run the videos file in python on the folder that contains all the merged images to chain together in a video




[View a video explanation here] https://drive.google.com/file/d/1akV7aNW-WXkzVlx5DordOXRelnaZ9OLv/view?usp=sharing

Example output
https://drive.google.com/file/d/1k71YothH72JnaS9Xjy-mSRzKWFdD68i3/view?usp=sharing
please note that the program was intended for outside use and some images weren't processed by detectnet
