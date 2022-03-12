## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/pasodouble/pasodouble.github.io/edit/main/index.md) to maintain and preview the content for your website in Markdown files.

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/pasodouble/pasodouble.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.

# c++基本语法 
## 类定义 _蓝图_
```cpp
class classname //class 为关键字 classname为类名
{
  Access specifiers: //访问修饰符(类成员的访问属性）：public_公共成员在类的外部可访问_private/protected
  Date members/variables;  //变量
  Member functions(){}     //方法
}
```
## 对象
```cpp
classname obj1;
classname obj2;
```

## 访问数据成员 _使用访问运算符.访问类的对象的公共数据成员_
```cpp
obj1.Data members/variables=sth1;
obj2.Data members/variables=sth2;
```
### 实例代码（助于理解）
```cpp
#include <iostream>
using namespace std;

class Box
{
 public:
 double length;
 double breadth;
 double height;
 //成员函数声明
 double get(void);
 void set(double len,double bre,double hei);
};

//成员函数定义
double Box::get(void) //::域解析操作符，指明get(void)函数使用的命名空间是Box
{
 return length * breadth * height;
}

void Box::set(double len,double bre,double hei)
{ length = len;
  breadth = bre;
  height = hei;
}


int main()
{
Box Box1; //声明Box1,类型为Box
Box Box2;h
Box Box3;
double volume = 0.0;//用于存储体积

//box 1 详述 访问数据成员
Box1.height = 5.0；
Box1.length = 6.0;
Box1.breath = 7.0;

//box 2 详述 访问数据成员
Box2.height = 10.0；
Box2.length = 12.0;
Box2.breath = 13.0;

//box1的体积
volume = Box1.height*Box1.length*Box1.breadth;
cout<<"Box1的体积："<<volume<<end1;

//box2的体积
volume = Box2.height*Box2.length*Box2.breadth;
cout<<"Box2的体积："<<volume<<end1;

//box3 详述
Box3.set(16.0,8.0,12.0);
volume = Box3.get();
cout << "Box3 的体积： "<<volume<<end1;
return 0;
}
```
`Box1 的体积： 210`
`Box2 的体积： 1560`
`Box3 的体积： 1536`
## hello world程序
```cpp
#include <iostream> //定义头文件
using namespace std; //告知编译器使用std命名空间_防止redefination_
int main() 
{
 cout<<"Hello World"; //显示"Hello World"
 return 0;
 }
```
[代码块](urlhttps://docs.github.com/cn/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/about-writing-and-formatting-on-github#enabling-fixed-width-fonts-in-the-editor)

## c++标识符 _标识变量/函数/类/模块/其他用户自定义项目的名称（区分大小写）_
## 关键字 [关键字完整介绍](urlhttps://www.runoob.com/w3cnote/cpp-keyword-intro.html)

# c++继承
_当创建一个类（派生类）时，不需要重新编写新的数据成员和成员函数，只需要指定派生类继承基类_

代码如下
```cpp
class Animal{

}

class Dog : public Animal {

};
```
```cpp
#include <iostream>
using namespace std;
//基类
class Shape
{
  public:
  void setWidth(int w)
  { 
    width = w;
  }
  
  void setHeight(int h)
  {
  height = h;
  }
  protected: //自身/子类/父类
  int width;
  int height;
}


```
