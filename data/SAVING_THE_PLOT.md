##### Export images

To save your plot as a PNG file, click on the small camera icon on the top right corner of the plot.

For Venn and Upset plots, simply right-click on the chart and "save image".

##### Automatically update PowerPoint with new images

All plots are saved with an unique name tied to the plot type and parameters. 

For instance, a multi-tier bar chart on Sales and by Sub_Category with 4 top items will be always saved as "multi-tier_bar_d867c0043f06eabf7c0b97d1d022d0ce.png" 

The advantage is that if you insert this particular chart in a ppt deck and then rerun the chart with an updated dataset, the chart will be generated with the same name. Therefore it is possible to update the PowerPoint presentation automatically.

To achieve this you must:

   (i) Save your PowerPoint as a .pptm (macro-enable powerpoint file)

   (ii) Add this macro to the PowerPoint file.        

```
Sub UpdateImages()

For Each Slide In Application.ActivePresentation.Slides
    For Each sh In Slide.Shapes        Debug.Print sh.Name
        If sh.Type = msoLinkedPicture Then
            sh.LinkFormat.Update
            Debug.Print sh.Name & " updated"
        End If        
   
Next sh
Next Slide
End Sub
```

 (iii) Save images to same directory where pptm file is saved

 (iv) Insert your plot images with "insert and link" option

  (v) Run the macro in PowerPoint in the view tab. The new images will take the place of the old ones in the PowerPoint file.