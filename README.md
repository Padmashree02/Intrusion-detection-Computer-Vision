# Application - Contour detection + Object detection
# Detection of the person's unappropriate actions
Libraries - cv2, numpy, movie.editor

Language - Python

Topics - Background subtractor, Erosion, contour (Human being / person detection), area of parameter, bounding box

Pipeline - 

    > Load the video (recoreded footage or live video).
  
    > Pre-processing :-
    
      : Store the video frame's dimensions- width and height, frames per second
      : Create an variable to store the output video
    
    > Define the background suntractor variable- help to identify moving objects from the static background.

    > Read the video :-

      : Apply the background subtractor in current frames of the video, in result it forms a foreground mask (the mask which highlights the foreground without background)

      : Apply erosion method on the mask to remove noises

      : Detect the contours from the input image as a foreground mask (input image)- results the list of each contour cardinally with (x,y) coordinate, width, hieght

      : Sort the detected contours (descending order), find the contour which has largest area and compute the largest contour's fraction area wrt the frame's size.

      : Draw the bounding box for the detected largest contour from its x,y,h,w values in each frames of the video.

    > Post-processing :-

      : Save the output video in defined variable 
