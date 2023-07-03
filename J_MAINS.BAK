#include<iostream.h>
#include<string.h>
#include<fstream.h>
#include<conio.h>
#include<stdio.h>

void Questions()
{
	clrscr();

	char str[80];

	ifstream file;

	file.open("Jee_ques.txt",ios::in);

	int i=9;


	while(!file.eof())
	{
		textcolor(WHITE);

		file.getline(str,80);

		if(str[strlen(str)-1]=='#')
		{

			gotoxy(3,i);
			for(int j=0;j<strlen(str)-1;j++)
			{
				cprintf("%c",str[j]);
			}

			getch();
			clrscr();
			i=9;
		}
		else
		{
			gotoxy(3,i);
			cprintf("%s",str);
			i++;
		}
		getch();
	}
	getch();
}
