<h1 align="center">AVESA (Audio-Visual Event Sentiment Analysis)</h1>

# Contributors
- <a href="https://github.com/berayboztepe" target="_blank">Beray Boztepe</a>
- <a href="https://scholar.google.com.tr/citations?user=NEhs3ttTIzkC&hl=tr" target="_blank">Prof. Dr. Bahadır Karasulu</a>
- <a href="https://github.com/bedirhankrkya/AVESA" target="_blank">Bedirhan Karakaya</a>
- <a href="https://github.com/ismetnl/AVESA" target="_blank">İsmet Ünlü</a>

# License
- The **MIT License** is used for infrastructure part of AVESA

# Backends (Used Frameworks and Tools)

<table>
  <tr>
    <th>Framework & Tool</th>
    <th>Used For</th>
  </tr>
  <tr>
    <td>Keras</td>
    <td>Deep Learning API</td>
  </tr>
  <tr>
    <td>Tensorflow-io & Opencv-Python</td>
    <td>Getting spectrograms and Data Augmentation techniques such as Multiple Masking, CLAHE etc.</td>
  </tr>
  <tr>
    <td>h5py</td>
    <td>To Save trained deep learning model</td>
  </tr>
  <tr>
    <td>Numpy & Pandas & Matplotlib </td>
    <td>General Purpose</td>
  </tr>
  <tr>
    <td>Moviepy & Pydub</td>
    <td>Applying some operations into frames and videos</td>
  </tr>
  <tr>
    <td>NLTK & Zeyrek & Jellyfish</td>
    <td>To find Similarity Score</td>
  </tr>
  <tr>
    <td>NLTK & Spacy</td>
    <td>Applying NLP techniques</td>
  </tr>
  <tr>
    <td>Vosk</td>
    <td>Get the speech to text translation from the video</td>
  </tr>
  <tr>
    <td>BERT</td>
    <td>Pre-trained models for Sentiment Analysis</td>
  </tr>
  <tr>
    <td>Transformers</td>
    <td>To Apply BERT models into the text for Sentiment Analysis</td>
  </tr>
  <tr>
    <td>Librosa</td>
    <td>Applying Gaussian Noise and some data augmentation techniques</td>
  </tr>
  <tr>
    <td>Gradio</td>
    <td>To build GUI structure. "Apache License 2.0"</td> 
  </tr>
  <tr>
    <td>Librosa</td>
    <td>Used in backend for BERT, Vosk models</td>
  </tr>
</table>

- Link for Gradio Reference:

(Abid, Abubakar and Abdalla, Ali and Abid, Ali and Khan, Dawood and Alfozan, Abdulrahman and Zou, James, (2019), "Gradio: Hassle-Free Sharing and Testing of ML Models in the Wild", ICML HILL 2019, arXiv preprint arXiv:1906.02569.): 

[![arXiv](https://img.shields.io/badge/arXiv-1906.02569-b31b1b.svg)](https://arxiv.org/abs/1906.02569)

# Metholodological Flow Diagram of our AVESA system

# How to use the AVESA:

- In order to use this GIU, first, you need to download this repo using this link.

<p align="center">
<a href="https://drive.google.com/drive/folders/1lvji1kKgQv_u-3GwBAYEgt-KuX0ei6yX?usp=sharing" target="_blank">Download</a>
</p>
 
- You need to run requierements.py file. After running the .py file, we recommend you to restart the kernel. Otherwise, you might get some errors about gradio. If there is an error about installing any library, You can use requirements.txt to install all libraries individually.

<p align="center">
<img src="img/reqirementsfile.png" width="600" height="50">
</p>

- Run this code section through your ide's console: 
```python
!python -m spacy download en
```

- Run project.py The output will give you a local IP adress. Copy that and paste it into the URL section of your browser. Do not forget to check your current folder inside the editor. **Current folder must be the folder where google drive link downloaded!**

<p align="center">
<img src="img/ip.png" width="600" height="100">
</p>

<p align="center">
<img src="img/paste.png" width="600" height="200">
</p>

- You can try the model incoming web page on your browser. Sometimes an error might occur by using not MP4 files. So, we suggest you to use .MP4 files as inputs.

<p align="center">
<img src="img/GIU.png" width="600" height="250">
</p>

- You can also start with the examples that was provided to you.

<p align="center">
<img src="img/samples.png" width="600" height="350">
</p>


# Known Issues and Fixing the Possible Errors

- 1) Make sure that your code runs in the same folder where your codes are. To ensure it, you can used this code.
```python
import os
print(os.getcwd())
```
If it is not the same folder, paste this line into the console or terminal of your ide.
```python
cd path\to\your\folder
```

- 2) If you encounter with an error while waiting the output of given video or exit while the model running, in order to run the model again, delete models/video_sum.h5 and delete Frames/name_of_the_video/. Otherwise you migth get these errors:
```diff
- models/video_sum.h5 is running by other process or unable to create a file, the file models/video_sum.h5 already exits:
```
You need to restart to kernel in order to delete this .h5 file. After restarting the kernel, you can delete the .h5 file and retry the model.

- 3) Keep in mind, Frames folder has to be empty. There will be folder in it only while the model is running. In order to run the model again or after the model gives an output, **check if the Frames folder is empty or not.**

- 4) In order to run the model, video_sum.h5 from the models folder should not exists in the folder. In order to run the model, delete this .h5 file first. This file will only be created while the model running and when the output is given, this .h5 file should be deleted. **Check if this file is deleted or not.**

# Some Notes:

- **Getting every frame and scoring by action rate for every frame process takes long and it gets longer if the video length gets longer! if there is a long text in the ner generated video for English, getting the speech by a vosk model takes long time. For Turkish, it takes short time but because of the proposed algorithm for Turkish NER, the process takes long time. So, please be patient to see the output while the model running.** 

- **You can also follow the process or you can see the reason of error through pycharm or spyder console if you are using one of them.**


# Enjoy the AVESA

**To learn more about the model, you can check the journal article about the AVESA here:**
