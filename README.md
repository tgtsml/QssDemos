# QssDemos
QSS of Qt Controls

- 边框<br>
border<br>
border-top<br>
border-right<br>
border-bottom<br>
border-left<br>
border-image<br>

- 外边距<br>
margin<br>
margin-top<br>
margin-right<br>
margin-bottom<br>
margin-left<br>

- 内边框<br>
padding<br>
padding-top<br>
padding-right<br>
padding-bottom<br>
padding-left<br>

- 边角<br>
border-radius<br>
border-top-left-radius<br>
border-top-right-radius<br>
border-bottom-right-radius<br>
border-bottom-left-radius<br>

- 背景色<br>
background<br>
background-color<br>

- 前景色<br>
color<br>

- 图片<br>
image url("...")<br>

- 表格<br>
alternate-background		//交替色<br>
gridline-color					//栅格<br>
selection-background-color<br>
selection-color<br>
注：需在CPP文件添加 table->setAlternatingRowColors(true);<br>

- 选中表格单元格后表头字体不高亮<br>
QHeaderView::setHighlightSections(false);<br>

- 下拉框<br>
对下拉列表的样式设置需要在CPP代码里面手动设置：<br>
//禁用item0<br>
ui->comboBox->setItemData(0, 0, Qt::UserRole - 1);<br>
//取消禁用item2<br>
ui->comboBox->setItemData(2, -1, Qt::UserRole - 1);<br>
//设置代理，以应用QSS<br>
ui->comboBox->setView(new QListView);<br>


Control-Name|Qss-MainPoints
-|-
[QCheckBox](https://github.com/tgtsml/QssDemos/blob/master/QCheckBox.txt)|::indicator, :checked, :unchecked, :indeterminate
[QComboBox](https://github.com/tgtsml/QssDemos/blob/master/QComboBox.txt)|::item, ::selected, ::drop-down, ::down-arrow
[QCompleter](https://github.com/tgtsml/QssDemos/blob/master/QCompleter.txt)|::item, QCompleter::popup()
[QScrollBar](https://github.com/tgtsml/QssDemos/blob/master/QScrollBar.txt)|::handle, ::sub-line, ::add-line, ::up-arrow, ::down-arrow, ::sub-page, ::add-page, ::left-arrow, ::right-arrow
[QSlider](https://github.com/tgtsml/QssDemos/blob/master/QSlider.txt)|::groove, ::handle, ::add-page, ::sub-page
[QTableView](https://github.com/tgtsml/QssDemos/blob/master/QTableView.txt)|QHeaderView::section, selection-background-color, selection-color, alternate-background-color


- Sub-Controls
    ```
    ::add-line 
    ::add-page 
    ::branch 
    ::chunk 
    ::close-button 
    ::corner 
    ::down-arrow 
    ::down-button 
    ::drop-down 
    ::float-button 
    ::groove 
    ::indicator 
    ::handle 
    ::icon 
    ::item 
    ::left-arrow 
    ::left-corner 
    ::menu-arrow 
    ::menu-button 
    ::menu-indicator 
    ::right-arrow 
    ::pane 
    ::right-corner 
    ::scroller 
    ::section 
    ::separator 
    ::sub-line 
    ::sub-page 
    ::tab 
    ::tab-bar 
    ::tear 
    ::tearoff 
    ::text 
    ::title 
    ::up-arrow 
    ::up-button 
    ```

- Pseudo-State
	```
	:active 
	:adjoins-item 
	:alternate 
	:bottom 
	:checked 
	:closable 
	:closed 
	:default 
	:disabled 
	:editable 
	:edit-focus 
	:enabled 
	:exclusive 
	:first 
	:flat 
	:floatable 
	:focus 
	:has-children 
	:has-siblings 
	:horizontal 
	:hover 
	:indeterminate 
	:last 
	:left 
	:maximized 
	:middle 
	:minimized 
	:movable 
	:no-frame 
	:non-exclusive 
	:off 
	:on 
	:only-one 
	:open 
	:next-selected 
	:pressed 
	:previous-selected 
	:read-only 
	:right 
	:selected 
	:top 
	:unchecked 
	:vertical 
	:window 
	```