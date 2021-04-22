# Fire Detection for real-time Streaming


The Project is Implemented in a Different Repo , where the actual training and process holds. The Complex MobileNet Architecture defines the entire model which is used to train a custom augmented dataset for "Fire & Smoke" Detection.

And in this repo, there's everything you need to test run your webcam or any suitable devices ( After Implementing ).

The application hasn't been deployed to any servers, considering the cost applicable,Size of SLUG (Therefore can't deploy to free services) and also since its an easy-go, anybody with some basic-flask experience can deploy it if needed.


## Run the Application in your own Device ?

### Step 1:
Install [Python 3.7](https://www.python.org/downloads/release/python-370/)  
Don't forget to add Path o Environment Varibales [Doubt?](https://www.educative.io/edpresso/how-to-add-python-to-path-variable-in-windows)

Completely Optional:
Install [Git](https://git-scm.com/downloads)

### Step 2:
Clone this Repository [Tutorial](https://www.youtube.com/watch?v=O72FWNeO-xY)

### Step 3:
From the root folder of the repository, open a commandline terminal/powershell and run the following commands:
`pip install virtualenv` :- Installs Virtualenv Python Module
`virtualenv ANY_NAME` :- Replace ANY_NAME with your choice of environment name
`.\ANY_NAME\Scripts\activate` :- Activates the Virtual Environment we just created
`pip install -r requirements.txt` :- Installs the Required Liraries , Takes time & Needs Space ("A lot")

### Step 4:
Once all the Above is Completed , Lets run our Application. There are Certain parameters to consider.


'--weights'     => 'model.pt path(s)'
'--source'      =>'# file/folder, 0 for webcam
'--img'         =>'inference size (pixels)'
'--conf'        =>'object confidence threshold'
'--iou'         =>'IOU threshold for NMS'
'--device'      =>'cuda device, i.e. 0 or 0,1,2,3 or cpu'
'--view-img'    =>'display results'
'--save-txt'    =>'save results to *.txt'
'--save-conf'   =>'save confidences in --save-txt labels'
'--save-crop'   =>'save cropped prediction boxes'
'--nosave',     =>'do not save images/videos'
'--classes'     =>'filter by class: --class 0, or --class 0 2 3'
'--agnostic-nms'=>'class-agnostic NMS'
'--augment'     =>'augmented inference'
'--update'      =>'update all models'
'--project'     =>'save results to project/name'
'--name'        =>'save results to project/name')
'--exist-ok'    =>'existing project/name ok, do not increment'

To Generally run the Application with a confidence of 30% via WebCam use this command from the root of the Repository
`python detect.py --weights best.pt --img 412 --conf 0.3 --source 0`

