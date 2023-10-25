import cv2
img = cv2.imread(r'C:\Users\DINESH\Desktop\teluguu.jpg')
# coordinates of bounding boxes
# specify top-left and bottom-right corners (x1, y1, x2, y2) [(x1, y1, x2, y2), (x1, y1, x2, y2), ...]
"""x1=int(input())
y1=int(input())
x2=int(input())
y2=int(input())"""
bounding_boxes = [(0,0,479,319)]  # Add your bounding box coordinates

color = ( 0,225,0)                            # The color for the bounding boxes
thickness = 10                               # thickness of the bounding box lines
for (x1, y1, x2, y2) in bounding_boxes:
    cv2.rectangle(img, (x1, y1), (x2, y2), color, thickness)        # Draw the bounding boxes on the image

# Save the image with bounding boxes
cv2.imwrite('teluguu.jpg', img)

cv2.imshow('Image with Bounding Boxes', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
