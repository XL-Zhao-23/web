#程序设计基础的作业

```c
//第一次作业

/*
//2019012590 赵小龙 7班 第一题
#include <math.h>
#include <stdio.h>

int main(void)
{
	double a = 1.0, b = 1.0;

	printf("请输入矩形的长和宽\n");
	scanf("%lf,%lf",&a,&b);
	printf("该矩形面积为：%f\n",a * b);

	return 0;
}

//2019012590 赵小龙 7班 第二题
#include <stdio.h>
#include <math.h>
	
int main(void)
{
	int a = 1, b = 1;
	
	printf("请输入两个整数\n");
	scanf("%d,%d",&a,&b);

	if (((a + b) % 10) == 0)
	{
		printf("是好朋友数\n");
	}
	else
	{
		printf("不是好朋友数\n");
	}

	return 0;
}

//2019012590 赵小龙 7班 第三题
#include <stdio.h>
#include <math.h>
	
int main(void)
{
	int a = 0;
	int g = 0, s = 0, b = 0, q = 0;
	
	printf("请输入一个4位八进制整数\n");
	scanf("%d",&a);

	g  = a % 10;
	s  = (a % 100 - g) / 10;
	b  = (a % 1000 - a % 100) / 100;
	q  = (a - a % 1000) / 1000;

	printf("该数对应的十进制数为：%d\n",g + s * 8 + b * 64 + q * 512);

	return 0;
}
*/
//第二次作业
/*
//2019012590 赵小龙 7班 第一题
#include <math.h>
#include <stdio.h>

int main(void)
{
	double a = 1.0, b = 1.0;

	printf("请输入矩形的长和宽\n");
	scanf("%lf,%lf",&a,&b);
	printf("该矩形面积为：%f\n",a * b);

	return 0;
}


//2019012590 赵小龙 7班 第二题
#include <stdio.h>
#include <math.h>
	
int main(void)
{
	int a = 1, b = 1;
	
	printf("请输入两个整数\n");
	scanf("%d,%d",&a,&b);

	if (((a + b) % 10) == 0)
	{
		printf("是好朋友数\n");
	}
	else
	{
		printf("不是好朋友数\n");
	}

	return 0;
}

 
//2019012590 赵小龙 7班 第三题
#include <stdio.h>
#include <math.h>
	
int main(void)
{
	int a = 0;
	int g = 0, s = 0, b = 0, q = 0;
	
	printf("请输入一个4位八进制整数\n");
	scanf("%d",&a);

	g  = a % 10;
	s  = (a % 100 - g) / 10;
	b  = (a % 1000 - a % 100) / 100;
	q  = (a - a % 1000) / 1000;

	printf("该数对应的十进制数为：%d\n",g + s * 8 + b * 64 + q * 512);

	return 0;
}
//第三次作业

//2019012590 赵小龙 7班 第一题
#include <stdio.h>
#include <math.h>

int main(void)
{
	int a, b, c, sum;
	
	printf("请输入三个整数\n");
	scanf("%d %d %d",&a,&b,&c);

	if(a + b > c && b + c > a && a + c > b)
		printf("以%d，%d，%d三条边能够组成三角形\n",a,b,c);
	else
		printf("以%d，%d，%d三条边不能组成三角形\n",a,b,c);

	return 0;
}


//2019012590 赵小龙 7班 第二题
#include <stdio.h>
#include <math.h>

int main(void)
{
	int n, i, x, sum = 0;
	
	printf("请输入数据个数：");
	scanf("%d",&n);

	for (i = 1; n >= i; i++ )
	{    
		printf("请输入第%d个数\n",i);
	    scanf("%d",&x);

		if (x >= 0)
		  sum += x;
	}

	printf("%d个数中正数的和为：%d\n",i - 1,sum);

	return 0;
}


//2019012590 赵小龙 7班 第三题
#include <stdio.h>
#include <math.h>
#include <time.h>
#include <stdlib.h>


int main(void)
{
	
	int i, n, num1, num2, num, flag;
	char x;

	printf("整数运算器（+、-、*）\n"
		   "=====================\n"
		   "|       +:加法      |\n"
		   "|       -:减法      |\n"
		   "|       *:乘法      |\n"
		   "=====================\n");
    
	srand(time(0));
	n = rand();

	

	for (i = n; i > 0;i--)
	{
		printf("您还可以正确计算%d次\n",i);
		printf("请输入表达式：");
		fflush(stdin);       //？清空缓存区，要不输入1+￥类似的会导致无法输入，引发无限循环。？
		flag = scanf("%d%c%d",&num1,&x,&num2);

		if (flag != 3 )
		{
			printf("本次输入有误\n");
			printf("\n");
		    i++;
		}

		else if  (x == '+')
		{
			num = num1 + num2;
			printf("和为：%d\n",num);
			printf("\n");
			
		}
		else if (x == '-')
		{
			num = num1 - num2;
			printf("差为：%d\n",num);
			printf("\n");
			
		}
		else if (x == '*')
		{
			num = num1 * num2;
			printf("积为：%d\n",num);
			printf("\n");
		
		}
	   else 
	    {
		    printf("本次输入有误\n");
			printf("\n");
			i++;
		}
		


	
	}

	return 0;
}
*/

//第四次作业
/*
//  n（5）        第i行  星星数2n-1-i  空格数为i
//*********         0        9            0           星星 = 2n-2i-1 
// *******          1        7            1
//  *****           2        5            2 
//   ***            3        3            3
//    *             4        1            4



//2019012590 赵小龙 7班  第一题
#include <stdio.h>
#include <math.h>

int main(void)
{
	int n, i, j;

	printf("请输入行数%\n");
	scanf("%d",&n);

	for (i = 0 ; i < n; i ++ )
	{
		for (j = 0; j < i;j++)
		{
			printf(" ");
		}
		for (j = 0; j < 2*n - 2*i - 1;j++)
		{
			printf("*");
		}
		printf("\n");
	}

	return 0;
}


//质数只能内1和其本身整除
//  1.从2取到n   i属于2到n。
//  2.每一个数都要判断是否为质数。
//  3.判断质数  i % j == 0  j属于2到i-1。


//2019012590 赵小龙 7班 第二题
#include <stdio.h>

int main(void)
{
	int sum = 0, i, n, j;

	printf("请输入n值：");
	scanf("%d",&n);

	for ( i = 2; i <= n; i++)                
	{           
		for (j = 2; j < i; j++)             
		{                                   
			if (i % j == 0)					
				break;
			if (j == i - 1)
				sum += i;
		}	
	}
	printf("%d\n",sum + 2);
	
	return 0;
}






// 计算1/1+1/(1+2)+1/(1+2+3)+...+1/(1+2+...+n)的值，n由用户输入。
//
//1. 共n个数相加  i 属于 1到n
//2. 第i个数的除数div是从 1 加到 i    j 属于 1到i  
//   分析   除数 sum = 1 + j + ... + i                    
//          结果 ALLsum = 1 / sum1 + 1 / sum2 ... + 1 / sumn
//3. 总结   累加 sum = 0  循环   sum += i       i取一系列值   
//               sum = 0  循环   sum += j       j取一系列值  
//            ALLsum = 0  循环   ALLsum += add  add取一系列值
//4. 用数学方法化简  数列求和转化为计算2 * （1 - 1/(n + 1)）

//2019012590 赵小龙 7班 第三题
#include <stdio.h>

int main (void)
{
	int n, i, j;
	double ALLsum = 0,add = 0,sum = 0;

	printf("请输入n值\n");
	scanf("%d",&n);

	for (i = 1; i <= n; i++ )
	{
		for (j = 1; j <= i; j++)
		{    sum += (double)j;		}

		add = 1.0 / sum;
		sum = 0;

		ALLsum += add;
	}
	printf("%f\n",ALLsum);
	return 0;
}

*/

//第五次作业
/*

//2019012590 赵小龙 7班 第一题计算完数
#include <stdio.h>
#include <math.h>

int main(void)
{
	int i, j;
	int sum = 0;

	for(i = 0; i < 10000; i++)
	{	
		sum = 0;
		for(j = 1; j < i; j++)
		{
			if (i % j == 0)
				sum += j;
			if (j == i - 1 && sum == i)
			{	
				printf("%d:",i);
				for(j = 1; j < i; j++) 
				{
					if(i % j == 0)
						printf("%d ",j);
				}
				printf("\n");
			}
		}
		
	}
	return 0;
}


//2019012590 赵小龙 7班 第二题五分制成绩
#include <stdio.h>
#include <math.h>

int main(void)
{
	int arr[100][1];
	int i;

	for (i = 0;i < 100;i++)
	    scanf("%d",&arr[i][0]);
	for (i = 0; i < 100; i++)
	{
		if (arr[i][0] >= 90)
			printf("A\n");
		else if(arr[i][0] >=80)
			printf("B\n");
		else if(arr[i][0] >=70)
			printf("C\n");
		else if(arr[i][0] >=60)
			printf("D\n");
		else
			printf("E\n");
	}

	return 0;
}



//2019012590 赵小龙 7班 第三题简单求和
#include <stdio.h>
#include <math.h>

int main(void)
{
	int a, n, i;
	int sum = 0;
    int t = 1;
	scanf("%d %d",&a,&n);

	for(i = 1; i <= n; i++)
	{
		t *= 10;
		sum += (t - 1) / 9 * a ;
		
	}

	printf("%d",sum );

	
	return 0;
}


//2019012590 赵小龙 7班 第四题简单求和
#include <stdio.h>
#include <math.h>

int main(void)
{
	int s, e, p, q;

	scanf("%d %d",&s,&e);

	if (s == 1)
		printf("1 ");	
	p = s;
	do
	{
		for(q = 2; q < p; q++)
		{
			if(p % q == 0)
			    break;
		}

		if (p == q)
			printf("%d ",p);
		p++;
	}while(p <= e);
	return 0;
}
/*

//2019012590 赵小龙 7班 第五题求二维数组最大元素
#include <stdio.h>
#include <math.h>

int main(void)
{
    int i, j;
	int arr[6][6];
	int max = 0;

	for(i = 0; i < 6; i++)
	{
			scanf("%d %d %d %d %d %d",&arr[i][0],&arr[i][1],&arr[i][2],&arr[i][3],&arr[i][4],&arr[i][5]);
			
            for(j = 0; j < 6;j++)
			{
				if(max < arr[i][j])
					max = arr[i][j]; 
			}
	}

	for(i = 0; i < 6; i++)
	{
		for(j = 0; j < 6; j++)
		{
			if (max == arr[i][j])
			    printf("%d %d",i,j);
		}
	}
	return 0;
}
*/

//第六次作业
/*
// 第一题 2019012590  赵小龙 7班
#include <stdio.h>
#include <string.h>

int main(void)
{
	char str1[20];
	char str2[10];
	
	printf("请输入第一个字符串（长度小于10）\n");
	gets(str1);
	printf("请输入第二个字符串（长度小于10）\n");
	gets(str2);
	printf("拼接结果为：");
	strcat(str1,str2);
	puts(str1);

	return 0;
}

// 第二题 2019012590  赵小龙 7班
#include <stdio.h>

int main(void)
{
    int arr[10];
	int i,j,temp;

    printf("请输入十个数字：");
	for(i = 0; i < 10; i++)
	   scanf("%d",&arr[i]);

	for(i = 0; i < 9; i++)
	{
		for (j = 0; j < 9 - i; j++)
		{
			if(arr[j] > arr[j+1])
			{
				temp = arr[j];
			    arr[j] = arr[j+1];
				arr[j+1] = temp;
			}
		}
	}

	for(i = 0; i < 10; i++)
		printf("%d ",arr[i]);


	return 0;
}

// 第三题 2019012590  赵小龙 7班
#include <stdio.h>

int main(void)
{
    int arr[4][4];
	int i,j,flag;
	//输入方阵
	for(i = 0; i < 4; i++)
	{
		for(j = 0;j < 4; j++)
			scanf("%d",&arr[i][j]);
	}	
	//判断是否对称
	for(i = 0; i < 3; i++)
	{
		for(j = i + 1;j < 4; j++)
		{
			flag = j;
			if(arr[i][j] != arr[j][i])
				break;
		}
		if (flag == j)
			break;
	}
	//输出方阵
	if (i == 3 && j == 4)
		printf("YES\n");
	else
	    printf("NO\n");
	

	return 0;
}

// 第三题 2019012590  赵小龙 7班
#include <stdio.h>

int main(void)
{
    int arr[4][4];
	int i,j,flag;
	//输入方阵
	for(i = 0; i < 4; i++)
	{
		for(j = 0;j < 4; j++)
			scanf("%d",&arr[i][j]);
	}	
	//判断是否对称
	for(i = 0; i < 3; i++)
	{
		for(j = i + 1;j < 4; j++)
		{
			flag = j;
			if(arr[i][j] != arr[j][i])
				break;
		}
		if (flag == j)
			break;
	}
	//输出方阵
	if (i == 3 && j == 4)
		printf("YES\n");
	else
	    printf("NO\n");
	

	return 0;
}
*/

//第七次作业
/*
//第一题 2019012590 赵小龙 7班
#include <stdio.h>

int gcd1(int num1, int num2)
{
	int i,temp;
	//从较小的数开始试，减少不必要运算。
	if (num1 > num2)
	{
		temp = num1;
		num1= num2;
		num2 = temp;
	}
	//从大到小试，找到的第一个公约数，就是最大的公约数。
	for (i = num1;;i--)
	{
		if ( num1%i == 0 && num2%i == 0)
			return i;
	}
            
}

int main(void)
{
	int num1, num2;

	printf("请输入两个整数");
	scanf("%d %d",&num1,&num2);
    printf("%d",gcd1(num1, num2));
	

	return 0;
}


//第二题 2019012590 赵小龙 7班
#include <stdio.h>

int gcd2(int num1, int num2)
{
    if(num1 % num2 == 0 )
		return num2;
	else
		return gcd2(num2, num1 % num2);
}

int main(void)
{
	int num1, num2;

	printf("请输入两个整数");
	scanf("%d %d",&num1,&num2);
    printf("%d",gcd2(num1, num2));

	

	return 0;
}

//第三题 2019012590 赵小龙 7班
#include <stdio.h>

void firecrackers(int n)
{
	int time;
	int liu = 0, guan = 0, zhang = 0;
	int count = n;

	for(time = n + 1; time < 3*n - 1; time++)
	{
		//   扔鞭炮的时间点                 | 扔出最后一个鞭炮的时间
        if( ((time - 1) % 3 == 0 && time<= 3*n -2) ||
			((time - 1) % 2 == 0 && time<= 2*n -1) ||
			((time - 1) % 1 == 0 && time<= n     ) )
		{
			count++;
		}
		else
			continue;
	}
	
	printf("time = %d \n"
		   "count = %d\n",3*(n-1)+1,count);
}
int main(void)
{
	int n;

	printf("请输入两个整数");
	scanf("%d",&n);
    firecrackers(n);

	return 0;
}
*/

//第八次作业
/*
//2019012590 赵小龙  软件7班
#include <stdio.h>
#include <string.h>

typedef struct text{
	char num[20];
    char name[20];
	int Chinese;
	int math;
	int English;
	double av;
}Text;

int main(void)
{
	Text arr[6];
	int i, max = 0;
	char topStudent[20];

	//输入六名同学的信息
	printf("==================请输入六名同学的学生信息===================\n");
	for (i = 0; i < 6; i++){
		scanf("%s %s %d %d %d",arr[i].num,
			                   arr[i].name,
							   &arr[i].Chinese,
							   &arr[i].math,
							   &arr[i].English);
		//求出六名同学各自的平均成绩
		arr[i].av = ((double)(arr[i].Chinese + arr[i].math + arr[i].English))/3.0;
	}
	

	//打印六名同学平均成绩
    printf("==================六名同学的平均成绩信息如下=================\n");
	for(i = 0; i < 6; i++){
		printf("%-20s %20s %20d %20d %20d %20f\n",arr[i].num,
			                                     arr[i].name,
									             arr[i].Chinese,
									             arr[i].math,
									             arr[i].English,
									             arr[i].av);
	}

	//找出平均成绩最高的学生
	for(i = 0; i < 6; i++){
		if (arr[i].av > max){
		    max = arr[i].av;
			strcpy(topStudent, arr[i].name);
		}
	}

	printf("========平均成绩最高的学生==========\n"
		   "%s\n"
		   "\n",topStudent);
	       
	return 0;
}


//2019012590 赵小龙 软件7班
#include <stdio.h>

typedef struct ATEMP{
    char name[20];
	int  spring;
	int  summer;
	int  autumn;
	int  winter;
	double av;
}atp;

int main(void)
{
	atp arr[10];
	int i, j;

	//输入
	printf("==================请输入依次十座城市名称及气温信息===================\n");
	for (i = 0; i < 10; i++){
		scanf("%s %d %d %d %d",arr[i].name,
			                   &arr[i].spring,
							   &arr[i].summer,
							   &arr[i].autumn,
							   &arr[i].winter);
		//求出六名同学各自的平均成绩
		arr[i].av = ((double)(arr[i].spring + arr[i].summer + arr[i].autumn + arr[i].winter))/4.0;
	}

	//排序
	for(i = 0; i < 9; i++){
		for (j = 0; j < 9 - i; j++){
			if (arr[j].av > arr[j + 1].av){
				atp temp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = temp;
			} 
		}
	}

	//打印
    printf("=================十座城市及平均气温信息平均如下=================\n");
	for(i = 0; i < 10; i++){
		printf("%-20s %5d %5d %5d %5d %7.2f\n",arr[i].name,
			                                   arr[i].spring,
							                   arr[i].summer,
							                   arr[i].autumn,
							                   arr[i].winter,
											   arr[i].av);
	}

	return 0;
}


//2019012590 赵小龙 软件7班
#include <stdio.h>
#include <malloc.h>
#include <string.h>

typedef struct node 
{
    char ID[20];//学号
    int Score;  //成绩
    struct node * Next;
}Node, * List;

void printList(List list)
{
	Node * head = list;
	for(; head != NULL; head = head -> Next)
		printf("%s %d\n",head -> ID,head -> Score);
	puts("===================");
}

void pushBackList(List * pList , char ID[20],int Score)
{
	Node * head = *pList;

	Node * newNode = (Node *) malloc(sizeof(Node));
	strcpy(newNode -> ID,ID);
	newNode -> Score = Score;
	newNode -> Next = NULL;

	if (head == NULL)
	{
		*pList = newNode;
	}

	else
	{
		while(head -> Next != NULL)
			head = head -> Next;
		head -> Next = newNode;
	}
}

//插入节点
void Insert(List * L, Node e)
{
	Node * head = *L;
	
	Node * newNode = (Node *) malloc (sizeof(Node));
	strcpy(newNode -> ID,e.ID);
	newNode->Score = e.Score;
	newNode->Next = NULL;

	//如果是空链表
	if (head == NULL){
	    *L = newNode;
	}

	//如果不是空链表
	else{
	    while(head ->Next != NULL)
            head = head -> Next; 
		head -> Next = newNode;
	}
}

//交换数据
Node * atList(List *L,int index)
{
	Node * head = *L;
	int i;

	for(i = 0;i < index - 1; i++)
		head = head -> Next;
	return head;
}

void Swap(List * L, int i, int j)
{
	int tempScore;
	char tempID[20];

	tempScore = atList(L,i) -> Score;
	strcpy(tempID,atList(L,i) -> ID);
	atList(L,i) -> Score = atList(L,j) -> Score;
	strcpy(atList(L,i) -> ID,atList(L,j) -> ID);
	atList(L,j) -> Score = tempScore;
	strcpy(atList(L,j) -> ID,tempID);
}

void freeList(List * pList)
{
	Node * head = *pList;
	Node * del = NULL;


	while (head != NULL)
	{
		del = head;
		head = head -> Next;
		free(del);
	}
}

int main(void)
{
	List list = NULL; 
	Node newNode;
	strcpy(newNode.ID,"2019012590");
	newNode.Score = 777777;

	pushBackList(&list, "2019012510",11);
	pushBackList(&list, "2019012520",22);
	pushBackList(&list, "2019012530",33);
	pushBackList(&list, "2019012540",44);
    pushBackList(&list, "2019012550",55);
	pushBackList(&list, "2019012560",66);
	pushBackList(&list, "2019012570",77);
	pushBackList(&list, "2019012580",88);
	pushBackList(&list, "2019012590",99);

	printList(list);

	Insert(&list,newNode);
	printList(list);

	Swap(&list,1,2);
	printList(list);

	freeList(&list);

	return 0;
}
*/

//第十次作业

/**********************
 * 姓名：赵小龙
 * 学号：2019012590
 * 程序设计基础：C语言-任务10
 **********************/
/*
#include <stdio.h>
#include <malloc.h>
#include <string.h>

typedef struct text
{
	char name[20];
	int math;
	int computer;
	int English;
	struct text * next ;
}Text, * List;
//在末尾插入新节点
void pushBackList(List* pList,char name[20],int math,int computer,int English){
    Text * head = *pList;
    Text * newnode = (Text*) malloc(sizeof(Text));
	strcpy(newnode->name,name);
	newnode->math = math;
	newnode->computer = computer;
	newnode->English = English;
	newnode->next = NULL;
	
	if (head == NULL){
	    *pList = newnode;
	}
	else{
	    for(;head->next != NULL; head = head -> next);
		head -> next = newnode;
	}
};
//打印节点内容
void printList(List list){
	Text *head = list;
	for (; head != NULL; head = head -> next){
		printf("name:%-20s math:%-5d computer:%-5d english:%-5d\n",head -> name, head -> math, head ->computer, head ->English);	
 	}
	puts("以下学生没通过考试");
};


int main(void)
{
	FILE *fp;
	List list = NULL;
	char name[20];
	int math, computer, English,i = 0;
    
	//学生信息
	puts("所有学生信息如下:");

	fp = fopen("D://info.txt","r");

	while(!feof(fp)){
	    fscanf(fp,"%s %d %d %d",name, &math, &computer, &English);
		pushBackList(&list, name, math, computer, English);
	}

	printList(list);

	//未通过的同学
	for(; list -> next != NULL; list = list -> next){
		if(list->math < 60 || list->computer < 60 || list->English < 60 || list->math + list ->computer + list -> English < 210 ){
		    i++;
			printf("%s\n",list -> name);
		}
	}
	
	//未通过人数
	printf("没有通过考试的人数：%d\n",i);

    fclose(fp);
	return 0;
}

*/

```

