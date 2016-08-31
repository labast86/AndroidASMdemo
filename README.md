# AndroidASMdemo

# IDE Setup
 * 1. Download Eclipse.
 * 2. Install java on your OS(I'm using Ubuntu14.04LTS), and configure the System variables.
 * 3. Install ADT which is used to develop Android project in Eclipse. Go to this link: http://developer.android.com/sdk/eclipse-adt.html  to download ADT tools. After download the ADT tools, open your Eclipse, and click Help->Install New Software..., then by archive install, please select all the components provided by ADT.
 * 4. Configure Android SDK and create Android Virtual Machine, if your want to run your app on a real device, then you don't need to create Android Virtual Machine. This step is easy, just use the Android SDK and AVD manager, and also please download the corresponding Anroid SDK.
 * 5. OPTIONAL, install CDT, if you select all the components in step 3, you don't need to do this step, but if you don't have CDT installed, please install CDT.
 * 6. Download NDK (Native Development Kit):http://developer.android.com/sdk/ndk/index.html , extract the package and put it somewhere on your disk.
 * 7. Download OpenCV4Android: http://sourceforge.net/projects/opencvlibrary/files/opencv-android/, extract the package and put it somewhere on your disk.

# ASMDemo

**Setup this project**:
 * 1. Import this project by Eclipse.
 * 2. Open the property of this project, click C/C++ Build -> Envrionment, change variable NDKROOT to your NDK root path. Such as : /home/wesong/software/android-ndk-r10d. 
 * 3. If you're using Windows, open the property of NDKDemo project, click C/C++ Build, in Builder setting, change ${NDKROOT}/ndk-build to ${NDKROOT}/ndk-build.cmd
 * 4. Import Opencv4Android into your Eclipse.
 * 5. Open the property of this project, click Android, and delete the default library reference, add your Opencv4Android library reference. (Pointing to the OpenCV4Android project)
 * 6. Still open the property, click C/C++ General -> Path and Symbols, in the include tab, select GNU C++, and find the variable such as "home/bastien/Downloads/OpenCV-2.4.10-android-sdk/sdk/native/jni/include", change this include directories to the OpenCV-2.4.10-android-sdk/sdk/native/jni/include of your opencv4android folder, this will make Eclipse be able to find the head files of opencv.
 * 7. Change Android.mk file, line 8, change the line "include home/bastien/Downloads/OpenCV-2.4.10-android-sdk/sdk/native/jni/OpenCV.mk" to include your OpenCV.mk, find OpenCV.mk on your OpenCV4Android, and put the path here.
