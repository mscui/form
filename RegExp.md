#### 常用符号
[]：字符集  
[^]：不包含在字符集里的内容
\s,\S,\w,\W,\b,\B  
cf：1. \S和\w的区别  
\S包含，。、￥这种符号  
\w不包含这些符号，只是字符  

#### 重复筛选(出现次数)  
贪婪匹配（尽可能多的匹配）{n,m}, {n,}, {n}, ?, \*, +  
非贪婪匹配（尽可能少的匹配）加?,
例如??, +?, \*?  
cf：/a+/和/a+?/的区别：    
     ![Img](https://github.com/Candybunny/form/blob/master/2-1.png)  

#### 组合，分组
|:  或  
():  判断块  
(?:...): 与前一项相同，但是不能用\n来引用（）内的内容    
\n: 括号内的内容，例如：\1  

#### 匹配位置  
^,$,\b,\B,(?=p),(?!p)  
cf:  
1. \b表示\w与\W之间：一般为了取得不包括空格的内容  
     ![Img](https://github.com/Candybunny/form/blob/master/4-1.png) ![Img](https://github.com/Candybunny/form/blob/master/4-2.png)  
2. (?=p) 表示正向先行断言，接下来的字符都与p匹配，但是不包含p这个字符  
     ![Img](https://github.com/Candybunny/form/blob/master/4-3.png)  
3. (?!p) 表示负向先行断言，接下来的字符都不与p匹配  
     ![Img](https://github.com/Candybunny/form/blob/master/4-4.png)  

#### String的使用正则
search：    
     ``` 
     String.search(/.../g);     
     返回匹配的数字 
     ```        
match：  
     ``` 
     String.match(/.../g);        
     返回数组
     ```  
replace：  
     ```
     String.replace(/.../g, ...);    
     ```  
spilt：    
     ```
     String.spilt(/.../g);        
     返回匹配后的数组  
     ```    
#### RegExp使用  
exec:    
     cf:转义字符用两个\\\    
     ```  
     var reg = new RegExp("\\d{3}", "g");          
     reg.exec(String);     
     返回匹配到的数组，区别于match，如果不递归调用，只返回一组数据  
     ```  
     ![Img](https://github.com/Candybunny/form/blob/master/6-1.png)  
     ![Img](https://github.com/Candybunny/form/blob/master/6-2.png)  
test:  
     ```
     reg.test(String);    
     返回true，false       
     ```    
     ![Img](https://github.com/Candybunny/form/blob/master/6-3.png)  

