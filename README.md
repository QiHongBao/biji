# biji
课堂笔记
博客园首页新随笔联系管理订阅
随笔- 4  文章- 0  评论- 0 
java中的一些规则（菜鸟的课堂笔记）
ls 查看目录下文件
java规则
代码都定义在类中，用class定义
禁止一个源文件写两个类；
一个源文件中，只能有一个类文件是pubic；
一个源文件中如果有多个类，编译完之后会产生多个class文件
类名开头必须大写
语句要写在方法体里
严格区分大小写
注释 // /* */ /** */
java关键字
abstract	do	implement	private	this
boolean	double	import	protected	throw
break	else	instanceof	public	throws
byte	extends	int	return	transient
case	false	interface	short	true
catch	final	long	static	try
char	fianlly	native	strictfp	void
class	float	new	super	volatile
continue	for	null	switch	while
default	if	package	enum	synchronized
assert	 	 	 	 
变量的概念：
占据着内存中的某一个存储区域;
该区域有自己的名称（变量名）和类型（数据类型）;
该区域的数据可以在同一类型范围内不断变化;
为什么要定义变量：
用来不断的存放同一类型的常量，并可以重复使用；
使用变量注意：
变量的作用范围, 初始化值
定义变量的格式：
数据类型 变量名 = 初始化值；
注：格式是固定的，记住格式，以不变应万变。
作用范围：定义开始到定义它的代码块结束;
同一范围内，不允许多个个局部变量命名冲突
 
局部变量：不是声明在类体括号里面的变量；
局部变量使用前必须初始化值;
局部变量没有默认初始化值;
局部变量的作用域是从定义开始到定义它的代码块结束;
 
成员变量:在方法体外,类体内声明的变量，又称字段(Field)或全局变量；
成员变量的作用域是整个类中;
java采用unicode编码可以存放中文
输入语句
static Scanner sc = new Scanner(System.in);
int *** = **.nextInt();
输出语句
System.out.print();
导包的语句
import java.util.*;
输入后接受字符串的语句
String *** = **.next();
定义方法的语句
private static void ***（int**，int**）；
将字符串转化成数组
char[] a = n.toCharArray();
 
方法的重载 》》》
方法的签名：
判别方法的唯一性包括：方法名和参数列表
（参数的顺序也是关键）；
return之后写东西没意义；
一个类中允许存在一个以上的同名方法；
 
局部变量必须先初始化在使用
 
NullPointerException 空引用异常；
今天做几个基础程序  99乘法表：
 
public class chengfa{
　　public static void main(String[] args){
　　　　int i,j;
　　　　for(i=1;i<=9;i++){
　　　　　　for(j=1;j<=i;j++){
　　　　　　　　System.out.print(j+"*"+i+"="+j*i+"\t");
　　　　　　}
　　　　　　System.out.println("\n");
　　　　}
　　}
}

以及冒泡排序：

import java.util.*;
public class Maopao{
　　public static void main(String[] args){
　　　　int a[] = new int[5];
　　　　System.out.println("请输入5个数来进行冒泡排序");
　　　　for(int i=0;i<5;i++){
　　　　　　System.out.println("下面请输入第"+(i+1)+"个数");
　　　　　　Scanner sc = new Scanner(System.in);
　　　　　　a[i] = sc.nextInt();
　　　　}
　　　　for(int i=0;i<4;i++){
　　　　　　for(int j=i;j<5;j++){
　　　　　　　　if(a[i]>a[j]){
　　　　　　　　　　int b = a[i];
　　　　　　　　　　a[i] = a[j];
　　　　　　　　　　a[j] = b;
　　　　　　　　}
　　　　　　}
　　　　}
　　　　System.out.println("排序结果为");
　　　　for(int j=0;j<5;j++){
　　　　　　System.out.println(a[j]); 
　　　　}
　　}
}
