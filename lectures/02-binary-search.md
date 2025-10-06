### `lectures/02-binary-search.md` (страница с маленькими автотестами)
```md
---
kernelspec:
name: xcpp17
language: C++17
---


# Бинарный поиск (итеративный)


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


int main(){vector<int> v{1,3,5,7,9};
cout << binary_search_iter(v, 7) << "\n"; // ожидаем 3
}

#include <bits/stdc++.h>
using namespace std;


void check(bool cond, const string& msg){
cout << (cond ? "[OK] " : "[FAIL] ") << msg << "\n";
}


int binary_search_iter(const vector<int>&, int);


int main(){
vector<int> v{1,3,5,7,9};
check(binary_search_iter(v,1) == 0, "first element");
check(binary_search_iter(v,9) == 4, "last element");
check(binary_search_iter(v,6) == -1, "not found");
}


## 4) Сборка и локальный предпросмотр
```bash
# В корне репозитория
jupyter-book build .
# Готовый сайт появится в каталоге _build/html
python -m http.server -d _build/html # локально открыть в браузере
vector<int> v{1,3,5,7,9};
cout << binary_search_iter(v, 7) << "\n"; // ожидаем 3
}

vector<int> v{1,3,5,7,9};
cout << binary_search_iter(v, 7) << "\n";  // ожидаем 3


auto check = [](bool cond, const string& msg){
  cout << (cond ? "[OK] " : "[FAIL] ") << msg << "\n";
};

vector<int> v{1,3,5,7,9};
check(binary_search_iter(v,1) == 0,  "first element");
check(binary_search_iter(v,9) == 4,  "last element");
check(binary_search_iter(v,6) == -1, "not found");
