#### 题目：1kb的内存不够要改成2kb，如何将之前的1kb内容转到2kb去

###### char *ptr = new char[1000];

###### char *ptr1 = new char[2000];

###### memcpy(ptr1,prt,1000);

######  delete[] ptr;

###### 如果在vector向量中，要用push_back,确保在地址1000的东西是空

###### vector<char> ptr(1000);

###### vector<char>ptr1(2000);

###### for (auto &i : ptr)

###### 		ptr1.push_back(i);

