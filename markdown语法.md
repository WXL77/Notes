[toc]
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
使用引用链接能达到复用的目的，一般把全文所有的URL标识符统一放在文章末尾，这样看起来比较干净。除了干净之外，它还能达到复用的目的，比如你在多个地方想使用同一个链接，那么文内使用标识符，只在最底部给标识符定义出实际的URL链接即可，类似编程语言中的变量。
  
- **代码**
  
  ```
  [他的博客][boke]
  
  [boke]: http://blog.csdn.net/guodongxiaren（统一放在文末，运行后被隐藏）
  ```
- **效果**
  
  [他的博客][boke]
  
</details>

<details><summary>图片链接</summary>

- **代码**
  
  ```
  [![baidu-logo]](http://www.baidu.com)

  [baidu-logo]: http://www.baidu.com/img/bdlogo.gif（统一放在文末，运行后被隐藏）
  ```
- **效果**
  
  [![baidu-logo]](http://www.baidu.com)
  
</details>

<details><summary>锚点</summary>
  
每一个标题都是一个锚点

- **代码**
  
  ```
  [回到顶部](#顶部标题)	
  ```
- **效果**
  
  [回到顶部](#文字)	
  
</details>

# 列表

<details><summary>无序列表</summary>
  
- **代码**
  ```
  * 昵称：果冻虾仁
  - 别名：隔壁老王
  * 英文名：Jelly
    * 多级无序列表
  ```
- **效果**
  * 昵称：果冻虾仁
  - 别名：隔壁老王
  * 英文名：Jelly
    * 多级无序列表
</details>

<details><summary>有序列表</summary>
  
- **代码**
  ```
  1. 封装
     1. 继承
        1. 多态
  ```
- **效果**  
1. 封装
   1. 继承
      1. 多态
     
</details>

<details><summary>复选框列表</summary>

- **代码**
  ```
  - [x] 需求分析
  - [x] 系统设计
  - [x] 详细设计
  - [ ] 编码
  - [ ] 测试
  - [ ] 交付
  ```
- **效果**
  - [x] 需求分析
  - [x] 系统设计
  - [x] 详细设计
  - [ ] 编码
  - [ ] 测试
  - [ ] 交付
</details>

# 块引用  
<details><summary>多级结构</summary>
  
- **代码**
  ```
  > 数据结构
  >> 树
  >>> 二叉树
  >>>> 平衡二叉树
  >>>>> 满二叉树
  ```
- **效果**
  > 数据结构
  >> 树
  >>> 二叉树
  >>>> 平衡二叉树
  >>>>> 满二叉树
</details>

<details><summary>代码高亮</summary>
  
- **代码**    
  在三个反引号后面加上编程语言的名字，另起一行开始写代码，最后一行再加上三个反引号
  
- **效果**
  ```sql
  select *
  from t1
  ```
</details>

# 表格
<details><summary>创建表格</summary>

- **代码**
  ```
  请使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列  
  | 标题一 | 标题二 |
  | ------ | ------|
  | Header | Title |
  | Paragraph | Text |
  ```
- **效果**
  | 标题一 | 标题二 |
  | ------ | ------|
  | Header | Title |
  | Paragraph | Text |
  
</details>

<details><summary>对齐方式</summary>

- **代码**  
  ```
  通过在标题行中的连字符的左侧，右侧或两侧添加冒号（:），将列中的文本对齐到左侧，右侧或中心。
  |左对齐	  |居中    |	 右对齐|
  |:---|:---:|---:|
  |col 3 is	  | some wordy text	     |$1600    |
  |col 2 is    |	centered	      |$12       |

  ```
- **效果**
  |左对齐	     |居中                   |	 右对齐         |
  |:---        |      :---:            |    ---:         |
  |col 3 is	   | some wordy text	     |$1600            |
  |col 2 is    |	centered	           |$12              |

</details>

<details><summary>混合文字加粗、斜体等语法</summary>
  
  |**左对齐**	  |居中    |	 右对齐|
  |:---|:---:|---:|
  |col 3 is	  | some wordy text	     |$1600    |
  |col 2 is    |	centered	      |$12       |

</details>







***
**以下是被引用的链接**  （运行后被隐藏）

[boke]: http://blog.csdn.net/guodongxiaren  

[baidu-logo]: http://www.baidu.com/img/bdlogo.gif "百度logo"


  






