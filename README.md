# JAceessibityDemo
Android UI自动化Demo

# 注意事项
  （1）不知道从哪个Android版本开始，AccessibilityService的声明需要在代码中动态声明了，在config资源文件中声明式无效的。  
  （2）Flag标志必须在config资源文件中声明，在代码中动态声明会获取不到root元素节点。
# 设计要点
## 事件过滤
 用户的一次屏幕操作（如点击）可能触发多个 AccessibilityEvent（例如 TYPE_VIEW_CLICKED、TYPE_WINDOW_CONTENT_CHANGED 等），需要实现一些机制来避免重复处理。以下是我的处理方法：  
 （1）节点哈希值去重法。
