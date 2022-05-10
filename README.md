# lagou-edu-101-datastructure
185_重学数据结构与算法



[MinGW-w64 离线包安装方法](https://blog.csdn.net/weixin_36466834/article/details/119569365)

[MinGW-w64离线安装，测试可用](https://blog.csdn.net/ZHAOJUNWEI08/article/details/86602120)



[Clion的安装和配置（C/C++开发神器）](https://blog.csdn.net/qq_44723773/article/details/104698675)

[windows上安装CLion教程及简单使用](https://www.cnblogs.com/attentle/p/12652512.html)



```c++
#include <iostream>

using namespace std;

/**
 * 自动数字类
 */
class Auto_arr {
public:
    // 构造函数
    Auto_arr(int length = 0);

    // 析构函数
    ~Auto_arr();

    int &operator[](int i);

    const int &operator[](int i) const;

    // 显示
    void display(int b);

    // 获取length
    int getLength();


private: // 私有属性
    // 长度
    int length;
    // 数组
    int *ptr_arr;

};

Auto_arr::Auto_arr(int length) {
    this->length = length;
    ptr_arr = new int[length];
}

Auto_arr::~Auto_arr() {
    delete[] ptr_arr;
}

/**
 * 取值
 * @param i
 * @return
 */
int &Auto_arr::operator[](int i) {
    return ptr_arr[i];
}

const int &Auto_arr::operator[](int i) const {
    return ptr_arr[i];
}

/**
 * 显示方法
 * @param b
 */
void Auto_arr::display(int b) {
    cout << ptr_arr[b];
}

/**
 * 获取长度
 */
int Auto_arr::getLength() {
    return length;
}

int main() {
    // 构造长度为10的数组
    Auto_arr A(10);
    // 打印类的sizeof 参考：https://www.cnblogs.com/huolong-blog/p/7587711.html
    cout << sizeof(Auto_arr) << endl;
    // 打印length
    cout << A.getLength() << endl;
    // 设置A[5]的值
    A[5] = 5;
    // 打印A[5]
    A.display(5);
    // 暂停
    system("pause");
    return 0;
}



```

