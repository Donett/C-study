# 1-19 reverse函数实现字符串s顺序逆转

---
## 1.我的版本
缺点：把把原字符串给弄没了
```c
int main()
{	
	char s[1000]="123456";
	reverse(s);		
	puts(s);		//for(i=0;i<=strlen(s);i++)	printf("%c",s[i]);
	while(1);
}

void reverse(char *a)   /*数组操作：缺：需要开辟一个新数组，且操作了n次*/
{
	int i;
	int b[1000];
	int length;

	length=strlen(a);
	for(i=0;i<length;i++)
		b[i]=a[length-1-i];	//操作了i次，大神的操作只用N/2次，用交换方式，且不用新数组
	b[length]='\0';
	
	for(i=0;i<=length;i++)
		a[i]=b[i];
}
```
改进：
```c
//交换数组一半之前的 和一半之后的。所以要 length-1
//数组最后一位'\0' 另外幅值
	for(i=0;i<length/2;i++)
		SWAP(a[i],a[length-1-i],c);
	a[length]='\0';
```
改进
```c
//指针操作 更高级
//局部变量p要赋初值！！
//p=s和我的操作一样  等价于新建一个数组
void  reverse_string(char * s)  
{  
    char temp;    //交换用
    char*	p=s;  //给p赋初值
 
    while(*p) p++;  //让p指向最后一个字符 
    p--;    //保留最后一位'\0'
    
    while(s<=p)     //？？s<=p很精髓
    {  
        SWAP(*s++,*p--,temp);    //交换两个字符，宏函数实现  
    }  
} 
```
在此输入正文




