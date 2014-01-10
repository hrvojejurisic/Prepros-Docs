---
##Tutorial: Using Susy and Responsive Grids sample from NET TUTS+
---

###Context

* MS Windows 8 Profesional x64
* Prepros App v.4.0.0 installed and started with administartor priviledges
* Ruby is not installed

####Notes:
 
  * if you have Ruby installed on your system you can skip steps 9, 10 and 11 of this tutorial;
  * if you have compass, susy and sassy-buttons Ruby gems installed you can skip steps 12 and 13 of this tutorial.

###Tutorial

1. Download sample code from [Responsive Grids With Susy] (http://cdn.tutsplus.com/net/uploads/legacy/2148_grids/code_download.zip) Net Tuts+ tutorial.
    
    ![DownloadSampleCode](img/sass-compass-susy/01-DownloadSampleCode.png)
    
2. Unzip sample into E:\Projects\Web\Prepros\SusyResponsiveGrids (Note: you can use any other folder you like for the sample project's files).
    
    ![UnzipSampleCode](img/sass-compass-susy/02-UnzipSampleIntoSusyResponsiveGridsFolder.png)
    
3. Drag sample code's `E:\Projects\Web\Prepros\SusyResponsiveGrids` folder...
    
    ![Drag Sample Code Folder](img/sass-compass-susy/03-DragSampleCodeFolder.png)
    
4. ...and drop it onto Prepros App main form
    
    ![Drop Sample Code Folder Onto Prepro Main Form](img/sass-compass-susy/04-DragAndDropSampleCodeFolderOntoPreproMainForm.png)
    
5. _SusyResponsiveGrids_ project will be added to the __Prepros App__ projects list.
    
    ![Sample Project Will Be Added To The Prepros Projects List](img/sass-compass-susy/05-SampleProjectWillBeAddedToThePreprosProjectsList.png)
    
6. Right-click on `SusyResponsiveGrids` project entry and select `Compile All Files` item from popup-menu or use `CTRL+SHIFT+S` (_Compile All Files_) short-cut...
    
    ![Compile All Files](img/sass-compass-susy/06-CompileAllFilesOfAProject.png)
    
7. ... and find `Compilation Failed` message box appearing for a few seconds in the right bottom corner of the display screen.
    
    ![Compilation Failed Message Box](img/sass-compass-susy/07-CompilationFailedMessageBox.png)
    
8. Open Prepros log by clicking on `App Log` toolbar button.
    
    ![Check Prepros Log](img/sass-compass-susy/08-CheckPreprosLog.png)
    
9. Figure out that you need a [Full Compass support] (http://alphapixels.com/prepros/docs/sass-compass.html) and that full Compass support requires `Ruby` installed on your system. Go and get downloaded [Ruby installation - Ruby 1.9.3-p484.exe](at http://rubyinstaller.org/downloads/).
    
    ![Download Ruby Setup](img/sass-compass-susy/09-GetRubySetupDownloaded.png)
    
10. Setup Ruby at `C:\Program Files (x86)\Ruby193`, check `Add Ruby executable to your PATH` setup option. (You have to run Ruby setup with Administrator priviledges (`Run as administrator`) to allow setup creating and writing to `C:\Program Files (x86)\Ruby193` folder. (You can select any other folder for Ruby setup - the one, which you'll have full access rights without system administrator priviledges.)
    
    ![Setup Ruby](img/sass-compass-susy/10-SetupRubyAtProgramFiles_x86.png)
    
11. Get Ruby setup completed successfully.
    
    ![Ruby Setup Completed Successfully](img/sass-compass-susy/11-RubySetupCompletesSuccessfully.png)
    
12. Open elevated command prompt window.
    
    ![Open Elevated Command Prompt](img/sass-compass-susy/12-OpenElevatedCommandPrompt.png)
    
13. Install compass, susy and sassy-buttons gems.
    
    ![Install Compass Susy Sassy-Buttons Gems](img/sass-compass-susy/13-InstallCompassSusySassy-ButtonsGems.png)
    
    ```
    >gem install compass susy sassy-buttons
    ```
    ```
    Fetching: sass-3.2.13.gem (100%)
    Fetching: chunky_png-1.2.9.gem (100%)
    Fetching: fssm-0.2.10.gem (100%)
    Fetching: compass-0.12.2.gem (100%)
    Successfully installed sass-3.2.13
    Successfully installed chunky_png-1.2.9
    Successfully installed fssm-0.2.10
    Successfully installed compass-0.12.2
    Fetching: susy-1.0.9.gem (100%)
    Successfully installed susy-1.0.9
    Fetching: sassy-buttons-0.2.6.gem (100%)
    Successfully installed sassy-buttons-0.2.6
    6 gems installed
    Installing ri documentation for sass-3.2.13...
    Installing ri documentation for chunky_png-1.2.9...
    Installing ri documentation for fssm-0.2.10...
    Installing ri documentation for compass-0.12.2...
    Installing ri documentation for susy-1.0.9...
    Installing ri documentation for sassy-buttons-0.2.6...
    Installing RDoc documentation for sass-3.2.13...
    Installing RDoc documentation for chunky_png-1.2.9...
    Installing RDoc documentation for fssm-0.2.10...
    Installing RDoc documentation for compass-0.12.2...
    Installing RDoc documentation for susy-1.0.9...
    Installing RDoc documentation for sassy-buttons-0.2.6...
    ```
    
14. Select Prepros Advanced Options.
    
    ![Select Prepros Advanced Options - Step 1](img/sass-compass-susy/14-SelectPreprosAdvancedOptions-1.png)
    
    ![Select Prepros Advanced Options - Step 2](img/sass-compass-susy/14-SelectPreprosAdvancedOptions-2.png)
    
    ![Select Prepros Advanced Options - Step 3](img/sass-compass-susy/14-SelectPreprosAdvancedOptions-3.png)
        
15. Check `Use Custom Ruby` option, `For Sass` option, enter Ruby setup fullpath `C:\Program Files (x86)\Ruby193\bin\ruby.exe`.
    
    ![Check Use Custom Ruby For Sass Etc](img/sass-compass-susy/15-CheckUseCustomRubyForSassEnterRubySetupFullpath.png)
    
16. Click on screen.scss file to get its options displayed on the right side of the Prepros form, check `Use Compass` and `Full Compass Support` options (the latter option's checkbox will appear after you'll get `Use Compass` option checked. Click `Compile` button.
    
    ![Open screen scss options](img/sass-compass-susy/16-OpenProject_screen_css_FileOptions.png)
    
17. Still no fun - compilation failed.
    
    ![Still no fun](img/sass-compass-susy/17-StillNoFun-CompileError.png)
    
18. Notice that config.rb is needed.
    
    ![Notice that config rb is needed](img/sass-compass-susy/18-NoticeThatConfigRbIsNeeded.png)
    
19. Create config.rb file in `E:\Projects\Web\Prepros\SusyResponsiveGrids` folder.
    
    ![Create config rb file](img/sass-compass-susy/19-CreateConfigRbFile.png)
    
    ```
    # Require any additional compass plugins here.
    require 'susy'
    require 'sassy-buttons'
    
    # Set this to the root of your project when deployed:
    http_path = "/"
    css_dir = "stylesheets"
    sass_dir = "sass"
    images_dir = "images"
    javascripts_dir = "javascripts"
    ```
    
20. Compile again - Compilation Successfull :)
    
    ![20-Compilation Sucessfull](img/sass-compass-susy/20-CompilationSucessfull.png)
    
21. Open Live Preview (Ctrl + L)...
    
    ![Open Live Preview](img/sass-compass-susy/21-OpenLivePreview.png)
    
22. ... and see sample site (`http://localhost:8000/`) previewed in IE. (If you have other browser as your default browser you'd have sample site previewed in that browser).
    
    ![Open Live Preview in IE](img/sass-compass-susy/22-OpenLivePreviewInIE.png)
    
    If you would haven't started Prepros as administartor then you would have got `This page can't be displayed` message page from IE.
    
    ![Open Live Preview in IE not Admin mode](img/sass-compass-susy/22-OpenLivePreviewInIE-PreprosIsNotInAdminMode.png)
    
23. Start Chrome browser and copy and paste sample site Url `http://localhost:8000/`. (Starting Chrome browser in Administrator mode is not needed).
    
    ![Live Preview In Chrome](img/sass-compass-susy/23-LivePreviewInChrome.png)
    
24. Start Firefox browser and copy and paste sample site Url `http://localhost:8000/`. . (Starting Firefox browser in Administrator mode is not needed).
    
    ![Live Preview In Fire Fox](img/sass-compass-susy/24-LivePreviewInFireFox.png)
    
25. Open screen.scss from sample project \sass subfolder.
    
    ![Open Screen Scss](img/sass-compass-susy/25-OpenScreenSCSS.png)
    
    Edit:
    
    ```
       thead{
           color: #FEFEFE;
           background: #000;
    ```
    
    to
    
    ```
       thead{
           color: #FEFEFE;
           background: green;
    ```
    
    and save edits.
    
26. Wait a momment and watch `Compilation Successful` message box in the bottom right corner...
    
    ![Compilation Sucessfull It Works](img/sass-compass-susy/26-CompilationSuccessful.png)
    
27. ... as well as find out that all the three browsers get sample web page tables headers' background color "automagically" changed to Green.
    
    ![Sample Web Page Table Header Background Color Changed](img/sass-compass-susy/27-SampleWebPageTableHeaderBackgroundColorChanged.png)


That's it.

Enjoy!
