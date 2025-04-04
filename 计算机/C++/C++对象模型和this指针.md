## 1.成员变量和成员函数分开存储
在c++中，类内的成员变量和成员函数分开存储
只有非静态成员变量才属于类的对象上

*空对象占用内存空间为：1*
*C++编译器会给每个空对象也分配一个字节空间，是为了区分空对象占内存的位置*

## 2.this指针概念
通过1我们知道在C++中成员变量和成员函数是分开存储的
每一个非静态成员数只会诞生一份函数实例，也就是说多个同类型的对象会共用一块代码
那么问颗是：这一块代码是如何区分哪个对象调用自己的呢？

c++通过提供特殊的对象指针，this指针，解决上述问题。**this指针指向被调用的成员函数所属的对象**

this指针是隐含每一个非静态成员函数内的一种指针
this指针不需要定义，直接使用即可

this指针的用途：
- 当形参和成员变呈同名时，可用this指针来区分
- 在类的非静态成员函数中返回对象本身，可便用return\*this

```cpp
#include <iostream>
using namespace std;

class Person {
public:
    Person(int age) {
      //this指针指向 被调用的成员函数 所属的对象
      this->age = age;
    }
    Person& PersonAddAge(Person& p) {
        this->age += p.age;
        // 返回对象本身
        return *this;
    }
    int age;
};
//1 解决名称冲突问题
void test01() {
    Person p1(10);
    cout << "p1的年龄 = " << p1.age << endl;

}
//2 返回对象本身用*this
void test02() {
    Person p1(12);
    Person p2(12);
    p2.PersonAddAge(p1).PersonAddAge(p1);
    cout << "p2的年龄 = " << p2.age << endl;
}
int main() {
    test02();
    system("pause");
    return 0;
}
```

## 3.空指针访问成员函数
C++中空指针也是可以调用成员函数，但是要注意有没有用到this指针
如果用到this指针，需要加以判断保证代码的健壮性

## 4.const修饰成员函数
**常函数：**
- 成员函数后加 const 后我们称为这个函数为**常函数**
- 常函数内不可以修改成员属性
- 成员属性声明时加关键字mutable后，在常函数中依然可以修改

**常对象：**
- 声明对象前加const称该对象为常对象
- 常对象只能调用常函数
```cpp
#include <iostream>
using namespace std;
//常函数
class Person {
public:
    //this指针的本质：是一个指针常量 指针的指向不能修改
    void showPerson() const {
        //this->age = 10;
        this->high = 180;
        cout << "age = " << this->age << endl;
    }
    int age;
    mutable int high;//特殊变量，即使在常函数中，也可以修改
};
//常对象
void test01() {
    const Person p;
    //p.age = 10;
    p.high = 180;
    //常对象只能调用常函数
    p.showPerson();
}
int main() {
    system("pause");
    return 0;
}
```