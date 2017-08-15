#CSS样式表
##1css简单认识。
 **一般分为三种:(1)行内>内联>外联
 
 ##2css选择器
 ###2.1基本选择器
   
   (1)*{}通用选择器 会给所有加样式(包括html和body)
 ```css
   <html>
      <head>
        <title></title>
        <style>
           *{
                color: red;
              }
        </style>
      </head>
      <body>
          <p>这是css样式表</p>
      </body>
   </html>
 
   
```
   (2)元素选择器    p{}
   ```css
      <html>
         <head>
           <title></title>
           <style>
              p{
                   color: red;
                 }
           </style>
         </head>
         <body>
             <p>这是css样式表</p>
         </body>
      </html>
    
      
   ```
   
   (3)Id选择器      #{}
   
   ````css
      <html>
         <head>
           <title></title>
           <style>
              #abc{
                   color: red;
                 }
           </style>
         </head>
         <body>
             <p id="abc">这是css样式表</p>
         </body>
      </html>
    
      
   ````
   
   (4)class选择器  .abc{}  p.abc{} class="abc def"

         <html>
            <head>
              <title></title>
              <style>
                 .abc{
                      color: red;
                    }
              </style>
            </head>
            <body>
                <p class="abc def">这是css样式表</p>
                <p class="abc">这是css样式表</p>
            </body>
         </html>

   
   (5)属性选择器     [href]{}  [type="password]{}
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
              <a href="www.baidu.com"></a>
              <input type="password"></input>
            </body>
         </html>
   
   (6)属性值开头匹配         [href^="http"] {}
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
              <a href="http://www.baidu.com"></a>
              <input type="password"></input>
            </body>
         </html>
   
               
   (7)属性值结尾匹配      [href$=".com"]{}
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
              <a href="www.baidu.com"></a>
              <input type="password"></input>
            </body>
         </html>
   
   (8)属性值包含        [href*="baidu"]{}
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
              <a href="www.baidu.com"></a>
              <input type="password"></input>
            </body>
         </html>
   
   (9)属性有多个值                [class~="def"]{}
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
              <a href="www.baidu.com"></a>
              <input type="password"></input>
            </body>
         </html>
   
   (10)属性有多个值如 <i lang="en_us">HTML5</i>    [lang|="en"]{} 
   
         <html>
            <head>
              <title></title>
            </head>
            <body>
               <i lang="en_us">HTML5</i>
            </body>
         </html>
   
   ###2.2复合选择器
   (1)分组选择器   p,i,b,span{}
       
              <html>
                   <head>
                     <title></title>
                   </head>
                   <body>
                      <p>这是一个标签</p>
                      <i>这是一个标签</i>
                      <b>这是一个标签</b>
                      <span>这是一个标签</span>
                   </body>
                </html>
   
   (2)后带选择器   p b{}选择p的所有b不在乎b的深度
           
                         <html>
                            <head>
                              <title></title>
                            </head>
                            <body>
                               <p><b>这是<span><b>一个</b></span>标签</b></p>
                            </body>
                         </html>
         
   
   (3)子选择器    ul>li{}只能是儿子
