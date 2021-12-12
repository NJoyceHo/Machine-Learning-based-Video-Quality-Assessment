# Machine-Learning-based-Video-Quality-Assessment
This repository contains the report and source codes of my final-year project (Title: Machine Learning-based Video Quality Assessment) of the course EIE4433: Honours Project of the [Department of Electronic and Information Engineering (EIE)](https://www.eie.polyu.edu.hk/home/index.html), the [Hong Kong Polytechnic University (PolyU)](https://www.polyu.edu.hk/).
One of the crucial aims of this subject is "learning by doing", which I am required to employ the skills and knowledge gained from other previous courses, and apply them to develop solutions to resolve problems.

To know more about EIE4433, you may read its description on [P.24](https://www.eie.polyu.edu.hk/docs/Programmes/Programme_Booklets/4year/42470/42470-BEngEIE-1920-Aug2019.pdf#page=30) and its syllabus on [P.254-256](https://www.eie.polyu.edu.hk/docs/Programmes/Programme_Booklets/4year/42470/42470-BEngEIE-1920-Aug2019.pdf#page=260) from the [BEng(Hons) in Electronic and Information Engineering Programme Booklet (2019/20)](https://www.eie.polyu.edu.hk/docs/Programmes/Programme_Booklets/4year/42470/42470-BEngEIE-1920-Aug2019.pdf).

## Acknowledgments
I wish to thank my project supervisor [Dr. Yui-Lam Chan](http://www.eie.polyu.edu.hk/~ylchan/) and tutor [Mr. Ngai-Wing Kwong](https://www.researchgate.net/profile/Ngai-Wing-Kwong), Titan of the EIE Department for their valuable guidance and suggestions on the development of this research project.

## Project Introduction
In the past, when the internet had not been well developed yet, television was the sole source for broadcasting videos. Nonetheless, times have changed. Communication technology becomes more and more advanced. Today’s audience does not only rely on the traditional medium to enjoy videos. Instead, there is an increasing tendency of viewing them on online streaming platforms such as Netflix and YouTube. The rising demand for video streaming services leads to the competitive market of those websites. For this reason, service providers have come to an awareness of how viewers perceive videos, which is also known as Quality of Experience (QoE). In order to control and optimise the standard of their services, Video Quality Assessments (VQA) are conducted to study the influences of video distortion toward QoE.

The means of VQA can be primarily categorised in two: subjective and objective VQA. Subjective VQA is defined as a test which “involves human participants providing scores of perceived visual quality after watching test sequences in a controlled environment” [1]. It is the most reliable way to evaluate QoE as human beings are those who receive videos at the end [2]. The brief process of executing this assessment has been described by Arun Kumar and Chandramathi [3]. A group of specialists were requested to watch video clips. The judges determined the quality of the films according to their perception by scoring each of them a Mean Opinion Score (MOS).

The implementation of subjective VQA, however, is “general complex, expensive, and time consuming” [4]. The process of computing MOS requires human resources and a significant amount of time to train the audience and determine the quality of the videos. Hence, it is not practical for real-time video processing and applications.

Due to this rationale, objective VQA is conducted instead to resolve the disadvantage of subjective VQA. 

In this project, a machine learning-based no-reference objective VQA (NR-VQA) will be conducted to assess the quality of videos. Shahid et al. [5] explain that NR approach “does not require access to the original image/video” to judge the features and artifacts in the distorted videos. It is a pragmatic way to be implemented when resources are limited, thus is favourable in running a real-time objective VQA. To conduct that, a machine learning-based NR-VQA model will be established to measure MOS of each video in the aspect of human perception. Its structure follows that of a long short-term memory (LSTM) of recurrent neural network (RNN). Temporal features of the videos are going to be collected and applied into the model, together with the given spatial and temporal features [6].

Upon the completion of this project, the outcomes of the trained NR-VQA model will be compared with the MOS collected from a subjective VQA. Principal component analysis (PCA) will be applied in the model to improve the performance. The capability of the resourceless NR-VQA will also be juxtaposed with the achievements of existing full-reference VQA (FR-VQA), where the original videos are available in testing.

#### References

[1] 	F. M. Moss, C.-T. Yeh, F. Zhang, R. Baddeley and D. R. Bull, “Support for reduced presentation durations in subjective video quality assessment,” Signal Processing: Image Communications, vol. 48, pp. 38-49, Aug. 2016. 

[2] 	Z. Wang, H. R. Sheikh and A. C. Bovik, “Objective Video Quality Assessment,” in The Handbook of Video Databases: Design and Applications, B. Furht and O. Marqure, Eds., Boca Raton, CRC Press, 2003, pp. 1041-1078.

[3] 	P. M. Arun Kumar and S. Chandramathi, “Video Quality Assessment Methods: A Bird' s-Eye View,” International Journal of Computer and Information Engineering, vol. 8, no. 5, pp. 772-778, Apr. 2014. 

[4] 	B. Ortiz-Jaramillo, J. Niño-Castañeda, L. Platiša and W. Philips, "Content-aware objective video quality assessment," Journal of Electronic Imaging, vol. 25, no. 1, pp. 1-16, Feb. 2016. 

[5] 	M. Shahid, A. Rossholm, B. Lövström and H.-J. Zepernick, "No-reference image and video quality assessment: a classification and review of recent approaches," EURASIP Journal on Image and Video Processing, vol. 2014, no. 1, pp. 1-32, Aug. 2014. 

[6] 	N. W. Kwong, "Video Quality Assessment based on Machine Learning," B.Eng thesis, Department of Electronic and Information Engineering, The Hong Kong Polytechnic University, Hong Kong, 2019.

## Project Objectives
1.	Construct a machine learning LSTM model for NR-VQA to reflect the QoE perceived by human when viewing videos

2.	Extract and evaluate the temporal features of videos to detect the temporal artifacts in them

3.	Apply the extracted temporal and the provided spatial and temporal features to train the model and simulate the execution of a subjective video quality assessment to predict the MOS of each video

4.	Test the model and compare the MOS obtained from it to those from the subjective VQA to observe the accuracy

5.	Perform PCA feature selection to enhance the model performance

6.	Compare the performance of the proposed NR-VQA with those of FR-VQA

## Brief Information of the Project Development Environment
Below are some tools I used to build the program for this project:

#### Required Hardware
| Name  | Requirements |
| ------------- | ------------- |
| PC | MS Window 10, with a Minimum of 256GB Storage and 12GB RAM |

#### Required Software
| Name  | Function(s) |
| ------------- | ------------- |
| Python | Programming Language |
| Anaconda Navigator | Distribution of Python Programming, Package and Environment Manager |

#### Libraries
| Name  | Function(s) |
| ------------- | ------------- |
| Keras | Machine Learning Library |
| OpenCV | Programming Language |
| Matplotlib | Provides Plotting Tools |
| Numpy | Constructs and Manipulates Arrays and Matrices |
| scikit-learn | Provides Algorithms for Data Processing and PCA Feature Selection |
| SciPy | Offers Formulas for Scientific Computing|
| Pandas | Manipulates and Analyses Data from Excel Files using DataFrame object |
| Openpyxl | Manipulates Excel Files |

## Other Details of the Research and Development of the Project
Others details of how I carried out research on this project and the development of the software program can be referred to the project report on [Github](https://github.com/NJoyceHo/Machine-Learning-based-Video-Quality-Assessment/blob/master/Machine-Learning-based-Video%20Quality-Assessment_Report_NJoyceHo.pdf) / [Google Drive](https://drive.google.com/file/d/1rEQtmSKbfx9cAtAdCwc_DFayULRhNQfg/view?usp=sharing).

## Results
The best trained model is of 6 PCs with 20 hidden nodes at 4857th epoch. The testing set loss (mean squared error) and its Pearson correlation coefficient are 1.6124 and 0.8479, respectively. 

## Source Codes
The entire application consists of many Python files. You are welcome to take a look at them by downloading the zipped program from [here](https://github.com/NJoyceHo/Machine-Learning-based-Video-Quality-Assessment/blob/master/Machine-Learning-based-Video%20Quality-Assessment_SourceCodes_NJoyceHo.zip). (Note: Only the codes written by me are contained in the ZIP folder. Program files offered by my supervisor and tutor to convert videos into frames and extract the given spatial and temporal artifacts, are not included in it.)

You can also try and run the files. Before you do so, please read "File Directory.txt" in the zipped folder to understand the usage of each program. Moreover, you are reminded to download the source video dataset first from [here](https://drive.google.com/file/d/1z41hdqR-bqNLcUWllPePzkfQW-I_A9ny/view?usp=sharing), which is provided by the [MCL-V Database project](http://mcl.usc.edu/mcl-v-database/) of [USC Media Communications Lab](http://mcl.usc.edu/). You are also recommended to read their [journal](http://mcl.usc.edu/wp-content/uploads/2015/03/MCL-V-A-streaming-video-quality-assessment-database.pdf) to learn more about how they created the dataset.
