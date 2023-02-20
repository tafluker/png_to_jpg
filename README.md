# png_to_jpg
Convert all pngs in a directory to jpgs

# Step 1 Copy this code

#**START** COPYING HERE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

    $files = (Get-ChildItem -Path C:\file_type_change\ -Filter *.png).FullName

    foreach ($file in $files)

    {

        Add-Type -AssemblyName system.drawing

        $imageFormat = “System.Drawing.Imaging.ImageFormat” -as [type]

        $image = [drawing.image]::FromFile($file)

        $image.Save($file.Replace(".png",".jpg"), $imageFormat::jpeg)

    }
    
#**STOP** COPYING HERE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

# Step 2 Find and open Powershell on your computer

![image](https://user-images.githubusercontent.com/46609274/220158387-a79d67a7-a5e6-4c0b-8d7e-5063896e4256.png)

# Step 3 Paste the code into powershell

![image](https://user-images.githubusercontent.com/46609274/220159985-626aca62-2dcb-4aa1-a64b-835205337d55.png)

# Step 4 Change the file path!

<img src="https://github.com/tafluker/png_to_jpg/blob/main/png%20snip.png?raw=true" alt="Alt text">

# Step 5 Run the code by pressing the play button

![image](https://user-images.githubusercontent.com/46609274/220160946-1b14d356-d390-4516-9c6f-fee48c7a776f.png)







