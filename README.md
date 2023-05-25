#Novel Automatic Speech Recognition System

The proposed work presents a Novel Framework for Automatic Speech Recognition (ASR), using the normal and the locally-time reversed audio sequence as two of its efficient cues. The cues are first well trained on a baseline model and then combined with effective fine-tuning. Furthermore, with the cohort of experiments conducted, the work also describes a variety of reverse sequences which are not fit for ASR systems. The presented architecture has achieved a remarkable metric score outperforming other methods and has therefore provided a path to the researchers to further explore the idea of employing the locally-time reversed sequences in a more sophisticated manner.
![image](https://user-images.githubusercontent.com/47940851/236496758-a5c38ba2-de56-4489-9898-56e0db977d15.png)

Consider opening the .ipynb notebook on Goole Colab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sabih411/CSE587-Project/blob/main/CSE587_Project.ipynb) for best code-interface. Code is well structured in Sections and in cells under the corresponding sections. To Properly understand the organization of code in the .ipynb notebook, see the snippet below! 

![image](https://user-images.githubusercontent.com/47940851/236500252-4c5cabea-d811-4cf2-b797-652e292bea84.png)

Over all the experiments conducted we have tried our best to preverse the outputs of almost all cells that we could!!! 

**Important Notes:** 
* The data pre-exists in the PyTorch Library **torchaudio** and is directly loaded. 
* During Training or Inference of different models, care must be take while specifying the name(**x**)  of the ```data_processing_x``` functions when loading the Train and Test loaders (under the Section Train-Test Functions). 
  * Differet ```data_processing_x``` functions and their functionality is listed below: 
  ```
      data_processing_normal (to handle undististurbed audio)
      data_processing_LTR (to handle locally-time reversed audio)
      data_processing_probabilistic25 ( to handle probabilistic-25 Reverse set)
      data_processing_50p (to handle Reverse set-50%)
  ```
* During Inference consider commenting out the Train function under epochs loop. Also to view the results specified, you have to load the best-checkpoints for each model.
  * The model checkpoint files can be found in the [weights folder](https://drive.google.com/drive/folders/10rjqI-G1iAzkn13xCWFoqsMeHtRLcJSG?usp=sharing). The organization of the weights follder is shown below. 
  ```
    |weights
      |->point_files
         |->check_point_files
           |...ckpt files
         |->reverse20
           |...ckpt files
         |->combined
           |...ckpt files
  ```
  * For infering the Model trained with Undisturbed Audio sequence use the checkpoints under **check_point_files**.
    * ```Best-Checkpoint```: [./weights/point_files/check_point_files/my_checkpoint_epoch_10_.pth.tar](https://drive.google.com/file/d/1nG5nQMShEEzNlfEVf05VX3ytAVMx2aGo/view?usp=share_link)
    * Output (expected) and shown in the .ipynb Notebook (Inference cell output).  
       ![image](https://user-images.githubusercontent.com/47940851/236508244-dd4eb13c-d9ff-4ff8-a007-04a179cc58d8.png)
  * For infering the Model trained with Locally Time Reversed Audio sequence use the checkpoints under **reverse20**
    * ```Best-Checkpoint```: [./weights/point_files/reverse_20/my_checkpoint_epoch_11_.pth.tar](https://drive.google.com/file/d/108ehKDuU5T7g1dyESjcU-2NWvf-HN5fk/view?usp=share_link)
    * Output (expected) and shown in the .ipynb Notebook(Inference cell output).
       ![image](https://user-images.githubusercontent.com/47940851/236508445-8e762186-3bae-40e7-ad68-a2b98c337e71.png)
  * For infering the Ensemble Model trained with combination of Undisturbed and Locally Time Reversed Audio Sequence use the checkpoints under **combined**
    * ```Best-Checkpoint```: [./weights/point_files/combined/my_checkpoint_epoch_4_.pth.tar](https://drive.google.com/file/d/1Zljv9E6URpokdKQ5yZs5IDDmWPsIArSF/view?usp=share_link)
    * Output (expected) and shown in the .ipynb Notebook(Inference cell output).  
        ![image](https://user-images.githubusercontent.com/47940851/236508599-54e20d32-aa57-40ae-b07a-2e5097a55845.png)
* The **training_stats folder** contains all the numpy files with the loss values recorded for each iteration for each model tested. 
* The **backup.txt** files contains the cell output of the recorded training statss of the Model trained with Undisturbed Speech Sequence, because the correspnding cell from the notebook got deleted. 

**THANK YOU!**

![Screenshot of a comment on a GitHub issue showing an image, added in the Markdown, of an Octocat smiling and raising a tentacle.](https://myoctocat.com/assets/images/base-octocat.svg)
