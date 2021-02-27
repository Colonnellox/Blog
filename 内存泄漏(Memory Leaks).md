# 内存泄漏(Memory Leaks)

Tag: <code>性能优化</code>
---

### ADB导出hprof文件

    adb shell am dumpheap pid/package name file
    
支持包名和进程id两种方式

### [Android Profiler](https://developer.android.com/studio/profile/memory-profiler)

  打开方式 依次点击 View > Tool Windows > Profiler（您也可以点击工具栏中的 ![Profile](https://developer.android.com/studio/images/buttons/toolbar-android-profiler.png) 图标 ）。点击MEMORY模块。
  
### 常见的内存泄漏点

  - 内部类持有对外部的引用
  
  - View布局没有从父布局removeView
  
  - Activity context 被静态持有
