# png_to_jpg
Convert all pngs in a directory to jpgs

# Step 1 Copy and paste into Powershell ISE

#START COPYTING HERE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

    $files = (Get-ChildItem -Path C:\file_type_change\ -Filter *.png).FullName

    foreach ($file in $files)

    {

        Add-Type -AssemblyName system.drawing

        $imageFormat = “System.Drawing.Imaging.ImageFormat” -as [type]

        $image = [drawing.image]::FromFile($file)

        $image.Save($file.Replace(".png",".jpg"), $imageFormat::jpeg)

    }
    
#STOP COPYING HERE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

# Step 4 Find Powershell on your computer

![image](https://user-images.githubusercontent.com/46609274/220158387-a79d67a7-a5e6-4c0b-8d7e-5063896e4256.png)

# Step 3 Change the file path!

<img src="https://github.com/tafluker/png_to_jpg/blob/main/png%20snip.png?raw=true" alt="Alt text">




