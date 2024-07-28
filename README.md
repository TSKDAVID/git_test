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


N5:

```cpp


#include <iostream>
#include <algorithm>
#include <vector>

using namespace std;


void sortedVector(vector<int>& nums){
    sort(nums.begin(), nums.end());
}

int main() {

vector <int> nums = {5,2,3,6,9,1,2,111,4};
cout<< "unsorted vector: ";
for (int num: nums)
    cout<<num<<" ";
sortedVector(nums);
cout<<"sorted vector: ";
for (int num:nums)
    cout<< num<< " ";
return 0;
}



```


N6:

```cpp
#include <iostream>
#include <algorithm>
#include <vector>

using namespace std;


int rekursia(int ricxvi, int xarisxi){
    return (xarisxi==0)?1: ricxvi * rekursia(ricxvi, xarisxi- 1);
}


int main() {
int ricxvi = 5;
int xarisxi = 4;

int pasuxi=rekursia(ricxvi,xarisxi);
cout<< ricxvi<< " ayvanili "<<xarisxi <<" xarisxshi, udris "<< pasuxi<< " -s";
return 0;
}



```

N7:

```cpp

#include <iostream>
#include <algorithm>
#include <vector>

using namespace std;

int main() {
vector <int> numbers = {1,2,3,4,5,6,7,8,9,10,11,12};
cout<<"vectori washlamde: ";
for (int num: numbers)
    cout<<num<< " ";

numbers.erase(numbers.begin() + 5, numbers.begin() + 10);
cout<<endl<<"vectori washlis shemdeg: ";
for (int num:numbers)
    cout<<num<<" ";
}

```

N8:

#include <iostream>
#include <fstream>
#include <vector>

using namespace std;

int main() {
    ifstream inputFile("numbers.txt");
    vector<int> numbers;
    int num;
    while (inputFile >> num) {
        numbers.push_back(num);
    }

    inputFile.close();

    bool isSorted = true;
    for (int i = 0; i < numbers.size() - 1; i++) {
        if (numbers[i] > numbers[i + 1]) {
            isSorted = false;
            break;
        }
    }

    if (isSorted) {
        cout << "The numbers are sorted in ascending order." << endl;
    } else {
        cout << "The numbers are not sorted in ascending order." << endl;
    }

    return 0;
}

```
