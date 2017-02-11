# Guess-number-game
Guess random numbers from 0 to 9
#include <iostream.h>
   #include <stdlib.h>
    #include <time.h>
    #define MAX 10
    void main()
    {
     bool b=false;
     int n;	//所猜的数字
      int sum=0;	//猜数的次数
      srand( (unsigned)time( NULL ) );	//随机数播种函数
     int num=rand()%MAX;	//设定随机数
     cout<<"随机数已经准备好，范围0到9."<<endl;
    while(b==false)	//猜不对就一直循环
	{
       sum+=1;
      cout<<"请输入你猜的数字"<<endl;
       cin>>n;
       if(n==num)
       {
         b=true;
         cout<<"你太聪明了！"<<endl;
         cout<<"你共猜了"<<sum<<"次"<<endl;
       }
       else if(n<num && n>=0)
       {
         cout<<"你猜小了！继续努力！"<<endl;
	   }
        else if(n>num && n<=9)
		{
         cout<<"你猜大了！继续努力！"<<endl;
        }
      else
	  {
         cout<<"数字范围是0到9，你输入的出界了"<<endl;
	  }
	}
    }
