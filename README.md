# WiderFace-Evaluation
Python Evaluation Code for [Wider Face Dataset](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/)，borrowed from wondervictor，fix the pyx compile issue
add bbox_overlaps.py file，making it usable in windows

## Widerface evaluation steps：
for WIDER_val images，write txt that has the same name with image name，and put it in the same place with where the image is，the txt file content is like this：
````
F:\dataset\WIDER_val\WIDER_val\images\0--Parade/0_Parade_Parade_0_960.jpg
18
54 214 104 145 0.999644 
231 19 71 103 0.980476 
711 237 67 97 0.979931 
879 200 72 100 0.957633 
562 602 77 86 0.255938 
62 336 125 153 0.232769 
184 519 124 140 0.141956 
643 440 13 15 0.120774 
151 493 114 111 0.1006 
298 288 244 282 0.0483384 
37 251 218 259 0.0465985 
38 175 174 221 0.0438161 
792 256 228 249 0.0418914 
188 452 191 261 0.0354786 
579 350 197 246 0.032592 
602 408 131 134 0.0303818 
400 257 56 54 0.0248604 
210 564 69 88 0.0217526 

````
where the first line is where the image is,the second line is the number of faces in the image,the other is x,y,w,h,confidence

after get the result(the most direct use is use this file to generate txt https://github.com/deepinsight/insightface/blob/master/RetinaFace/test_widerface.py),use the code in this repo to evaluate the widerface.

## Usage


##### before evaluating ....

````
python3 setup.py build_ext --inplace
````

##### evaluating

**GroungTruth:** `wider_face_val.mat`, `wider_easy_val.mat`, `wider_medium_val.mat`,`wider_hard_val.mat`

````
python3 evaluation.py -p <your prediction dir> -g <groud truth dir>
````

## Bugs & Problems
please issue

## Acknowledgements

code borrowed from  wondervictor
