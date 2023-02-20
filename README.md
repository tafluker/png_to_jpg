# png_to_jpg
Convert all pngs in a directory to jpgs

#Change the file path!

<img src="https://github.com/tafluker/png_to_jpg/blob/main/png%20snip.png?raw=true" alt="Alt text">

#Copy and paste into Powershell ISE

#Copy everything below this line!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

    $files = (Get-ChildItem -Path C:\file_type_change\ -Filter *.png).FullName

    foreach ($file in $files)

    {

        Add-Type -AssemblyName system.drawing

        $imageFormat = “System.Drawing.Imaging.ImageFormat” -as [type]

        $image = [drawing.image]::FromFile($file)

        $image.Save($file.Replace(".png",".jpg"), $imageFormat::jpeg)

    }
