# CSE587-Project
The proposed work presents a Novel Framework for Automatic Speech Recognition (ASR), using the normal and the locally-time reversed audio sequence as two of its efficient cues. The cues are first well trained on a baseline model and then combined with effective fine-tuning. Furthermore, with the cohort of experiments conducted, the work also describes a variety of reverse sequences which are not fit for ASR systems. The presented architecture has achieved a remarkable metric score outperforming other methods and has therefore provided a path to the researchers to further explore the idea of employing the locally-time reversed sequences in a more sophisticated manner.
![image](https://user-images.githubusercontent.com/47940851/236496758-a5c38ba2-de56-4489-9898-56e0db977d15.png)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1S7BleRcCpj6xDeVbFDdoeUvnSIcNNJxR?usp=sharing]
Consider opening the .ipynb notebook on Goole Colab https://colab.research.google.com/ for best code-interface. Code is well structured in Sections and in cells under the corresponding sections. To Properly understand the organization of code in the .ipynb notebook, see the snippet below! 

![image](https://user-images.githubusercontent.com/47940851/236500252-4c5cabea-d811-4cf2-b797-652e292bea84.png)

Over all the experiments conducted we have tried our best to preverse the outputs of almost all cells that we could!!! 

**Important Notes:** 
* During Training or Inference of different models, care must be take while specifying the name(**x**)  of the ```data_processing_x``` functions when loading the Train and Test loaders (under the Section Train-Test Functions). 
  * Differet ```data_processing_x``` functions and their functionality is listed below: 
  ```
      data_processing_normal (to handle undististurbed audio)
      data_processing_LTR (to handle locally-time reversed audio)
      data_processing_probabilistic25 ( to handle probabilistic-25 Reverse set)
      data_processing_50p (to handle Reverse set-50%)
  ```
* During Inference consider commenting out the Train function under epochs loop. Also to view the results specified, you have to load the best-checkpoints for each model. 
  * For infering the Model trained with Undisturbed Audio sequence.
  
    ```Best-Checkpoint```: ./weights/point_files/check_point_files/my_checkpoint_epoch_10_.pth.tar
    Output (expected) and shown in the .ipynb Notebook (Inference cell output).
    
    ![image](https://user-images.githubusercontent.com/47940851/236508244-dd4eb13c-d9ff-4ff8-a007-04a179cc58d8.png)

  * For infering the Model trained with Locally Time Reversed Audio sequence.
  
    ```Best-Checkpoint```: ./weights/point_files/check_point_files/my_checkpoint_epoch_10_.pth.tar
    Output (expected) and shown in the .ipynb Notebook(Inference cell output).
    
    ![image](https://user-images.githubusercontent.com/47940851/236508445-8e762186-3bae-40e7-ad68-a2b98c337e71.png)

    
  * For infering the Ensemble Model trained with combination of Undisturbed and Locally Time Reversed Audio Sequence.
  
    ```Best-Checkpoint```: ./weights/point_files/check_point_files/my_checkpoint_epoch_10_.pth.tar
    Output (expected) and shown in the .ipynb Notebook(Inference cell output).
    
    ![image](https://user-images.githubusercontent.com/47940851/236508599-54e20d32-aa57-40ae-b07a-2e5097a55845.png)


