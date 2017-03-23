# ppt技巧
### 将word内容分页插入到ppt中
- 使用母版，设置格式
- 将word内容复制到ppt中
- 进入大纲视图
- enter，开始，降低列表等级（机械运动，理论上可以通过宏完成）


# ppt 宏
- 将ppt中的图片排列整齐
``` VB
Sub setthepicture()
    Dim sld As Slide, shp As Shape
	For Each sld In ActivePresentation.Slides
	i = 1
	For Each shp In sld.Shapes
		If shp.Type = msoPicture Then

            shp.ScaleHeight 1, msoFalse
			shp.Top = 20 * i
			shp.Left = 20
			i = i + 5
		End If
		Next
	Next
End Sub
```
