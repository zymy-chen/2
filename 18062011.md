#### **2.23**

###### 不可以，指针是否有效还不知道。

#### **2.24**

###### 因为lp的类型不是int，而void定义了一个空指针，可以接受任何对象。

#### **2.25**

###### （a） ip是一个int类指针型的，i是一个int型的变量，r是一个int型的引用。

###### （b） i是一个int型的变量，ip是一个空指针。

###### （c） ip是一个int类型的指针，ip2是一个int类型的变量。



####   **2.35**

###### 第一个auto j 类型为int。

###### 第二个 auto &k 为 const int &。

###### 第三个 auto *p类型为const int *。

###### 第四个 auto j2类型为const int。

###### 第五个 auto &k2类型为const int &。

#### **3.4**

###### #include <iostream>

###### #include <string>

###### using namespace std;

###### void main()

###### {	

###### 	string m1 , m2;

###### 	cin>>m1>>m2;

###### 	if (m1 != m2)

###### 	{

###### 		cout<<(m1 >= m2 ? m1 : m2)<<endl;

###### 	}

###### 	return 0;

###### }

###### 改写后：

###### #include <iostream>

###### #include <string>

###### using namespace std;

###### void main()

###### {	

###### 	string m1 , m2;

###### 	cin>>m1>>m2;

###### 	if (m1.size() != m2.size())

###### 	{

###### 		cout<<(m1.size() >= m2.size() ? m1 : m2)<<endl;

###### 	}

###### 	else

###### 	{

###### 		cout<<" same"<<endl;

###### 	}	

###### 	return 0；

###### }

#### **3.5**

###### #include <iostream>

###### #include <string>

###### using namespace std;

###### void main()

###### {	

###### 	string m;

###### 	string s;

###### 	while (getline(cin ,m))

###### 	{

###### 		s+= m;	#(修改的话 后边加  +" ")

###### 		cout<<s<<endl;

###### 	}

###### 	return 0;

###### }

#### **3.20**

###### #include <iostream>

###### #include <string>

###### #include <vector>

###### using namespace std;

###### void main()

###### {	

###### 	vector<int> My_vector;

###### 	int a[10];

###### 	for (int i = 0;i<10;i++)

###### 	{

###### 		cin>>a[i];

###### 	}

###### 	for (int j = 0;j<10;j++)

###### 	{

###### 		My_vector.push_back(a[j]);

###### 	}

###### 	int sum[10];

###### 	for (int k = 0;k<10;k++)

###### 	{

###### 		sum[k] = My_vector[k] + My_vector[k+1];

###### 		cout<<sum[k]<<endl;

###### 		k++;

###### 	}

###### }

###### 修改后：

###### #include <iostream>

###### #include <string>

###### #include <vector>

###### using namespace std;

###### void main()

###### {	

###### 	vector<int> My_vector;

###### 	int a[10];

###### 	for (int i = 0;i<10;i++)

###### 	{

###### 		cin>>a[i];

###### 	}

###### 	for (int j = 0;j<10;j++)

###### 	{

###### 		My_vector.push_back(a[j]);

###### 	}

###### 	int sum[10];

###### 	for (int k = 0;k<5;k++)

###### 	{

###### 		sum[k] = My_vector[k] + My_vector[9-k];

###### 		cout<<sum[k]<<endl;

###### 	}

###### } 

#### **3.23**

###### #include <iostream>

###### #include <string>

###### #include <vector>

###### using namespace std;

###### void main()

###### {	

###### 	vector<int> text(10,5);

###### 	for (auto it = text.begin(); it != text.end();it++) 

###### 	{

###### 		*it = *it * 2;

###### 		cout<<*it<<endl;	

###### 	}

###### }

#### **6.16**

###### 加上const 表示常量引用。

#### **6.19**

###### （a） 函数只有一个，传入两个不合法

###### （b） 合法

###### （c） 合法

###### （d） 合法

#### **6.30**

###### 返回类型必须与函数类型相同

#### **7.16**

###### public 后定义需要控制类的相关操作一类成员的初始化、拷贝、赋值。

###### private隐藏类的相关实现细节，实现封装。

#### **7.24**

###### Screen() = default; 

###### Screen(pos ht, pos wd) : height(ht), width(wd), contents(ht * wd, ' ') {} 

###### Screen(pos ht, pos wd, char c) : height(ht), width(wd), contents(ht * wd, c)

###### {

###### } 

#### **7.49**

###### (a)合法

###### (b)不合法，Salesdata&类型与Salesdata类型之间不可转换

###### (c)不合法，const不对，因为combine本身是需要改变传入参数的

#### **7.58**

###### rate可以不要申明为const

