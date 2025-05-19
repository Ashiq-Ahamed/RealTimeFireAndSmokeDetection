# RealTimeFireAndSmokeDetection

Fire is detected using a color range in the HSV color space. The script checks for red and yellow colors typically found in flames. Two color masks (red and yellow) are created, and then combined to detect fire.

### Smoke Detection

Smoke detection is based on motion and edge detection. The script converts the frame to grayscale, applies Gaussian blur, and uses the Canny edge detector to find smoke.

### Real-Time Detection

The main function real\_time\_fire\_smoke\_detection() captures video from a specified source (webcam or video file), processes each frame to detect fire and smoke, and displays the results.

Functions
---------

### detect\_fire(frame)

This function detects fire in a frame by identifying pixels that match the red and yellow color ranges.

*   **Input**: A video frame (image).
    
*   **Output**: A binary mask indicating the regions where fire is detected.
    

### detect\_smoke(frame)

This function detects smoke in a frame by using edge detection.

*   **Input**: A video frame (image).
    
*   **Output**: A binary mask highlighting the edges that may indicate smoke.
    

### real\_time\_fire\_smoke\_detection(video\_source=0)

This function captures frames from a video source (e.g., webcam or video file), processes them to detect fire and smoke, and displays the results.

*   **Input**: A video source (default is 0, which is the webcam).
    
*   **Output**: Displays the original video, fire detection, smoke detection (edges), and combined results.
    

Running the Code
----------------

You can run the script by calling the main function real\_time\_fire\_smoke\_detection(). If you want to process a specific video file, provide the path to the file.

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pythonCopyEditreal_time_fire_smoke_detection("path_to_video.mp4")   `

If you want to use a webcam, the default video source (0) will be used:

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   pythonCopyEditreal_time_fire_smoke_detection()   `

Key Points
----------

*   The fire detection uses HSV color space with specific red and yellow ranges.
    
*   The smoke detection utilizes the Canny edge detection technique.
    
*   The combined output of fire and smoke detections is displayed in real time.
    

License
-------

This project is licensed under the MIT License - see the LICENSE file for details.
