# 🎮 C++ 控制语句详解：成为程序的指挥家！

控制语句是编程中至关重要的结构，它们决定了程序的执行路径，就像导演指挥演员一样！下面我们将全面学习 C++ 中的控制语句：

---

## 🚦 条件语句：程序的选择题

### 1️⃣ `if` 基础判断
```cpp
if (条件) {
    // 条件为真时执行的代码
}

// 📝 示例：检测成绩是否及格
int score = 75;
if (score >= 60) {
    cout << "恭喜及格！🎉";
}
```

### 2️⃣ `if-else` 二选一
```cpp
if (条件) {
    // 条件为真执行
} else {
    // 条件为假执行
}

// 🎥 实用案例：判断奇偶数
int num = 7;
if (num % 2 == 0) {
    cout << "偶数";
} else {
    cout << "奇数";  // 执行这里
}
```

### 3️⃣ `else if` 多重选择
```cpp
if (条件1) {
    // 代码块1
} else if (条件2) {
    // 代码块2
} else {
    // 默认代码块
}

// 🌈 分段评级系统示例
int grade = 85;
if (grade >= 90) {
    cout << "A+";
} else if (grade >= 80) {  // 本条件触发
    cout << "A"; 
} else {
    cout << "再接再厉";
}
```

---

## 🔁 循环语句：重复执行的艺术

### 🔄 `for` 循环（精确控制次数）
```cpp
for(初始化; 条件; 更新) {
    // 循环体
}

// 🚀 发射倒计时案例
for(int i=10; i>0; i--) {
    cout << i << "秒后发射！\n";
}
cout << "点火升空！🚀";
```

### 🕰️ `while` 循环（条件优先）
```cpp
while(条件) {
    // 循环体
}

// 🍪 吃饼干直到饱腹感达标
int fullness = 0;
while(fullness < 100) {
    cout << "吃掉一块饼干🍪\n";
    fullness += 30;  // 三次后结束
}
```

### 🎡 `do...while` 循环（先执行后判断）
```cpp
do {
    // 循环体（至少执行一次）
} while(条件);

// 🤑 银行至少操作一次的案例
int balance = 500;
do {
    cout << "当前余额：" << balance << "\n";
    balance -= 100;
} while(balance > 600);  // 判断时已减到400
```

---

## ⚡ 循环控制指令：精准操控循环流

### 🛑 `break`——紧急刹车
```cpp
for(int i=1; i<=10; i++) {
    if(i == 5) {
        break;  // 立即终止循环
    }
    cout << i << " ";  // 输出：1 2 3 4
}
```

### ⏭️ `continue`——跳过当前
```cpp
for(int i=1; i<=5; i++) {
    if(i == 3) {
        continue;  // 跳过本次循环
    }
    cout << i << " ";  // 输出：1 2 4 5 
}
```

---

## 🧩 综合应用案例：智能售货机
```cpp
#include <iostream>
using namespace std;

int main() {
    int money = 10;
    char choice;
    
    while(true) {
        cout << "\n可选饮料：\n1. 可乐(3元)\n2. 果汁(5元)\nQ. 退出\n";
        cin >> choice;
        
        if(choice == 'Q') {
            break;  // 退出循环
        }
        
        if(choice == '1') {
            if(money >= 3) {
                cout << "可乐已出货 🥤";
                money -= 3;
            } else {
                cout << "余额不足！";
            }
        } else if(choice == '2') {
            if(money >= 5) {
                cout << "果汁已出货 🧃";
                money -= 5;
            } else {
                cout << "余额不足！";
            }
        } else {
            cout << "无效选项！";
            continue;  // 跳过本次循环
        }
        
        cout << "\n剩余金额：" << money << "元\n";
    }
    
    return 0;
}
```

---

## 📌 关键要点总结

| 结构类型 | 应用场景 | 注意事项 |
|----------|-----------|-----------|
| `if-else` | 分支选择 | 使用 `else if` 处理多条件 |
| `for` | 已知循环次数 | 避免修改循环变量导致失控 |
| `while` | 条件触发循环 | 注意设置终止条件防死循环 |
| `do...while` | 至少执行一次 | 末尾分号不能忘 |
| `break/continue` | 精细控制循环流程 | `break` 跳出整个循环 |

### 💡 运行小贴士：
可以通过调试工具逐步执行代码，直观观察控制流的变化！

希望这能帮助你更好地理解和实践C++编程的基础知识，并享受编程的乐趣！
