# 文字
<details> <summary>换行</summary>  
  
- **代码**
  ```
      法一  
      在上一行文本后面补两个空格，这样下一行的文本就换行了

      法二
      在两行文本直接加一个空行  
      也能实现换行效果，不过这个行间距有点大

      法三<br>
      在每行后加<br>也可实现换行效果
  ```

- **效果**  
  第一行  
  第二行<br>
  第三行

  第四行

</details>

<details> <summary>标题</summary>  

- **代码**
  ```
      # 一级标题
      ## 二级标题
      ### 三级标题
      #### 四级标题
      ##### 五级标题
      ###### 六级标题
  ````
  
- **效果**
  # 一级标题
  ## 二级标题
  ### 三级标题
  #### 四级标题
  ##### 五级标题
  ###### 六级标题

</details>

<details> <summary>文本块</summary>  

  - 普通文本<br>
  
    一段普通的文本  

  - 单行文本
    ```
    在一行开头加入1个Tab或者4个空格
    ```
  - 文本块
    ```
    方法：
    使用一对各三个的反引号
    ```
</details>

<details> <summary>文字高亮</summary> 
  
- **代码**
  ```
  文字高亮功能能使行内部分文字高亮，使用一对反引号
   `学习` `编程`
  ```

- **效果**  
  `学习` `编程`

 </details>

 <details> <summary>斜体、粗体、删除线</summary>

 - **代码**
   ```
   *斜体1*
   _斜体2_
    **粗体1**
    __粗体2__
    ~~删除线~~
    ***斜粗体1***
    ___斜粗体2___
    ***~~斜粗体删除线1~~***
    ~~***斜粗体删除线2***~~
    ```
- **效果**  
  *斜体1*  
  _斜体2_  
  **粗体1**  
  __粗体2__  
  ~~删除线~~  
  ***斜粗体1***  
  ___斜粗体2___  
  ***~~斜粗体删除线1~~***  
  ~~***斜粗体删除线2***~~

   </details>

# 图片
<details><summary>代码</summary>
  
  ```
  基本格式：  
  ![alt](URL title)

  alt和title即对应HTML中的alt和title属性（都可省略）：  
  alt表示图片显示失败时的替换文本  
  title表示鼠标悬停在图片时的显示文本（注意这里要加引号）
 
  URL即图片的url地址，如果引用本仓库中的图片，直接使用相对路径就可了，
  如果引用其他github仓库中的图片要注意格式，即：仓库地址/raw/分支名/图片路径，如：
  https://github.com/guodongxiaren/ImageCache/raw/master/Logo/foryou.gif
  ```

</details>

<details><summary>效果</summary>
  
![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")  

</details>

# 链接

<details><summary>链接外部URL</summary>
  
- **代码**
  
  ```
  [他的博客](http://blog.csdn.net/guodongxiaren "悬停显示")
  ```
- **效果**  
  [他的博客](http://blog.csdn.net/guodongxiaren "悬停显示")
</details>

<details><summary>链接本仓库里的URL</summary>

- **代码**
  
  ```
  [他的简介](/example/profile.md)
  ```
- **效果**  
  [他的简介](/example/profile.md)
</details>

<details><summary>引用链接</summary>

- **代码**
  
  ```
  [他的博客][boke]
  
  [boke]: http://blog.csdn.net/guodongxiaren
  ```
- **效果**
  
  [他的博客][boke]
  
  [boke]: http://blog.csdn.net/guodongxiaren
  
</details>

<details><summary>图片链接</summary>

- **代码**
  
  ```
  ![baidu](http://www.baidu.com/img/bdlogo.gif "百度logo")	
  ```
- **效果**
  
  [![baidu-logo]](http://www.baidu.com)

  [baidu-logo]: http://www.baidu.com/img/bdlogo.gif
  
</details>








  
