# READ.MD的使用方法

## 1 高亮操作
* 1.`高亮`显示
  * 二级高亮，具体请[百度](http://www.baidu.com "悬停显示")
      * 三级高亮
> 字符包含
>> 二级字符包含


## 2 书籍引用
> 最近对它的README.md文件颇为感兴趣。便写下这贴，帮助更多的还不会编写README文件的同学们。
README文件后缀名为md。md是markdown的缩写，markdown是一种编辑博客的语言。用惯了可视化的博客编辑器（比如CSDN博客，囧），这种编程式的博客编辑方案着实让人眼前一亮。不过GitHub支持的语法在标准markdown语法的基础上做了修改，称为Github Flavored Markdown，简称GFM。可不是GFW呀偷笑。

转载注明出处：http://blog.csdn.net/kaitiren/article/details/38513715

我在GitHub上为本文建的一个仓库“test”，供大家查看代码即具体效果：https://github.com/guodongxiaren/test 


## 3 代码格式 
```c
/*指针操作*/
void  reverse_string(char * s)  
{  
    char*	p=s;  
    char temp;  
    while(*p) p++;  //让p指向最后一个字符  
    p--;  
    while(s<=p)  
    {  
        SWAP(*s,*p,temp);   //交换两个字符，宏函数实现  
        s++;  
        p--;  
    }  
} 
```
### 三级标题未用
