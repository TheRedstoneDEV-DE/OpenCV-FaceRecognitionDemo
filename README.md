# OpenCV-FaceRecognitionDemo
The FaceRecognitionDemo from OpenCV version 2.4 updated to OpenCV verseion 4.x

I've had the Idea to write a face recognition software using OpenCV, but I needed the demo code, to see how the face recognition with OpenCV really works.
The original demo code was only availlable in version 2.4 and was not going to work with version 4.x (**just compiling the version 2.4 was not an option,
because it would just throw lots of error messages saying that variables are not set and other things**), 
so I had to change some of the code, to get it working with this version. If you had the same problem, you're lucky, here is the source code which is 
working with version 4.x.

## Building and running

### Dependencies:
- OpenCV version 4 (follow the build instructions on their website)
- g++, make, cmake
normally it should be everything, when you get issiues,
just install the dependencies opencv needs for building
- a linux mashine (it should be enougth, when you create a virtual mashine and pass your webcam through)
(on Windows you would need VisualStudio and a c++ extension, just search for a guide how to use and install OpenCV on Windows and replace 
the source with the  content of the main.cpp)

### Step 1:
Clone the github repository:
```bash
git clone https://github.com/TheRedstoneDEV-DE/OpenCV-FaceRecognitionDemo.git
```
or just download it as zip and unpack it

### Step 2:

If not allready done change directory into the Folder of the clone:
```bash
cd OpenCV-FaceRecognitionDemo
```

Create the build directory:
```bash
mkdir build && cd build
```

### Step 3:
Run cmake:
```bash
cmake ..
```

### Step 4:
Compile the configured Makefile:
```bash
make
```

### Step 5 (final):
Run the demo:
```bash
./FaceRecognitionDemo </path/to/haar_cascade> </path/to/csv.ext> </path/to/device id>
```

The parameters mean:

`</path/to/haar_cascade>` -- Path to the Haar Cascade for face detection. 
(normally in `<OpenCVInstallDir>/data/haarcascades/haarcascade_frontalface_default.xml`)

`</path/to/csv.ext>` -- Path to the CSV file with the face database. (more info in their documentation: <https://docs.opencv.org/4.x/da/d60/tutorial_face_main.html>)

`<device id>` -- The webcam device id to grab frames from.



