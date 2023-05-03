1.该系统包含一个目录，输入目录上的数字可以跳转各个功能，执行完目录重新输出，知道按7.结束进程为止。以while循环和switch实现

2.头文件部分（右）

3.因为要求每一个功能点通过一个函数实现。函数多数用得是void
 void ReadIn();
void SexJudge();
void MonJudge();
int PeopleNeeded(string);
void ChangeData();
void Addtudent();
void sort();

4.数据多以int 和string存储数据
 struct stu { 
	int id;
	string name;
	string sex;
	string pro;
	int birthyear;
	int birthmon;
	int birthday;
	int st;
};
stu stus[40];//结构体

5. 读入文档，此处分离了年月日，a安放“/”
ifstream file;//读入
	file.open("C:/Users/童殿/Desktop/Rosetta‘s stone/大学/计算机/作业/期末大作业/student.txt", ios::in);//它建立了file和文件的关系
	if (!file) cout << "检查输入是否正确";
	for (int i = 0; i < ruler; i++)//回车断行
	{
		file >> stus[i].id >> stus[i].name >> stus[i].sex >> stus[i].pro >> stus[i].birthyear >> a >> stus[i].birthmon >> a >> stus[i].birthday;
	} 
}

6. 性别查询会把所有stus[i].sex 对比一遍，
7.            
8.人名查询如果不在档案中会告诉你，没有着一个人，不然会输出这个人的基本信息
9. 更改宋羽玲同学的生源地后重新覆盖了一遍student.txt 并输出   


10. 我的按日期从小到大输出是用了一个类桶排序的算法




本来我是用strcpy、strtok读文档，为const char型。但这个在后面比较修改造成的很大的烦恼，加上当时用strcmp对比数组内的内容。在csdn搜索不出名堂后，选择重开用更方便的string数组来写。

我的按日期从小到大输出是用了一个类桶排序的算法，虽然从到在床上发着烧灵机一动，到最后改完bug，用了超多时间，废了不少脑细胞，但觉得这个算法很漂亮。

改这个bug用了2个小时，当时在碰到访问冲突时，在代码里加了很多cout，输出循环里的重要信息，学会的在调试暂停时，看数组和各个变量的情况，反推到底在哪一步写错。这个改bug的方法以后做算法题时也可以用到，而不是出问题就逛论坛或换一种方法。
还是要尽量做到，写出来的代码就是对的，思路清晰，不要出bug再改。
