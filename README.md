# bounding-boxes
import cv2
import numpy as np
import pandas as pd
import tensorflow as tf
import matplotlib.pyplat as plt
from """file name""" import image
from d2l import mxnet as d2l
image=imread("image.jpg")
def bounding_box_corner_to center(boxes):
  x1,y1,x2,y2= boxes[:,0],boxes[:,1],boxes[:,2],boxes[:,3]
  cx=(x1+x2)/2
  cy=(y1+y2)/2
  wid=x2-x1
  heig=y2-y1
  boxes=np.stack((cx,cy,wid,heig),axis=1)
  return boxes
def bounding_box_center_to_corner(boxes):
  cx,cy,wid,heig=boxes[:,0],boxes[:,1],boxes[:,2],boxes[:,3]
  x1=cx-0.5 * wid
  y1=cy-0.5 * heig
  x2=cx+0.5 * wid
  y2=cy+0.5 * heig
  boxes=np.stack((x1,y1,x2,y2),axis=1)
  return boxes
image_bounding_box=  []      # Enter the coordinates as a list of elements

# to check whether the image is accurate or not by converting image to matplotlib.pyplot format
def box_to_rect(bbox,center):
  return(d2l.plt.Rectangle(xy=(bbox[0], bbox[1]), width=bbox[2]-bbox[0], height=bbox[3]-bbox[1],fill=False, edgecolor=color, linewidth=2)


figure=d2l.plt.imshoe(image)
figure.axis.add_patch(bbox_to_rect(image,'green')
