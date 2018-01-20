# Tensorflow-Mobile-Face-Detection
 After the release of Tensorflow Lite on Nov 14th, 2017 which made it easy to develop and deploy Tensorflow models in mobile and embedded devices.There are many pre-trained models available for training your own set of images .In this project we developed a model using ssd-mobilenet and proposed a hypothesis that this model can also be used for facial Recognition .We trained the model using tensorflow object detection api .Then the inferenced model is deployed to a android app using Tensorflow android .Now this module can embedded with any of your app as a feature for facial recognition.
![alt text](https://d33wubrfki0l68.cloudfront.net/363c0293012f654ed9db1deab5dc6e3ce61c7f54/46849/svrmedia/heroes/f/object-and-face-detection.png "Steve")
 
 ## Python Library Dependencies ##
 + [Tensorflow](https://www.tensorflow.org/)
 + [pandas](http://pandas.pydata.org/)
 + [Tensorflow_object_detection_api](https://github.com/tensorflow/models/tree/master/research/object_detection)
 
 ## Software Requirements ##
 1. Android Studio (SDK Version >=27 and NDK Version >=16)
 2. Labelimg(To annotate the image by boundary box)
 3. Sublime or Atom (Any Text editor according to your wish)
 
 ## Prefarable Hardware Requirements ##
 1. CPU (Intel i7,8GB RAM)or GPU (if you cannot prefer this configuration, try Google Cloud Platform of free $300 credits) to train           the model.
 ### If any of specification did'nt adapt you .Dont worry continue as much as you can .But there may be a delay in training the model and building the app. ###
 
 **Core Functionality**
+ `xml_to_csv.py` - This code is used to convert the collection of xml of the images to a single csv file.
+ `generate_tfrecord.py` - This code convert the csv to a tfrecord file. 
+ `android` - This folder contains all the built android files for this project
+ `data` - It contains the csv and tefrecord of my image files.
+ `training`- This folder contains the ssd-mobilenet pre-trained model.

**STEPS TO DEVELOP THE APP***
1. First,collect the images which you need to train.(As much as you collect you can get the better accuracy)
2. Next step ,label the particular coordinates of the image like the face which your model going to concentrate.This is also called as annotation of the image.It can be made easy using the software called labelimg.
3. Convert all the xml files generated by the software to a single csv file using the xml_to_csv.py code.After the conversion you get a csv file
4. Then convert the csv file to tensorflow easy readable form like tfrecords using generate_tfrecord.py code.Now you have the raw resource to proceed with the project.
5. Now you have to specify all the file path to the ssd-mobilenet.config file.
6. Move the data,training and ssd-mobilnet folders to the object_detection folder inside tensorflow_object_detection_api folder.
7. Run the program by giving your own set of parameters.
8. You will get the model file convert to a inference graph.
9. Next step is to build your tensorflow android app.
10. Export your model.pb and label.txt file to the assets folder in android module.
11. Since presetted all the neccessary change in the android file there is no need to change anything.
12. Now run your app,I guess you will be wondered that you implemented a face detection AI into your mobile.

### Note: The steps which given above are very generic and its suits for the people who are worked in this area ###

### For Beginners to develop this project ###
Visit the Link: https://www.skcript.com/svr/realtime-object-and-face-detection-in-android-using-tensorflow-object-detection-api/

**OUTPUT ( Visit the Link )**: https://vimeo.com/250737672

I hope you understand quite a lot from the tutorial to make your independent tensorflow app .If you need any help or issue kindly raise a issue in the repo and we will return you shorlty.Happy Coding !
