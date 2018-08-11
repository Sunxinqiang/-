## Form表单里 button和input提交问题
> 问题：点击button或者input框回车，会提交表单
1. 产生原因：
    1. button的type 属性，IE的默认是 “button”，非IE默认是 “submit”。
    2.  若只有一个input type="text"，按回车键表单会自动提交
2. 解决办法：
    1. button的type属性设置为button
    2. 添加
    ```html
    <input type="text" style="display: none;">
    ```
    3. 
    ```html
    <form action="" method="post" onsubmit="return false;">
    ```
    4. 
    ```html
    <input type="text" onkeydown="if(event.keyCode==13{return false;}">
    ```