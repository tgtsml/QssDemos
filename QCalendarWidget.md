QCalendarWidget样式

1. 背景
	QCalendarWidget QWidget

2. 顶部按钮
	QCalendarWidget QToolButton
	设置顶部按钮是否可见：
	setNavigationBarVisible();
	
3. 月份加减按钮
    可以通过QObject::objectName()打印每个控件的对象名
    QCalendarWidget QToolButton#qt_calendar_prevmonth
    QCalendarWidget QToolButton#qt_calendar_nextmonth

4. 月份菜单按钮
    QCalendarWidget QMenu
    即设置菜单样式

5. 年份选择按钮
    QCalendarWidget QSpinBox
    即设置QSpinBox样式

6. 日历主体
    QCalendarWidget QAbstractItemView
    当前月份的日期属性：enable
    上月或下月的日期属性：disabled

7. 设置日期控件显示语言——周一 ~ 周日
    日期控件：

  >calendarWidget->setLocale(QLocale(QLocale::English));
  calendarWidget->setLocale(QLocale(QLocale::Chinese, QLocale::China));

  弹出日期控件：
  >dateEdit->calendarWidget()->setLocale(QLocale(QLocale::English));
  dateEdit->calendarWidget()->setLocale(QLocale(QLocale::Chinese, QLocale::China));

  设置栅格显示：
  >setGridVisible();

  设置显示格式：
  >setHorizontalHeaderFormat()
  可选参数：
  QCalendarWidget::SingleLetterDayNames
  QCalendarWidget::ShortDayNames
  QCalendarWidget::LongDayNames
  QCalendarWidget::NoHorizontalHeader

8. 周数显示
    setVerticalHeaderFormat()
    可选参数：
    QCalendarWidget::ISOWeekNumbers
    QCalendarWidget::NoVerticalHeader

* 示例
	```CSS
    QCalendarWidget QWidget{
        background-color:rgb(25,115,82);
        alternate-background-color: rgb(200,200,200);
    }
    QCalendarWidget QToolButton{
        margin-top:0px;
        margin-bottom:0px;
        height:24px;
        color:white;
        icon-size:24px 24px;
    }
    QCalendarWidget QToolButton#qt_calendar_prevmonth{
    icon-size:25px, 25px;
    margin-left:5px;
    qproperty-icon:url(:/arrow_left.png);
    }
    QCalendarWidget QToolButton#qt_calendar_nextmonth{
    icon-size:25px, 25px;
    margin-right:5px;
    qproperty-icon:url(:/arrow_right.png);
    }
    QCalendarWidget QAbstractItemView{
        font-size:13px;
    }
    QCalendarWidget QAbstractItemView:enabled{
        background-color: white;
        selection-background-color: rgb(200,200,200);
        color:black;
    }
    QCalendarWidget QAbstractItemView:disabled{
        color:rgb(150,150,150);
    }
    QCalendarWidget QMenu{
        margin:0px;
        width:90px;
        background-color:white;
    }
    QCalendarWidget QMenu::item:selected{
        color:black;
        background-color:#CCE8FF;
    }
    QCalendarWidget QSpinBox {
        width: 40px;
        margin-top:1px;
        background-color:white;
    }
    QCalendarWidget QSpinBox::down-arrow{
        image:url(:/dropdownArrow.png);
    }
    QCalendarWidget QSpinBox::up-arrow{
        image:url(:/dropupArrow.png);
    }
	```

	![image-20201126093901176](md_images\image-20201126093901176.png) ![image-20201126094131651](md_images\image-20201126094131651.png)
