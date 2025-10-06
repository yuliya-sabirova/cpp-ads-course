---
jupytext:
  formats: md:myst
kernelspec:
  name: xcpp17
  display_name: C++17
myst:
  enable_extensions:
    - colon_fence
---

# Введение: вывод и базовые конструкции

Ниже — исполняемая ячейка C++ (нажмите **Live Code** → **Run**):

```{code-cell} cpp
#include <bits/stdc++.h>
using namespace std;

cout << "Hello, DS&A!\n";
vector<int> a = {1, 2, 3};
cout << accumulate(a.begin(), a.end(), 0) << "\n";
```

Ещё одна ячейка — поэкспериментируйте:

```{code-cell} cpp
vector<int> b = {10, 20, 30, 40};
cout << "size=" << b.size() << ", back=" << b.back() << "\n";
```
