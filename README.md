# VideoTrimmer - A library with UI and mechanisms to trim local videos on Android applications.

#### This project aims to provide an ultimate and flexible video trimmer experience.

<img src="https://github.com/knowledge4life/k4l-video-trimmer/raw/master/Screenshots/Screenshot.png" alt="VideoTrimmer Screenshot" width="400" height="568" />

# Usage

*For a working implementation, please have a look at the Sample Project - sample*

1. Include the library as local library project.

    ``` compile 'life.knowledge4:k4l-video-trimmer:1.0' ```
    
2. Add K4LVideoTrimmer component into your layout.

    ```
    <life.knowledge4.videotrimmer.K4LVideoTrimmer
        android:id="@+id/timeLine"
        android:layout_height="match_parent"
        android:layout_width="match_parent" />
    ```

3. Set the K4LVideoTrimmer selected video Uri.

    ```java
    K4LVideoTrimmer videoTrimmer = ((K4LVideoTrimmer) findViewById(R.id.timeLine));
    if (videoTrimmer != null) {
        videoTrimmer.setVideoURI(Uri.parse(path));
    }
    ```

# Default destination folder
    ```java
    Environment.getExternalStorageDirectory()
    ```

# Here is an example of a listener implementation.

1. Implements `OnTrimVideoListener` methods

    ```java
    @Override
    public void getResult(final Uri uri) {
        // handle K4LVideoTrimmer result.
    }

    @Override
    public void cancelAction() {
        // handle K4LVideoTrimmer cancel action
    }
    ```

# Customization

* Custom destination folder
    ```java
    videoTrimmer.setDestinationPath("/storage/emulated/0/DCIM/CameraCustom/");
    ```

* Set maximum video time interval
    ```java
    videoTrimmer.setMaxDuration(10);
    ```

# Incoming improvements

- Customize K4LVideoTrimmer colors
- Customize K4LVideoTrimmer drawables
- Add support for `setMinDuration`
- Add tests

# Known issues and limitations
- Thumbnails are only added to the timeline once all of them are created in a background thread
- As for now there is no way of personalising the component
- We only support MP4 files
- Methods count: 5768 from Isoparser + [CHECK HOW MANY METHODS THERE ARE IN OUR LIB] from K4l-video-trimmer
    
# Compatibility
  
  * Library - Android ICS 4.1+ (API 16)
  * Sample - Android ICS 4.1+ (API 16)

## Collaboration
There are many ways of improving and adding more features, so feel free to collaborate with ideas, issues and/or pull requests.  
  
### Let us know!

We’d be really happy if you sent us links to your projects where you use our component. Just create an issue and let us know if you have any questions or suggestion regarding the library.