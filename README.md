# Object Detector dataset

## Dataset description

The dataset presents images of additively manufactured objects, which consists of images of 3 types of manufactured objects built by 3D printer. The objects are parts for elevator maintenance*. Objects are arranged in images at different positions and distances from the camera, each image contains 1 to 3 objects. Each image is 600 pixels high and 800 pixels wide. The objects are located in the center of the image, which has a gray background.

The dataset was annotated using the VGG Image Annotator (VIA) tool (https://www.robots.ox.ac.uk/~vgg/software/via/) which allows you to annotate different image information. The information noted was:

- Type: The class that the object belongs to, part 1, part 2 or part 3;
- Defect level: The defect level of the object:
     - 0 - Not visible defect: The object does not have any visible defects;
     - 1 - Few defects: The object has defects that can be easily removed, for example, a small protrusion that is removed when handled;
     - 2 - Some defects, but do not interfere with the operation: These are defects that do not interfere with the operation of the object, most of which are aesthetic defects that are easily removed;
     - 3 - Too many defects, the object can be discarded: The object has many defects that interfere with its operation, making it unusable. The object must then be discarded to create a new one.
- Color: The color of the object, being: light blue, dark blue, white, purple or orange;
- Defect? (Defective?): Information on whether the object is defective or not, that is, if it has some type of defect, valid options: yes or no.
- Defect type: Defines the type of defect that the object has, an object can have more than one type of defect. Valid options: Warping, Delamination, Stringing, Overhangs, None (no defects).

**They are used in the Flexible and Autonomous Manufacturing Systems for Custom-Designed Products (FASTEN) project (https://inescbrasil.org.br/projetos/projeto-fasten/) whose objective is to develop a manufacturing system for personalized and low-cost products.

## Dependencies

- VIA tool.

# Other repositories

- API: https://github.com/LuckasMacedo2/object-detection-api;
- Mobile app: https://github.com/LuckasMacedo2/object-detection-app

# Files present in the repository

- json_dataset.json: JSON file with the information annotated by the VIA tool. It can be used to process datasets or create new datasets. Note: The location of the objects is in the format of a polygon, but can be converted to the format recognized by object detectors by converting a polygon to a rectangle;
- Imgs: Folder containing all the images for all objects present in the dataset. This is, therefore, the complete dataset. The following other datasets are derived from this one:
    - Object_isDefective_Dataset: Dataset with objects separated into defective and non-defective. They are separated into two training and test folders; within each folder, they are separated according to the class - defective (Defect) or not defective (OK).
    - Defect_Level_Dataset: Dataset with data relating to the defect level of the objects. Contains two training and test folders each containing one of 4 defect levels ranging from zero to three.

# References:

SILVA, L. M.; ALCALÁ, S. G. S.; BARBOSA, T. M. G. A.; ARAÚJO, R. Object and defect detection in additive manufacturing using deep learning algorithms. Production Engineering, p. 1-14, 2024. DOI: http://dx.doi.org/10.1007/s11740-024-01278-y
