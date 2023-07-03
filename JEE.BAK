#include<iostream.h>
#include<process.h>
#include<fstream.h>
#include<conio.h>
#include<string.h>
#include<stdio.h>

void add_record();
void instruction();
void Home_page();
void physics_test();
void chemistry_test();
void maths_test();
void Jee_test();
void custom_test();
void test_series();
void change_test();

#include"JEETEST.cpp"

struct Records
{
	char User_Name[20];
	char User_Id[10];
	char User_Password[30];

	char Name[30];
	char Phone[20];
	char Std[5];

	void insert()
	{
		cout<<"User Name:";
		gets(User_Name);

		cout<<"User Password:";
		gets(User_Password);

		cout<<"User Id:";
		gets(User_Id);

		cout<<"Name:";
		gets(Name);

		cout<<"Phone Number:";
		gets(Phone);

		cout<<"Standard:";
		cin>>Std;
	}
	void display()
	{
		cout<<"User Name:";
		cout<<User_Name;

		cout<<"User Password:";
		cout<<User_Password;

		cout<<"User Id:";
		cout<<User_Id;

		cout<<"Name:";
		cout<<Name;

		cout<<"Phone Number:";
		cout<<Phone;

		cout<<"Standard:";
		cout<<Std;
	}
}user;

//****************************************************************************************************************//
//****************************************************************************************************************//

void layout()
{
	clrscr();

	textcolor(WHITE);

	cprintf(" ***************************************************************************** ");cout<<"\n";
	cprintf("|                                                                             |");cout<<"\n";
	cprintf("|        J E E     M A I N S     M O C K     T E S T S     O N L I N E        |");cout<<"\n";
	cprintf("|       ~~~~~~~   ~~~~~~~~~~~   ~~~~~~~~~   ~~~~~~~~~~~   ~~~~~~~~~~~~~       |");cout<<"\n";
	cprintf(" *****************************************************************************");cout<<"\n";


}

//****************************************************************************************************************//
//****************************************************************************************************************//

void details()
{
	ifstream file;
	file.open("jeerec.bin",ios::binary | ios::in);

	details:;

	char regist;

	while(1)
	{
		clrscr();

		layout();

		char Name_check[30];
		char Id_check[30];
		char Password_check[30];

		cout<<"\n\n\t\t\t";
		cprintf("       LOGIN  DETAILS:");
		cout<<"\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("User Name:      |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		cout<<"\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("User Id:        |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		cout<<"\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("User Password:  |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		gotoxy(35,10);
		gets(Name_check);

		gotoxy(35,13);
		gets(Id_check);

		gotoxy(35,16);
		gets(Password_check);

		while(file.read((char*)&user,sizeof(user)))
		{
			if(strcmp(Id_check,user.User_Id)==0)
			{
				if(strcmp(Name_check,user.User_Name)==0)
				{
					if(strcmp(Password_check,user.User_Password)==0)
					{
						gotoxy(30,20);
						cprintf("Your Account Has Been Found !!");
						getch();
						Home_page();  // test menu!!!1
					}
					else
					{
						gotoxy(30,20);
						cprintf(" X X Wrong Password X X");
						getch();
						file.seekg(0);
						goto details;
					}
				}
				else
				{
					gotoxy(30,20);
					cprintf(" X X Wrong User Name  X X");
					getch();
					file.seekg(0);
					goto details;
				}
			}
			else
			{
				gotoxy(30,20);
				cprintf(" X X Account Doesnot Exists... X X");
				gotoxy(30,21);
				cprintf(" Want To Register..?");
				gotoxy(30,22);
				cprintf(" Press Y/y To Register..!!");

				cin>>regist;

				if(regist=='y' || regist=='Y')
				{
					add_record();
					file.seekg(0);
					goto details;

				}
				else
				{
					cprintf("Want To Exit ??");
					cprintf("Press y/Y To Exit.....!!!");
					cin>>regist;

					if(regist=='y' || regist=='Y')
					{
						exit(0);
					}
					else
					{
						details();
					}
				}

			}
		}


	}
}

//****************************************************************************************************************//
//****************************************************************************************************************//

void add_record()
{
	int x_name=0, x_phone=0, x_std=0, x_username=0, x_userid=0, x_userpassword=0;
	Records tempuser;

	while(x_name==0 && x_phone==0 && x_std==0 && x_username==0 && x_userid==0 && x_userpassword==0 )
	{
		clrscr();

		layout();


		cout<<"\t\t\t";
		cprintf("       SIGNUP DETAILS:");
		cout<<"\n\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("Name:           |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		cout<<"\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("Phone:          |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		cout<<"\n\t\t";
		cprintf("                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
		cout<<"\n\t\t";
		cprintf("Std:            |                            |");
		cout<<"\n\t\t";
		cprintf("                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

		cout<<"\n\t\t                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|";
		cout<<"\n\t\tUser Name:      |                            |";
		cout<<"\n\t\t                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~";

		cout<<"\n\t\t                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|";
		cout<<"\n\t\tUser Password:  |                            |";
		cout<<"\n\t\t                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~";

		cout<<"\n\t\t                |~~~~~~~~~~~~~~~~~~~~~~~~~~~~|";
		cout<<"\n\t\tUser Id:        |                            |";
		cout<<"\n\t\t                 ~~~~~~~~~~~~~~~~~~~~~~~~~~~~";

		gotoxy(35,9);
		gets(tempuser.Name);

		gotoxy(35,12);
		gets(tempuser.Phone);

		gotoxy(35,15);
		cin>>tempuser.Std;


		gotoxy(35,18);
		gets(tempuser.User_Name);

		gotoxy(35,21);
		gets(tempuser.User_Password);
		gotoxy(35,21);
		for(int i=0;i<strlen(tempuser.User_Password);i++)
		{
			cout<<"*";
		}

		gotoxy(35,24);
		gets(tempuser.User_Id);

		x_name=strlen(tempuser.Name);

		x_phone=strlen(tempuser.Phone);

		x_std=strlen(tempuser.Std);

		x_username=strlen(tempuser.User_Name);

		x_userid=strlen(tempuser.User_Id);

		x_userpassword=strlen(tempuser.User_Password);

		if(x_name==0 || x_phone==0 || x_std==0 || x_username==0 || x_userid==0 || x_userpassword==0 )
		{
			gotoxy(22,7);

			textcolor(RED+BLINK);
			cprintf("Your Form Is Still Missing !!!!");

			getch();
		}

		ifstream fellow;

		ofstream file;

		file.open("tempjeerec.bin",ios::app);

		fellow.open("jeerec.bin",ios::binary | ios::in);

		while(fellow.read((char*)&user,sizeof(user)))
		{
			// Name,Password,Std can be same....
			// User-id ,user-name ,phon should be different!!

			if((strcmp(tempuser.User_Id,user.User_Id)==0)  &&  (strcmp(tempuser.User_Name,user.User_Name)==0)  &&  (strcmp(tempuser.Phone,user.Phone)==0) )
			{
				gotoxy(22,7);
				cout<<"This Whole Account Exists.....!!!";
				getch();

				x_name=0;
				x_phone=0;
				x_std=0;
				x_username=0;
				x_userid=0;
				x_userpassword=0;
			}
			else if(strcmp(tempuser.User_Id,user.User_Id)==0)
			{
				gotoxy(22,7);
				cout<<"User_Id Exists.....!!!";
				getch();
				x_userid=0;
			}
			else if(strcmp(tempuser.User_Name,user.User_Name)==0)
			{
				gotoxy(22,7);
				cout<<"User_Name Exists.....!!!";
				getch();
				x_username=0;
			}
			else if(strcmp(tempuser.Phone,user.Phone)==0)
			{
				gotoxy(22,7);
				cout<<"Phone Number Exists.....!!!";
				getch();
				x_phone=0;
			}
			else
			{
				gotoxy(22,7);
				textcolor(RED+BLINK);
				cprintf("Your Account Has Been Registered !!!");

				file.write((char*)&tempuser,sizeof(tempuser));
				getch();
			}

	       }

	       file.close();

	       fellow.close();

	       remove("jeerec.bin");

	       rename("tempjeerec.bin","jeerec.bin");



	}

	details();


}

//****************************************************************************************************************//
//****************************************************************************************************************//

void Home_page()
{
	Fill_Start:;

	char ch;
	int count_tab=0;
	clrscr();
	layout();

	cout<<"\n\n";
	textcolor(WHITE);

	textcolor(YELLOW+BLINK);
	gotoxy(17,9);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(17,10);
	cprintf("| 1. Physics Test ( 25 Questions)            |");
	gotoxy(17,11);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	textcolor(WHITE);
	gotoxy(17,12);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(17,13);
	cprintf("| 2. Chemistry Test ( 25 Questions)          |");
	gotoxy(17,14);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(17,15);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(17,16);
	cprintf("| 3. Mathematics Test ( 25 Questions)        |");
	gotoxy(17,17);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(17,18);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(17,19);
	cprintf("| Jee Test (ALL SUBJECTS --> (75 Questions)  |");
	gotoxy(17,20);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(17,21);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(17,22);
	cprintf("| Custom Test..( TEST OF YOUR CHOICE )       |");
	gotoxy(17,23);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");


	while(1)
	{
		ch=getch();
		if(int(ch)==13)
		{

			//physics_test();

			layout();
			test_series();
			change_test();

		}
		else if(int(ch)==9)
		{
			count_tab++;
		}
		else if(int(ch)==27)
		{
			exit(0);
		}
		if(count_tab==1)
		{

			textcolor(WHITE);
			gotoxy(17,9);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,10);
			cprintf("| 1. Physics Test ( 25 Questions)            |");
			gotoxy(17,11);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			textcolor(YELLOW+BLINK);
			gotoxy(17,12);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,13);
			cprintf("| 2. Chemistry Test ( 25 Questions)          |");
			gotoxy(17,14);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			ch=getch();

			if(int(ch)==13)
			{
				chemistry_test();
			}
			else
			{
				continue;
			}


		}
		else if(count_tab==2)
		{
			textcolor(WHITE);
			gotoxy(17,12);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,13);
			cprintf("| 2. Chemistry Test ( 25 Questions)          |");
			gotoxy(17,14);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			textcolor(YELLOW+BLINK);
			gotoxy(17,15);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,16);
			cprintf("| 3. Mathematics Test ( 25 Questions)        |");
			gotoxy(17,17);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");


			ch=getch();

			if(int(ch)==13)
			{
				maths_test();
			}
			else
			{
				continue;
			}

		}
		else if(count_tab==3)
		{
			textcolor(WHITE);
			gotoxy(17,15);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,16);
			cprintf("| 3. Mathematics Test ( 25 Questions)        |");
			gotoxy(17,17);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			textcolor(YELLOW+BLINK);
			gotoxy(17,18);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,19);
			cprintf("| Jee Test (ALL SUBJECTS --> (75 Questions)  |");
			gotoxy(17,20);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			ch=getch();

			if(int(ch)==13)
			{
				Jee_test();
			}
			else
			{
				continue;
			}

		}
		else if(count_tab==4)
		{

			textcolor(WHITE);
			gotoxy(17,18);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,19);
			cprintf("| Jee Test (ALL SUBJECTS --> (75 Questions)  |");
			gotoxy(17,20);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			textcolor(YELLOW+BLINK);
			gotoxy(17,21);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(17,22);
			cprintf("| Custom Test..( TEST OF YOUR CHOICE )       |");
			gotoxy(17,23);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

			ch=getch();

			if(int(ch)==13)
			{
				custom_test();
			}
			else
			{
				continue;
			}

		}
		else if(count_tab==5)
		{

			goto Fill_Start;
		}
	}

}
//****************************************************************************************************************//
//****************************************************************************************************************//

void instruction()
{
	clrscr();
	layout();

	cout<<"\n";
	cprintf("                       *****  GENERAL INSTRUCTION  *****                    ");

	cout<<"\n\n";
	cprintf(" # Students Must");
	textcolor(YELLOW);
	cprintf(" Not Use Calculator");
	textcolor(WHITE);
	cprintf(" And Other Unfair Means While Taking The ");
	cout<<"\n";
	cprintf("   Test.");

	cout<<"\n\n";
	cprintf(" # The Duration Of The Test Is");
	textcolor(YELLOW);
	cprintf(" 30 Minutes ");
	textcolor(WHITE);
	cprintf(". You Will ");
	textcolor(YELLOW);
	cprintf("Not Be Able To Submit ");
	textcolor(YELLOW);
	cout<<"\n";
	cprintf("   The Test After The Time Is Over.");
	textcolor(WHITE);

	cout<<"\n\n";
	cprintf(" # There Will Be Total ");
	textcolor(YELLOW);
	cprintf("20 MCQ Type Questions ");
	textcolor(WHITE);
	cprintf("in The Test.");

	cout<<"\n\n";
	cprintf(" # Each Question Carries");
	textcolor(YELLOW);
	cprintf(" 4 Marks");
	textcolor(WHITE);
	cprintf(" . There Is ");
	textcolor(YELLOW);
	cprintf("Negative Marking (-1) ");
	textcolor(WHITE);
	cprintf("For Every ");
	cout<<"\n";
	cprintf("   Incorrect Question.");

	cout<<"\n\n";
	cprintf(" # To Move To ");
	textcolor(YELLOW);
	cprintf("Next Question");
	textcolor(WHITE);
	cprintf(" , Click On The ");
	textcolor(YELLOW);
	cprintf("Next Button");
	textcolor(WHITE);
	cprintf(". To Move To ");
	textcolor(YELLOW);
	cprintf("Previous ");
	textcolor(WHITE);
	cout<<"\n";
	cprintf("   Question");
	cprintf(" , Click On The ");
	textcolor(YELLOW);
	cprintf("Previous Button.");

	textcolor(WHITE);
	cout<<"\n\n";
	cprintf(" # Student Can Submit Their Test By CLicking On ");
	textcolor(YELLOW);
	cprintf("The Submit Button.");
	textcolor(WHITE);
	getch();
}
void test_series()
{

	gotoxy(1,7);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,8);
	cprintf("| Test - 1          Not Attemped |");
	gotoxy(1,9);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(1,10);

	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,11);
	cprintf("| Test - 2          Not Attemped |");
	gotoxy(1,12);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(1,13);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,14);
	cprintf("| Test - 3          Not Attemped |");
	gotoxy(1,15);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(1,16);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,17);
	cprintf("| Test - 4          Not Attemped |");
	gotoxy(1,18);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(1,19);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,20);
	cprintf("| Test - 5          Not Attemped |");
	gotoxy(1,21);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(1,22);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,23);
	cprintf("| Test - 6          Not Attemped |");
	gotoxy(1,24);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(45,7);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,8);
	cprintf("| Test - 7          Not Attemped |");
	gotoxy(45,9);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");


	gotoxy(45,10);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,11);
	cprintf("| Test - 8          Not Attemped |");
	gotoxy(45,12);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(45,13);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,14);
	cprintf("| Test - 9          Not Attemped |");
	gotoxy(45,15);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(45,16);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,17);
	cprintf("| Test - 10         Not Attemped |");
	gotoxy(45,18);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(45,19);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,20);
	cprintf("| Test - 11         Not Attemped |");
	gotoxy(45,21);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(45,22);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(45,23);
	cprintf("| Test - 12         Not Attemped |");
	gotoxy(45,24);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");

	gotoxy(3,25);
	textcolor(YELLOW+BLINK);
	cprintf("Press Esc To EXiT !!!! ....");

}
  /*
void physics_test()
{
	clrscr();
	layout();

	test_series();
	change_test();

	getch();
}
*/
void change_test()
{
	char ch;

	start:;

	int count_tab=0;
	int not_again=0;

	textcolor(WHITE);
	test_series();
	textcolor(YELLOW+BLINK);
	gotoxy(1,7);
	cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
	gotoxy(1,8);
	cprintf("| Test - 1          Not Attemped |");
	gotoxy(1,9);
	cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
	textcolor(WHITE);

	while(1)
	{
		ch=getch();

		if(int(ch)==9)
		{
			count_tab++;
		}
		else if(int(ch)==27)
		{
			clrscr();
			Home_page();
		}
		if(count_tab==0 && not_again==0)
		{
			ch=getch();
			not_again++;

			if(int(ch)==13)
			{
				instruction();
				physics_test();
				break;
			}
			else
			{
				goto start;
			}
		}
		if(count_tab==1)
		{
			test_series();
			textcolor(YELLOW+BLINK);
			gotoxy(1,10);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(1,11);
			cprintf("| Test - 2          Not Attemped |");
			gotoxy(1,12);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==2)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(1,13);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(1,14);
			cprintf("| Test - 3          Not Attemped |");
			gotoxy(1,15);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==3)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(1,16);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(1,17);
			cprintf("| Test - 4          Not Attemped |");
			gotoxy(1,18);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==4)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(1,19);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(1,20);
			cprintf("| Test - 5          Not Attemped |");
			gotoxy(1,21);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==5)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(1,22);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(1,23);
			cprintf("| Test - 6          Not Attemped |");
			gotoxy(1,24);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==6)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,7);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,8);
			cprintf("| Test - 7          Not Attemped |");
			gotoxy(45,9);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==7)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,10);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,11);
			cprintf("| Test - 8          Not Attemped |");
			gotoxy(45,12);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==8)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,13);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,14);
			cprintf("| Test - 9          Not Attemped |");
			gotoxy(45,15);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==9)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,16);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,17);
			cprintf("| Test - 10         Not Attemped |");
			gotoxy(45,18);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==10)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,19);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,20);
			cprintf("| Test - 11         Not Attemped |");
			gotoxy(45,21);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==11)
		{
			test_series();textcolor(YELLOW+BLINK);
			gotoxy(45,22);
			cprintf("|~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~|");
			gotoxy(45,23);
			cprintf("| Test - 12         Not Attemped |");
			gotoxy(45,24);
			cprintf(" ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~");
			textcolor(WHITE);
		}
		if(count_tab==12)
		{
			goto start;
		}
	}

}
void chemistry_test()
{
	clrscr();
	cout<<"Chemsitry!!!";
}
void maths_test()
{
	clrscr();
	cout<<"Maths!!!";
}
void Jee_test()
{
	clrscr();
	cout<<"JEE!!!";
}
void custom_test()
{
	clrscr();
	cout<<"Custom!!";
}

void main()
{
	clrscr();
	layout();
	details();
	Home_page();
	getch();
}

