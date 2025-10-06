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

# Бинарный поиск (итеративный)

Определим функцию:

```{code-cell} cpp
#include <bits/stdc++.h>
using namespace std;

int binary_search_iter(const vector<int>& a, int x) {
  int l = 0, r = (int)a.size() - 1;
  while (l <= r) {
    int m = l + (r - l) / 2;
    if (a[m] == x) return m;
    if (a[m] < x) l = m + 1; else r = m - 1;
  }
  return -1;
}
```

Быстрая проверка:

```{code-cell} cpp
vector<int> v{1,3,5,7,9};
cout << binary_search_iter(v, 7) << "\n";  // ожидаем 3
```

Мини-тесты:

```{code-cell} cpp
auto check = [](bool cond, const string& msg){
  cout << (cond ? "[OK] " : "[FAIL] ") << msg << "\n";
};
vector<int> v{1,3,5,7,9};
check(binary_search_iter(v,1) == 0,  "first element");
check(binary_search_iter(v,9) == 4,  "last element");
check(binary_search_iter(v,6) == -1, "not found");
```
