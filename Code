#include<iostream>
using namespace std;

class ACC {
    string name;
    double ACCNO;
    
public:
    void setName(string n){
        name = n;
    }
    void setACCNO(double A){
        ACCNO=A;
    }
    string getname(){
        return name;
    }
    double getACCNO(){
        return ACCNO;
    }
};

class savingACC : public ACC {
    double Deposit;
    double Balance = 500;
    
public:
    void setDeposit(double D) {
        Deposit = D;
    }
    void setBalance(double B){
        Balance = B;
    }
    double getDeposit() {
        return Deposit;
    }
    double getBalance() {
        return Balance;
    }
    void interest(int money) {
        float sertax = 2;
        Balance = Balance - sertax;
    }
    void Withdrawl() {
        int money;
        cout<<"Enter the amount of money: ";
        cin>>money;
        if (Balance - money > 50) {
            if (Balance < 500) {
                cout<<"We are imposing a penalty for low minimum balance."<<endl<<endl;
                int p1ty = 50;
                Balance = Balance - (money + p1ty);
                interest(money);
                cout<<"Transaction is successful."<<endl;
            } else {
                Balance = Balance - money;
                interest(money);
                cout<<"Transaction is successful."<<endl;
            }
        } else {
            cout<<"Transaction cannot be done."<<endl;
        }
    }
        
    void Deposit1() {
        int money;
        cout<<"Enter the amount of money: ";
        cin>>money;
        Balance = Balance + money;
    }
    
    void Display(){
        cout<<"\n\nBalance: "<<Balance<<endl;
        cout<<"Minimum balance: 500\n\n"<<endl;
    }
};

class currACC : public ACC {
    double Deposit;
    double Balance = 500;
    
public:
    void setDeposit(double D){
        Deposit = D;
    }
    void setBalance(double B){
        Balance = B;
    }
    double getDeposit(){
        return Deposit;
    }
    double getBalance(){
        return Balance;
    }
    void cheque(){
        int money;
        string Bname;
        cout<<"Enter the name of the cheque receiver: ";
        cin>>Bname;
        cout<<"Enter the amount of money: ";
        cin>>money;
        if(Balance - money > 50){
            if(Balance == 0)
                cout<<"Transaction cannot be done."<<endl;
            else{
                Balance = Balance - money;
                cout<<"The transaction is successful."<<endl;
                cout<<endl;
                Display1(Bname, money);
            }
        }
    }
        
    void Deposit1(){
        int money;
        cout<<"Enter the amount of money: ";
        cin>>money;
        Balance = Balance + money;
    }
    
    void Display(){
        cout<<"\n\nBalance: "<<Balance<<endl;
        cout<<"Minimum balance: 500\n\n"<<endl;
    }
    
    void Display1(string Bname, int money){
        cout<<"Cheque receiver: "<<Bname<<endl;
        cout<<"Money: "<<money<<endl;
        cout<<"Balance: "<<Balance<<endl;
    }
};

int main(){
    int choice;
    cout<<"Enter the type of account:"<<endl;
    cout<<"1. Current"<<endl;
    cout<<"2. Saving"<<endl;
    cout<<"Choice: ";
    cin>>choice;
    cout<<"\n\n\n";
    switch (choice){
        case 1:{
            currACC c1;
            string h;
            cout<<"Enter the name of the account holder: ";
            cin>>h;
            c1.setName(h);
            double k;
            cout<<"Account number: ";
            cin>>k;
            c1.setACCNO(k);
            cout<<"\n\nAccount name: "<<c1.getname()<<endl;
            cout<<"Account Number: "<<c1.getACCNO()<<endl;
            cout<<"Balance: "<<c1.getBalance();
            do{
                cout<<"\n\n1. Deposit"<<endl;
                cout<<"2. Withdrawal"<<endl;
                cout<<"3. Exit"<<endl;
                cout<<"Enter choice: ";
                cin>>choice;
                switch (choice) {
                    case 1:
                        c1.Deposit1();
                        c1.Display(); 
                        break;        
                    case 2:
                        c1.cheque();
                        c1.Display(); 
                        break;
                }
            } while (choice != 3);
            break;
        }
        case 2:{
            savingACC s1;
            string h;
            cout<<"Enter the name of the account holder: ";
            cin>>h;
            s1.setName(h);
            double k;
            cout<<"Account No: ";
            cin>>k;
            s1.setACCNO(k);
            cout<<"\n\nAccount name: "<<s1.getname()<<endl;
            cout<<"Account Number: "<<s1.getACCNO()<<endl;
            cout<<"Balance: "<<s1.getBalance();
            do{
                cout<<"\n\n1. Deposit"<<endl; 
                cout<<"2. Withdrawal"<<endl;
                cout<<"3. Exit"<<endl;
                cout<<"Enter choice: ";
                cin>>choice;
                switch (choice) {
                    case 1:
                        s1.Deposit1();
                        s1.Display();
                        break;
                    case 2:
                        s1.Withdrawl();
                        s1.Display();
                        break;
                }
            } while (choice != 3);
            break;
        }
    }
    return 0;
}
