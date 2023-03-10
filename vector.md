# C++ Vector Methods

###vector::size(): Returns the number of elements in the vector.

```c++
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    cout << vec.size() << endl; // output: 3
    return 0;
}
```

### vector::push_back(): Adds an element to the end of the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.push_back(40);
    for (int i : vec) {
        cout << i << " "; // output: 10 20 30 40
    }
    return 0;
}
```

### vector::pop_back(): Removes the last element from the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.pop_back();
    for (int i : vec) {
        cout << i << " "; // output: 10 20
    }
    return 0;
}
```

### vector::clear(): Removes all elements from the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.clear();
    cout << vec.size() << endl; // output: 0
    return 0;
}
```

### vector::empty(): Returns true if the vector is empty, false otherwise.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    cout << vec.empty() << endl; // output: 0 (false)
    vec.clear();
    cout << vec.empty() << endl; // output: 1 (true)
    return 0;
}
```

### vector::resize(): Changes the size of the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.resize(5);
    for (int i : vec) {
        cout << i << " "; // output: 10 20 30 0 0
    }
    vec.resize(2);
    for (int i : vec) {
        cout << i << " "; // output: 10 20
    }
    return 0;
}
```

### vector::erase(): Removes an element or a range of elements from the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30, 40, 50 };
    vec.erase(vec.begin() + 1);
    for (int i : vec) {
        cout << i << " "; // output: 10 30 40 50
    }
    vec.erase(vec.begin() + 2, vec.end());
    for (int i : vec) {
        cout << i << " "; // output: 10 30
    }
    return 0;
}
```

### vector::insert(): Inserts an element or a range of elements into the vector at a specified position.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.insert(vec.begin() + 1, 15);
    for (int i : vec) {
        cout << i << " "; // output: 10 15 20 30
    }
    vector<int> to_insert{ 40, 50 };
    vec.insert(vec.end(), to_insert.begin(), to_insert.end());
    for (int i : vec) {
        cout << i << " "; // output: 10 15 20 30 40 50
    }
    return 0;
}
```

### vector::assign(): Replaces the elements in the vector with a specified number of elements, or a range of elements.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    vec.assign(2, 5);
    for (int i : vec) {
        cout << i << " "; // output: 5 5
    }
    vector<int> to_assign{ 1, 2, 3 };
    vec.assign(to_assign.begin(), to_assign.end());
    for (int i : vec) {
        cout << i << " "; // output: 1 2 3
    }
    return 0;
}
```

### vector::swap(): Swaps the contents of two vectors.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec1{ 10, 20, 30 };
    vector<int> vec2{ 40, 50 };
    vec1.swap(vec2);
    for (int i : vec1) {
        cout << i << " "; // output: 40 50
    }
    for (int i : vec2) {
        cout << i << " "; // output: 10 20 30
    }
    return 0;
}
```

### vector::front(): Returns the first element of the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    cout << vec.front() << endl; // output: 10
    return 0;
}
```

### vector::back(): Returns the last element of the vector.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    cout << vec.back() << endl; // output: 30
    return 0;
}
```

### vector::at(): Returns the element at a specified position in the vector. Throws an out_of_range exception if the position is out of bounds.

```c++

#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> vec{ 10, 20, 30 };
    cout << vec.at(1) << endl; // output: 20
    try {
        cout << vec.at(3) << endl; // throws out_of_range exception
    }
    catch (const out_of_range& e) {
        cout << e.what() << endl; // output: vector::_M_range_check: __n (which is 3) >= this->size() (which is 3
```
