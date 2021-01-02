#include<bits/stdc++.h>
using namespace std;

class bank{
    
    public:
          char hname[100],add[100],y;
          int balance,a;
          
          void open_account();
          void deposite();
          void withdraw();
          void display_account();
          
};
        
          void bank:: open_account() {
              
              cout<<"enter your full name  : ";
              cin.ignore();
              cin.getline(hname,100);
              cout<<"enter your addresss  : ";
                            cin.ignore();
              cin.getline(add,100);
              cout<<"what type of account you want to open  for 'currant' (c)  and for 'saving' (s) : ";
              cin>>y;
              cout<<"enter  amount for deposite : ";
              cin>>balance;
              
              cout<<"your account has been created  /n : ";
              
              
       void bank::deposite(){
           
           cout<<"enter money you want to deposite : ";
           cin<<a;
           balance+=a;
           cout<<"total amount in your account : \t"<<balance;
           
       }
       
       void bank::dispaly(){
           
           cout<<"your name :  /t"<<name;
           cout<<"your address: /t"<<add;
           cout<<"type of account did you open :/t"<<y;
           cout<<"amount you deposite :/t"<<balance;
           
       }
       
              
     void bank::withdraw()
     {
         float amount;
        cout<<"\n withdraw : " ;
        cout<<"enter ammount to withdraw : ";
        cin>>amount;
        balance-=amount;
        cout<<"your currant balance is  : "<<balance;        
          }


int main()
{
    bank obj;
    
  cout<<"welcome in banking procedure  \n";

int ch,x;

    do{
        
    
    cout<<"1.open account \n";
        cout<<"2.deposite money \n";
            cout<<"3.withdraw money \n";
                cout<<"4.display accounty \n";
                  cout<<"5.exit \n";
 
 cout<<"select an above  options that you want to choose";
 
 cin>>ch;
 
 switch(ch)
 {
   case 1:<<"1.open account \n";
        obj.open_account();
        break;
        
   case 2:<<"2.deposite money \n";
        obj.deposite();
        break;
  
   case 3:<<"3.withdraw \n";
        obj.withdraw();
        break;
   case 4:<<"4.display account\n";
        obj.display_account();
        break;
   case 5:
         if(ch==5){
                exit(1);
         }
         
         default:
         cout<<"this is not exist  plz try again   ";
         
         cout<<"\n if you want to select next option then press :y \n";
         cout<<"if you wan to exit then press : n";
         
     x=getch();
     if (x=='n')
     {
         exit (0);
     }
 }while(x=='y');
 
    

    return 0;
}

