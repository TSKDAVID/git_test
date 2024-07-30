N1:
მთავარ ფუნქციაში:
1.  შემოვიტანოთ ცვლადი მასივის ზომისთვის
2. შემოვიტანოთ მასივი და შევავსოთ მთელი რიცხვებით
3. შევქმნათ ცვლადი რომელიც გამოიძახებს ფუნქციას, ეს ფუნქცია დაადგენს რომელი მთელი რიცხვია მაქსიმალური, რეკურსიის მეშვეობით, და გადავცეთ მას მასივი და მისი ზომა პარამეტრების სახით

მთავარი ფუნქციის გარეთ:

5. შევადგინოთ ფუნქცია რომელიც მიიღებს 2 პატამეტრს, მასივს და მასივის ზომას
    ```cpp
    int maxnum(int arr[],int size)
    ```
5. დავწეროთ ლოგიკური ოპერატორი რომელიც ხელს შეუშლის ფუნქციას უსასრულოდ განმეორებაში და დააბრუნებს მასივში დარჩენილ პირველ ელემენტს
    ```cpp
    if (size ==1)
   return arr[0];
   ```
6. შევქმნათ ცვლადი რომელიც გამოიძახებს იგივე ფუნქციას, მასივის პირველი ელემენტის ინდექს მიუმატებს 1-ს და მასივის ზომას გამოაკლებს ასევე 1-ს
   
   ```cpp
   int maximum = maxnum(arr+1,size-1);
   ```
8. დავწეროთ return მეთოდი რომელიც შეადარებს მასივის პირველ ელემენტს ცვლადს maxnum-ს და დააბრუნებს მასივის პირველ ელემენტს თუ კი ეს ელემენტი maxnum-ზე მეტი იქნება, სხვა შემთხვევაში უბრალოდ maxnums-ს

    ```cpp
   return (arr[0]>maximum)?arr[0]:maximum;
   ```
10. საბოლოოდ როცა ზომა მიაღწევს 1-ს ფუნქცია დააბრუნებს ბოლო ელემენტს რომელიც მასივში დარჩენილი იქნება, და რეკურსიულად გამოძახებული ფუნქციის ჯაჭვი შეადარებს თითოეულ ელემენტს ერთმანეთთან და საბოლოოდ მხოლოდ დარჩება მხოლოდ მაქსიმალური ელემენტი

11. მთავარ ფუნქციაში გამოვიტანოთ მაქსიმალური ელემენტი

N2:

1.შევქმნათ bool ტიპის ფუნქცია რომელიც მიიღებს პარამეტრებს: მასივი, რიგების და სვეტების რაოდენობა
    
 ```cpp
    bool  samkutxa(int arr[][...],int row, int col)
 ```
2. შემოვიტანოთ bool ტიპის ცვლადი 
 
    ```cpp
    bool triangle = false;
    ```
3. შევქმნათ ციკლი რომელიც გაივლის ამ მასივის ყველა ელემენტს ორივე განზომილებაში

   ```cpp
    for (int i=0; i<row;i++)
        for(int j=0;j<col;j++)
    ```
5. თითოეული ელემენტის გავლისას შევამოწმოთ 2 რამ, არის თუ არა j<i, თუ ასეა იმ შემთხვევაში თუ რომელიმე ელემენტი რომელიც ამას აკმაყოფილებს არ იქნება 0 ამ შემთხვევაში triangle=true, ხოლო თუ j>i ზე მაგრამ რომელიმე მათგანი არ იქნება 0 მაშინ პირდაპირ ვაბრუნებთ false

     ```cpp
    if(j<i&& arr[i][j] !=0)
        triangle=true;
    if(j>i && arr[i][j] !=0)
        returnfalse;
    ```
7. თუ ზემოთ მოცემულმა კოდმა არაფერი დააბრუნა ნიშნავს რომ ყველა მოთხოვნა დაკმაყოფილებულია და ფუნქციამ უნდა დააბრუნოს true

    ```cpp
    return true;
    ```

N4:

1. შევქმნათ void ტიპის ფუნქცია: void printunique().
   
2. დავწეროთ ციკლი რომელიც ყველა ელემენტს გაივლის 100 დან 999 ის ჩათვლით

    ```cpp
    for (int num = 100; num<=999;num++){
    }
    ```
3. ამავე ციკლში შევქმნათ 3 ცვლადი, int unit = num,ten = num, hundred

4. დავწეროთ ციკლი რომელიც მოგვცემს ამ რიცხვის ერთეულის პოზიციაზე არსებულ ციფრს,რომელიც შეგვიძლია მივიღოთ ამ რიცხვისთვის 10 ის გამოკლებით მანამ სანამ unit>=10:

     ```cpp
    while (unit >=10)
        unit -=10;
     ```
5. შევქმნათ მსგავსი ციკლი ათეულების პოზიციაზე არსებული ციფრის გასაგებად, რომელიც ამ რიცხვზე 100 ის გამოკლებით მიიღება სანამ ten>=100 , ten -=unit და ბოლოს რადგან / და % მეთოდის გამოყენება არ არის დაშვებული ten = ten* 0.1:
 
   ```cpp
   while (ten>=100)
       ten -=100;
   ten -= unit;
   ten = ten * 0.1;
   ```
6. ასეულების პოზიციის ციფრის გასაგებად კი შეგვიძლია პირდაპირ გამოვთვალოთ: hundred = (num - (tens + units))* 0.01, მსგავსად თუ ასეულ რიცხვს რომელიც არ შეიცავს ათეულებს ან ერთეულებს გავამრავლებთ 0.01 ზე იგივეა რაც 100 ზე გაყოფა, რითიც მივიღებთ ასეულის პოზიციაზე არსებულ ციფრს.

7. და ბოლოს დავწეროთ ლოგიკური ოპერატორი რომელიც შეამოწმებს, ათობით წარმოდგენის ციფრი ემთხვევა თუ არა სხვა რომელიმე ციფრს ამ რიცხვში, ეს ყველაფერი კი ციკლშია მოქცეული რომელიც ყველა რიცხვს გაივლის ამიტომ შეგვიძლია მაშინვე დავბეჭდოთ ეს რიცხვი:
    ```cpp
    if (tens != hundreds && tens != units){
    cout<< num << " ";
    }
    ```


N5:



1.მთავარ ფუნქციაში შემოვიტანოთ მასივის ზომა და მასივი
 
 ```cpp
    int size;
    cin>> size;
    int arr[size];
 ```
2. შევავსოთ მასივი ელემენტებით:

 ```cpp
    for (int i=0; i<size;i++)
        cin>>arr[i];
 ```
3. შევქმნათ ცვლადი და მივანიჭოთ ფუნქციის მნიშვნელობა:

```cpp
    int result = aritm(arr,size);
```
4.შევქმნათ ფუნქცია რომელიც გამოითვლის საშუალო არითმეტიკულს 00 ზე დაბოლოვებული ელემენტებისთვის
    ```cpp
    int aritm(int arr[],int size)
    ```

5. შემოვიტანოთ 2 ცვლადი რომელიც საჭირო ელემენტთა ჯამს და რაოდენობას დაითვლის:

       ```cpp
       int jami=0,raod=0;
        ```
7. დავწეროთ ციკლი რომელიც გაივლის ყველა ელემენტს ამ მასივში და შეამოწმებს მთავრდება თუ არა 00 ზე

   ```cpp
      for (int i =0;i<size;i++){
      if (arr[i]%100 == 00){
          jami +=arr[i];
          raod ++;
      }}
   ```
8. შევამოწმოთ იყო თუ არა საერთოდ მსგავსი ელემენტი მასივში,თუ არა დავაბრუნოთ 0:

    ```cpp
    if (raod ==0){
        return 0;
    }
     ```

9. თუ მსგავსი ელემენტი მოიძებნა დავაბრუნოთ მისი ან მათი საშუალო არითმეტიკული:

   ```cpp
   return static_cast<float>(jami) / raod;
   ```



    

N7:

1. მთავრ ფუნქციაში შემოვიტანოთ ცვლადი int ricxvi; cin>> ricxvi;

2. გამოვიძახოთ ფუნქცია რომელიც გამოითვლის 1 დან ამ რიცხვამდე ლუწი ელემენტების ნამრავლს int namr = product(ricxvi);

3. შევქმნათ int ტიპის ფუნქცია  int product(int n) რომელიც პარამეტრად მთელ რიცხვს მიიღებს

4. დავწეროთ ლოგიკური ოპერატორი რომელიც იმოქმედებს საბოლოოდ როცა რეკურსიის შემდეგ n გახდება 0 ან 0 ზე ნაკლები

    ```cpp
   if(n <=0){
   return 1;}
    ```
5.  დავწეროთ ლოგიკური ოპერატორი რომელიც შეამოწმებს ამჟამინდელი n ის მნიშვნელობა ლუწია თუ არა, იმ შემთხვევაში თუ ლუწია ვიყენებთ რეკურსიას ამავე ფუნქციის გამოძახებით product(n-2) მნიშვნელობით,თუ კი n ლუწი არ აღმოჩნა კვლავ რეკურსიას მივმართავთ product(n-1) რათა ლუწ რიცხვამდე მისვლა შევძლოთ:

    ```cpp
         if(n % 2 ==0){
             return n* product(n-2);
         }else{
             return product(n-1);
     }
7. ამგვარად ეს ფუნქცია გაივლის ყველა ელემენტს 1 დან მოცემულ რიცხვამდე, და ყველა ლუწ ელემენტს ამრავლებს ერთმანეთზე.

8. მთავარ ფუნქიცაში გამოვიტანოთ ნამრავლი.
         
   


N8:
Efficiency Comparison
Function 1:

Iterates from the start of the string to the midpoint.
Each iteration swaps characters from the beginning and end of the string moving towards the center.
The length of the string is accessed multiple times in each loop iteration (s.length()).
Function 2:

Also iterates from the start of the string to the midpoint.
Each iteration swaps characters from the beginning and end of the string moving towards the center.
The length of the string is accessed only once before the loop starts.





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
```cpp

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
