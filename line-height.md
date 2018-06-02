# line-height

## line-height 定义

* line-height：行高指的是两行文字基线之间的距离。

  ###  什么是基线：

  ![mahua](./public/images/base-line.jpeg)

  基线（baseline），指的是一行字横排时下沿的基础线，基线并不是汉字的下端沿，而是英文字母 x 的下端沿。

  ### 基线乃\*线定义之根本。(顶线、中线、底线)

  ![mahua](./public/images/line.png)

  ### 行距与行高(文本行的基线间的距离)：

  ![mahua](./public/images/line-height.jpg)

* line-height 与行内框盒子模型

  所有内联元素的样式表现都与行内框盒子模型有关！

  ```html
  <p>这是一行普通的文字，这里有个<em>em</em>标签。</p>
  ```

  这普通的一行包含了 4 种盒子，下面详解。

  1、内容区域(content area)，是一种围绕文字看不见的盒子。内容区域的大小与 font-size 大小相关。

  ![mahua](./public/images/content-area.png)

  2、内联盒子(inline boxes)，内联盒子不会让内容成块显示，而是排成一行。如果(文字)外部包含 inline 水平的标签(span、a、em、strong 等)，则属于内联盒子。如果是个光秃秃的文字，则属于匿名内联盒子。

  ![mahua](./public/images/inline-boxes.jpeg)

  3、行框盒子(line boxes)，每一行就是一个行框盒子，每个行框盒子又是由一个一个内联盒子组成。

  4、p 标签所在的包含盒子(containing box)，此盒子有一行一行的行框盒子组成。

* line-height 的高度机理(机制原理)

  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>line-height</title>
    <style>
      .test1 {
        font-size: 36px;
        line-height: 1px;
        background: green;
        border: 1px solid #FFF
      }
      .test2 {
        font-size: 0px;
        line-height: 36px;
        background: green;
        border: 1px solid #FFF
      }
    </style>
  </head>
  <body>
    <p class="test1">测试：行高是由字体撑开的</p>
    <br>
    <br>
    <p class="test2">测试：行高是由line-height决定的</p>
  </body>
  </html>
  ```

  [查看页面](http://localhost:4000/html/test.html)
