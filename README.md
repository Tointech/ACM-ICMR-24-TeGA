## ACM ICMR 2024 - The 14th International Conference on Multimedia Retrieval 
---
### Description 
This code represents a Text-Guided Generative-based Approach developed for the [ACM ICMR 2024 Grand Challenge on Detecting Cheapfakes](https://detecting-cheapfakes.github.io/icmr-2024.html). It is showcased in both Task 1 and Task 2.

Our Paper: [Link](https://doi.org/10.1145/3652583.3657602)

### Overall Pipeline

**Task 1:** Detect miscontextualization in (Image, Caption1, Caption2) triplets. If captions describe the same objects but different events, it's out-of-context (OOC). If they describe the same event regardless of objects, it's not-out-of-context (NOOC).

<img src="assets/task1.png">


**Task 2:** Determine whether a given (Image,Caption) pair is genuine (real) or falsely generated (fake).

<img src="assets/task2.png">

### Generated Dataset

In this work, we create a new dataset tailored to our specific requirements, leveraging the [COSMOS](https://github.com/shivangi-aneja/COSMOS) dataset as a foundation.

You can find our training dataset in folder [generated_dataset](generated_dataset). 
 - The [sd_dataset.txt](generated_dataset/sd_dataset.txt) file contains links to images stored on Google Drive, along with their corresponding annotations in the [sd_pairs.json](generated_dataset/sd_pairs.json) file. The annotation file includes captions and the relative path to each image.

### Evaluation Guide

-  To begin, please access the [icmr2024_challenge.ipynb](icmr2024_challenge.ipynb). If needed, adjust the input folder path within the notebook to suit your setup.
  
**Note:** The input folder path should have the following structure:

    INPUT_FOLDER
    ├── test.json
    ├── public_test_mmsys
    │ ├── 0.jpg
    │ ├── 1.png
    │ ├── 2.jpg
    │ ├── ...jpg

- Next, execute the first section `I. Init & Setup` of the notebook to initialize the environment and define essential functions.

- In the last section `II. Execute`, proceed to execute the cells relevant to the task you wish to explore.

### Experimental Results

#### Dataset
We utilize the `public_test_set`, consisting of 1000 samples, provided by the challenge organizer for Task 1.

##### Effectiveness
(1) Accuracy: *79.4%*

(2) Average Precision: *75.4%*

(3) F1-Score: *72.4%*

For Task 2, we achieved an accuracy of 56.4% in the public test. 

##### Efficiency
(1) Number of Trainable Parameters: *278811651*

(2) Inference Time (s): *5311.27* (calculated for 1000 test samples in public test set)

(3) Model Size (MBs): *1063.58*


**Note:** This experiment run on Google Colab Pro with A100 GPU.

---
**Contact Us**

If you have questions regarding the dataset or code, please email us at lathu21@clc.fitus.edu.vn.

### Citation
If you utilize the code in your research or reference our paper, kindly include the following citation:

```
@inproceedings{le2024tega,
  author = {Le, Anh-Thu and Nguyen, Minh-Dat and Dao, Minh-Son and Tran, Anh-Duy and Dang-Nguyen, Duc-Tien},
  title = {TeGA: A Text-Guided Generative-based Approach in Cheapfake Detection},
  year = {2024},
  isbn = {9798400706196},
  publisher = {Association for Computing Machinery},
  address = {New York, NY, USA},
  url = {https://doi.org/10.1145/3652583.3657602},
  doi = {10.1145/3652583.3657602},
  booktitle = {Proceedings of the 2024 International Conference on Multimedia Retrieval},
  pages = {1294–1299},
  numpages = {6},
  series = {ICMR '24}
}
```
