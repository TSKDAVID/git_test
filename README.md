N1:


```cpp
#include <iostream>
#include <string>
#include <vector>
#include <utility>
#include <algorithm>

using namespace std;

void dalageba_anb(vector<pair<string, int>>& studentebi) {
    sort(studentebi.begin(), studentebi.end(), [](const pair<string, int> &a, const pair<string, int> &b) {
        return a.first < b.first;
    });
}

int main() {
    vector<pair<string, int>> studentebi;

    studentebi.push_back(make_pair("tskabelia", 20));
    studentebi.push_back(make_pair("gelitashvili", 20));
    studentebi.push_back(make_pair("amiranashvili", 18));
    studentebi.push_back(make_pair("beraia", 28));

    dalageba_anb(studentebi);

    for (const auto& student : studentebi) {
        cout << student.first << " " << student.second << endl;
    }

    return 0;
}
```


N2:

```cpp
