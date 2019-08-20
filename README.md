# WiderFace-Evaluation
Python Evaluation Code for [Wider Face Dataset](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/)，borrowed from wondervictor，fix the pyx compile issue
add bbox_overlaps.py file，making it usable in windows

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
