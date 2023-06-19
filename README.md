#include<iostream>
#include<string.h>
using namespace std;

void menu()
{
    cout<<"<====WELCOME TO HALDIRAM====>"<<endl;
    cout<<"_____________________________________________________"<<endl;
    cout<<"    No.    MENU                      PRICE"<<endl;
    cout<<"    01.    Masala Dosa               110.00"<<endl;
    cout<<"    02.    Plain Dosa                90.00"<<endl;
    cout<<"    03.    Raj Kachori               120.00"<<endl;
    cout<<"    04.    Vegetable Chowmein        165.00"<<endl;
    cout<<"    05.    Vegetable Fried Rice      190.00"<<endl;
    cout<<"    06.    French Fries              70.00"<<endl;
    cout<<"    07.    Ginger Tea                120.00"<<endl;
    cout<<"    08.    Colf Coffee With Choco    150.00"<<endl;
    cout<<"    09.    Hot Coffee               80.00"<<endl;
    cout<<"_____________________________________________________"<<endl;
}

main()
{
    float at;
    int n;
    int qty[4];
    int no[4];
    long price[4], total[4];
    string name[4];
    float change,pay;
    
    menu();
    cout<<"How many type of menu do you want to order? : ";
    cin>>n;

    if(n>0 && n<=9)
    {
        for(int i=0;i<n;i++)
        {
            cout<<"Enter your choice: "<<i+1<<"=";
            cin>>no[i];
            cout<<"Enter Amount = ";
            cin>>qty[i];
            if(no[i]==1)
            {
                name[i]="Masala Dosa";
                price[i]=110.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==2)
            {
                name[i]="Plain Dosa";
                price[i]=90.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==3)
            {
                name[i]="Raj Kachori";
                price[i]=120.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==4)
            {
                name[i]="Vegetable Chowmein";
                price[i]=165.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==5)
            {
                name[i]="Vegetable Fried Rice";
                price[i]=190.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==6)
            {
                name[i]="French Fries";
                price[i]=70.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==7)
            {
                name[i]="Ginger Tea";
                price[i]=120.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==8)
            {
                name[i]="Cold Coffee With Chocolete";
                price[i]=150.00;
                total[i]=price[i]*qty[i];
            }
            else
             if(no[i]==9)
            {
                name[i]="Hot Coffee";
                price[i]=80.00;
                total[i]=price[i]*qty[i];
            }
           at=at+total[i];
            }
            system("cls");
            menu();
            cout<<"Your choice is : "<<endl;
            for(int i=0;i<n;i++)
            {
                cout<<""<<qty[i]<<"portion"<<""<<name[i]<<endl;
                cout<<"price/portion ="<<price[i]<<endl;
                cout<<"Total Price"<<name[i]<<"="<<total[i]<<endl;
            }
            cout<<"All Total: "<<at<<"\n";
            
            cout<<"Paid : Rs. ";
            cin>>pay;
            change=pay-at;
            cout<<"Change : Rs. "<<change<<endl;
            cout<<"THANK YOU FOR VISITING HALDIRAM";
    }
    else
    cout<<"Code you input doesn't exist";

    return 0;
}
