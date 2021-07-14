# Fire Detection for real-time Streaming

## DataSet Used

I've used a Custom Built Dataset with anotations, here the model will be able to recognize household as well as forest fire scenarios.
The project has its limitations when it comes to Accuracy, due to lack of computational resources. This was a project build to learn and understand the Working of Object-Detection Models.

<img src="https://github.com/reekithak/Fire-Detection-NET-Stream-API/blob/master/images/fire.png">

## Architecture Used
The Project is Implemented in a Different Repo , where the actual training and process holds. The Complex Yolo Architecture defines the entire model which is used to train a custom augmented dataset for "Fire & Smoke" Detection.

<img src="https://github.com/reekithak/Fire-Detection-NET-Stream-API/blob/master/images/yolo.png">

### Yolo WorkFlow

<img src="https://github.com/reekithak/Fire-Detection-NET-Stream-API/blob/master/images/yolowork.png">

## This Repo?

In this repo, there's everything you need to test run your webcam or any suitable devices ( After Implementing ).

The application hasn't been deployed to any servers, considering the cost applicable,Size of SLUG (Therefore can't deploy to free services) and also since its an easy-go, anybody with some basic-flask experience can deploy it if needed.

## Flash-Demo?
https://user-images.githubusercontent.com/42499275/125557012-23727ccc-c2a2-43d8-9bf5-88807591d15f.mp4


## Run the Application in your own Device ?

### Step 1:
Install [Python 3.7](https://www.python.org/downloads/release/python-370/)  
Don't forget to add Path o Environment Varibales [Doubt?](https://www.educative.io/edpresso/how-to-add-python-to-path-variable-in-windows)

Completely Optional:
Install [Git](https://git-scm.com/downloads)

### Step 2:
Clone this Repository [Tutorial](https://www.youtube.com/watch?v=O72FWNeO-xY)

### Step 3:
From the root folder of the repository, open a commandline terminal/powershell and run the following commands:<br />


`pip install virtualenv` :- Installs Virtualenv Python Module<br />
`virtualenv ANY_NAME` :- Replace ANY_NAME with your choice of environment name<br />
`.\ANY_NAME\Scripts\activate` :- Activates the Virtual Environment we just created<br />
`pip install -r requirements.txt` :- Installs the Required Liraries , Takes time & Needs Space ("A lot")<br />

### Step 4:
Once all the Above is Completed , Lets run our Application. There are Certain parameters to consider.


'--weights'     => 'model.pt path(s)'<br />
'--source'      =>'# file/folder, 0 for webcam<br />
'--img'         =>'inference size (pixels)'<br />
'--conf'        =>'object confidence threshold'<br />
'--iou'         =>'IOU threshold for NMS'<br />
'--device'      =>'cuda device, i.e. 0 or 0,1,2,3 or cpu'<br />
'--view-img'    =>'display results'<br />
'--save-txt'    =>'save results to *.txt'<br />
'--save-conf'   =>'save confidences in --save-txt labels'<br />
'--save-crop'   =>'save cropped prediction boxes'<br />
'--nosave',     =>'do not save images/videos'<br />
'--classes'     =>'filter by class: --class 0, or --class 0 2 3'<br />
'--agnostic-nms'=>'class-agnostic NMS'<br />
'--augment'     =>'augmented inference'<br />
'--update'      =>'update all models'<br />
'--project'     =>'save results to project/name'<br />
'--name'        =>'save results to project/name')<br />
'--exist-ok'    =>'existing project/name ok, do not increment'<br />

To Generally run the Application with a confidence of 30% via WebCam use this command from the root of the Repository<br />
`python detect.py --weights best.pt --img 412 --conf 0.3 --source 0`

