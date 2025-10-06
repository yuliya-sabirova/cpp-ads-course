---
# Указываем ядро для Thebe на этой странице
kernelspec:
name: xcpp17
language: C++17
---


# Введение: вывод и базовые конструкции


Ниже — исполняемая ячейка C++ (нажмите Live Code → Run):


```{code-cell} cpp
#include <bits/stdc++.h>
using namespace std;


int main() {
cout << "Hello, DS&A!\\n";
vector<int> a = {1, 2, 3};
cout << accumulate(a.begin(), a.end(), 0) << "\\n";
}
