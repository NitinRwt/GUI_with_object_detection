# Image-Recoginition

1. Create a new virtual environment
python -m venv (Name of Env).

2. Activate your virtual environment
source tfod/bin/activate # Linux
.\tfod\Scripts\activate # Windows 

3. Install dependencies and add virtual environment to the Python Kernel
python -m pip install --upgrade pip
pip install ipykernel
python -m ipykernel install --user --name=(Name of Env)

4. OPEN Jupyter Notebook

5. Collect images using the Notebook 1. Image Collection.ipynb - ensure you change the kernel to the virtual environment as shown below
![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/c217ef1c-d52c-4d6c-837a-a9a122a431f5)

6. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFOD\Tensorflow\workspace\images\train
\TFOD\Tensorflow\workspace\images\test

7. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFOD\Tensorflow\workspace\images\train
\TFOD\Tensorflow\workspace\images\test

8. During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.
![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/fda39d2a-bb08-465f-bf2c-d3b63df9fd62)

9. Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics.
  ![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/356b3e4b-384b-4061-8da5-c954f521a12f)

10. You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g.
 cd Tensorlfow/workspace/models/my_ssd_mobnet/eval
and open Tensorboard with the following command
tensorboard --logdir=. 
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
