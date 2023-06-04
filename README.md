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
![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/63a9f9a6-16dc-4ebe-9ee8-91ab4394c460)


6. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFOD\Tensorflow\workspace\images\train
\TFOD\Tensorflow\workspace\images\test

7. Manually divide collected images into two folders train and test. So now all folders and annotations should be split between the following two folders.
\TFOD\Tensorflow\workspace\images\train
\TFOD\Tensorflow\workspace\images\test

8. During this process the Notebook will install Tensorflow Object Detection. You should ideally receive a notification indicating that the API has installed successfully at Step 8 with the last line stating OK.

![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/da8b741e-251b-455f-80c4-6e09c8c30b64)

9. Once you get to step 6. Train the model, inside of the notebook, you may choose to train the model from within the notebook. I have noticed however that training inside of a separate terminal on a Windows machine you're able to display live loss metrics.

![image](https://github.com/NitinRwt/Image-Recog/assets/110294741/7653f65a-7a95-4789-ab95-99301d3b0cc7)


10. You can optionally evaluate your model inside of Tensorboard. Once the model has been trained and you have run the evaluation command under Step 7. Navigate to the evaluation folder for your trained model e.g.
 cd Tensorlfow/workspace/models/my_ssd_mobnet/eval
and open Tensorboard with the following command
tensorboard --logdir=. 
Tensorboard will be accessible through your browser and you will be able to see metrics including mAP - mean Average Precision, and Recall.
