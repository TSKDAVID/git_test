N2:


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


N3:

```cpp
#include <iostream>
#include <vector>


using namespace std;


int main() {
    vector<int> nums= {1, 2, 3, 4, 5,6,12,14,18};
    for (int num : nums){
        if(num%6==0)
        cout<<num<<endl;
    }
    
    
    return 0;
}
```

N4:

```cpp
#include <iostream>
#include <cmath>

using namespace std;

struct Point {
    double x;
    double y;
    double z;
};

struct Sphere {
    Point center; 
    double radius;
};
bool isinsphere(const Point& p, const Sphere& sphere) {
    double distance = sqrt(pow(p.x - sphere.center.x, 2) +
                           pow(p.y - sphere.center.y, 2) +
                           pow(p.z - sphere.center.z, 2));
    return distance <= sphere.radius;
}

int main() {
    Point point = {2, 3, 4};
    Sphere sphere = {{1, 2, 3}, 3};

    if (isinsphere(point, sphere)) {
        cout << "The point is inside the sphere." << endl;
    } else {
        cout << "The point is not inside the sphere." << endl;
    }

    return 0;
}


```

