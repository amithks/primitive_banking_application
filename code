#include <iostream>
#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <Windows.h>
using namespace std;
void gotoxy(int x, int y)
{
printf("%c[%d;%df", 0x1B, y, x);
fflush(stdout);
}
class Account
{
private:
char name[20];
int ac_no;
long balance;
public:
Account();
void open();
void deposit();
void withdraw();
void display();
int Account::get_ac_no()
{
return(ac_no);
}
~Account();
};
Account::Account()
{
ac_no = 0;
balance = 0;
}
void Account::open()
{
cout << endl << "Name of A/C holder = ";
gets_s(name);
fgets(name, sizeof(name), stdin);
cout << "A/C number = ";
cin >> ac_no;
cout << "\n Balance = ";
cin >> balance;
cout << "press any key to continue......" << endl;
_getch();
}
void Account::deposit()
{
cout << "Name of A/C holder is " << name;
long bal = 0;
cout << endl << "Enter the amount to be deposited = " << endl;
cin >> bal;
balance += bal;
cout << " Updated Balance is : " << balance << "\n";
cout << "Press any key to continue.......";
_getch();
}
void Account::withdraw()
{
cout << "Name of A/C holder is " << name;
long bala = 0;
cout << endl << "Enter the amount to be withdrawn = " << endl;
cin >> bala;
if (balance >= bala)
{
balance = balance - bala;
cout << "Updated balance is : " << balance << "\n";
cout << "Press any key to continue.......";
}
else
{
cout << "Insufficient amount for withdraw: " << endl;
cout << "Press any key to continue.......";
}
_getch();
}
void Account::display()
{
cout << endl << "Name of A/C holder = " << name << endl;
cout << "A/C number = " << ac_no << endl;
cout << "Balance = " << balance << endl;
cout << "Press any key to continue.......";
_getch();
}
Account::~Account()
{
ac_no = 0;
balance = 0;
}
int acc;
void main()
{
Account a[10];
int k = 1, i;
while (1)
{
system("cls");
int c;
gotoxy(30, 8);
cout << " Welcome to SBI ";
gotoxy(30, 9);
cout << "________________";
gotoxy(22, 12);
cout << "1.Open an account" << endl;
gotoxy(22, 13);
cout << "2.Deposit" << endl;
gotoxy(22, 14);
cout << "3.Withdraw" << endl;
gotoxy(22, 15);
cout << "4.Display account information" << endl;
gotoxy(22, 16);
cout << "5.EXIT" << endl;
gotoxy(22, 18);
cout << "Enter your choice" << endl;
gotoxy(22, 19);
cin >> c;
switch (c)
{
case 1:
system("cls");
a[k].open();
k++;
break;
case 2:
system("cls");
cout << "Enter the account number to deposit:" << endl;
cin >> acc;
for (i = 1; i <= 10; i++)
{
if (acc == a[i].get_ac_no())
a[i].deposit();
else
continue;
}
break;
case 3:
system("cls");
cout << "Enter the account no for withdraw:" << endl;
cin >> acc;
for (i = 1; i <= 10; i++)
{
if (acc == a[i].get_ac_no())
a[i].withdraw();
else
continue;
}
break;
case 4:
system("cls");
cout << "Enter the account no for displaying:" << endl;
cin >> acc;
for (i = 1; i <= 10; i++)
{
if (acc == a[i].get_ac_no())
a[i].display();
else
continue;
}
break;
case 5:
exit(5);
}
}
}
