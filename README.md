# Yolo_v4-population-density-of-area
This is an object detection project I did primarily seeking to improve social distancing during the COVID-19 pandemic. I used a pre-trained Yolo_v4 model for object detection. I programmed so that the program leaves a red mark at the place each person was in each frame. The intensity of the red mark whitens if there are overlaps, meaning either the area is densely populated with people or many people have walked passed that area.

# Snippet of code that I've added to the Yolo source code:
cv::Mat img(1352, 1013, CV_8UC3, cv::Scalar(0, 0, 0)); cv::imshow("result", img);

# How to test this program:
change directory to darknet-master\darknet-master\build\darknet\x64 and open command prompt and run: darknet_no_gpu detector demo data/coco.data yolov3-tiny.cfg yolov3-tiny.weights -i 0 -thresh 0.25 -ext_output test1.mp4

Do not close the program immediately as there will be fewer data points(red marks) you will be able to observe. Press esc key.

Sample outputs:
![image](https://github.com/rho13030/Yolo_v4-population-density-of-area/assets/64012444/9536e246-da46-46a5-ab9b-0d05a92c5b5d)
![image](https://github.com/rho13030/Yolo_v4-population-density-of-area/assets/64012444/f7eb6d88-7624-42fd-a071-e6d528d9a947)

