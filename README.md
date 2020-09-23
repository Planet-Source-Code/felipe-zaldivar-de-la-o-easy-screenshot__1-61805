<div align="center">

## Easy ScreenShot


</div>

### Description

When u've Style Xp and u take a screenshot u&#180;ll see that the taskbar &#180;ll not appear this solves the problem!!!! :::::Take screenshots with only 7 lines ::::: Rate me pls!!!!!
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Felipe Zaldivar  de la O](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/felipe-zaldivar-de-la-o.md)
**Level**          |Intermediate
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 6\.0
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__1-46.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/felipe-zaldivar-de-la-o-easy-screenshot__1-61805/archive/master.zip)

### API Declarations

```
Private Declare Sub keybd_event Lib "user32" (ByVal bVk As Byte, ByVal bScan As Byte, _
                       ByVal dwFlags As Long, ByVal dwExtraInfo As Long)
```


### Source Code

```

'''1 picture box
'''1 commandbutton
Private Sub Command1_Click()
  Dim tempfile As String
  tempfile = App.Path & "\picture.bmp"
  keybd_event vbKeySnapshot, 0, 0, 0
  DoEvents
  SavePicture Clipboard.GetData(vbCFBitmap), tempfile
  Picture1.Picture = LoadPicture(tempfile)
End Sub
```

