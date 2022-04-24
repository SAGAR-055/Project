# Project
#include <stdio.h>
 
 int main(){
     float total_amt,tranfer,deposit,withdraw,check_balance;
     int pin,password,user_input;

     printf("------------------------------------------------------------------------------------------------------------------------------------------------------------\n");
     printf("-----------------------------------------------------------------WELCOME TO---------------------------------------------------------------------------------\n");
     printf("-----------------------------------------------------------------SRMIST ATM---------------------------------------------------------------------------------\n");
     printf("------------------------------------------------------------------------------------------------------------------------------------------------------------\n");
     printf("Enter your Account Number :RA");
     scanf("%d",&password);
     printf("Enter amount to create account :₹");
     scanf("%f",&total_amt);
     printf("1. check balance\n2. Deposits\n3. Withdraw\n4. Tranfer \nEnter Your Choice :");
    scanf("%d",&user_input);
    printf("Enter Pin :");
    scanf("%d",&pin);

    if(pin==password)
    {
    
    switch (user_input)
    {
    case  1 :
         printf("Your total balance in your account is :₹ %f",total_amt); 
         break;
         case 2 :
          printf("Enter Amount to Deposits :₹");
          scanf("%f",&deposit);
          float net_bal_after;
          net_bal_after = total_amt +deposit;

           printf("\n");
          printf("------------------TRANACTION COMPLETED SUCCESSFULLY-----------------------\n");
           printf("\n");

          printf("Net balance :₹ %.2f",net_bal_after);
          break;
          case 3:
          printf("Enter amount to Withdraw :₹");
          scanf("%f",&withdraw);
          float bal_after_withdraw;
          bal_after_withdraw = total_amt - withdraw;
          printf("\n");
          printf("------------------TRANACTION COMPLETED SUCCESSFULLY-----------------------\n");
          printf("\n");
          printf("Net balance :₹%.2f",bal_after_withdraw);
          break;
      case 4 :
         int Enter_Account_NO;
         printf("ENTER account Number :RA");
        scanf("%d",&Enter_Account_NO);
        printf("Enter amount to transfer :₹");
         scanf("%f",&tranfer);

         float bal_after_tranfer;
         bal_after_tranfer = total_amt - tranfer;
         printf("\n");
         printf("------------------MONEY TRANSFERD SUCCESSFULLY-----------------------\n");
         printf("\n");
         printf("Net balance :₹%.2f",bal_after_tranfer);
         break;    
        default:
        printf("Enter valid  user input");
         break;
    }
    }
    else 
    {
        printf("Invalid Pin");
    }

    printf("\n");
    printf("\n***********************THANK YOU FOR VISTING*************************");
   return 0;
 }

 
