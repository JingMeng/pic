

1.

关于适配器的这个，看一下hongyang的那个，一起总结一下

 0. 直接传递String进去
 
 1.new TextVIew的情况
 样式太单一 
 
 2.点击事件不好处理

 3.我们传递的不一定是String

==================================


2.

源码分析的目的是为了在开发的过程中避免犯错
应该明白各式各样的问题


3.


案例很不错呀

4.

事件变成对象
ListenerInfo 

5.

你覆写了VIew的onTouchEvent
就要考虑onClick要不要执行
这种代码
比如vp


覆写dispatchTouchEvent 
就是完全你自己托管了
这个就是下拉刷新的代码了

