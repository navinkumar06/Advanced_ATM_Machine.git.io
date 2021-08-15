          # Advanced_ATM_Machine
          
          # source   code 
          
          import random
CIN = random.randint(1094785800,9999999999)
TID=random.randint(12345555,543211111)
FN=random.randint(123455,5432111)
pin_code = 1234
amount = 100000
acc_no = 20424637245
acc_holder_name = "NAVIN KUMAR"
print("\n\n")
print("\tSWIPE YOUR CARD\t")
pc = int(input("ENTER YOUR PIN CODE : "))
if pc==pin_code:
    while(True):
        print("\n\n")
        print("1. BANKING .")
        print("2. OPEN / WITHDRAW FIXED DEPOSIT .")
        print("3. PAY UTILITY BILLS .")
        print("4. PAY INCOME TAX .")
        print("5. PAY INSURANCE PREMIUM .")
        print("6. APPLY FOR PERSONAL LOANS .")
        print("7. EXIT .")
        
        choice=int(input("ENTER YOUR CHOICE : "))
        
           #     BANKING   PARTS   START     HERE
            
        
        if choice == 1:                     #   banking
            print("\n\n")
            print("\n\tWELCOME TO BANKING  ZONE ...\n")
            print("1. WITHDRAW CASH .")
            print("2. DEPOSIT CASH / CHEQUE .")
            print("3. TRANSFER MONEY .")
            print("4. BALANCE ENQUIRY .")
            print("5. PIN CHANGE .")
            print("6. EXIT .")
            print("\n\n")
            
            ch1=int(input("ENTER YOUR CHOICE : "))
            if ch1 == 1:
                withdraw_amt=int(input("\nENTER AMOUNT TO WITHDRAW : "))
                
                if withdraw_amt > amount:
                    print("\n")
                    print("INSUFFICIENT AMOUNT IN YOUR ACCOUNT \nPLEASE ENTER A VALID AMOUNT !")
                    print("\n\n")
                else:
                    print("\n")
                    print("TRANSACTION IS SUCCESSFUL")
                    print("COLLECT YOUR RS " ,withdraw_amt," CASH BEFORE LEAVING ATM")
                    print("YOUR TRANSACTION ID IS : ",TID)
                    amount = amount - withdraw_amt
                    print("ACCOUNT BALANCE : ",amount)
                    print("\n\n")
                
            elif ch1 == 2:
                print("\n\nPLEASE PUT YOUR CASH / CHEQUE INTO MACHINE FIRST . THEN , ")
                deposit_amt=int(input("\nENTER AMOUNT TO DEPOSIT : "))
                
                if deposit_amt > 50000:
                    print("\n")
                    print("\nCROSSES MAXIMUM DEPOSIT LIMIT.  \nPLEASE ENTER A VALID AMOUNT BETWEEN 100.00  AND 50,000.00  !")
                    print("\n\n")
                else:
                    print("\n")
                    print("TRANSACTION IS SUCCESSFUL")
                    print("YOUR TRANSACTION ID IS : ",TID)
                    print("\n")
                    print("PLEASE COLLECT YOUR RECEIPT....")
                    print("\n\n")
                    amount = amount + deposit_amt
                
            elif ch1 == 3:
                print("\n\n")
                bf_name=input("ENTER BENEFICIARY NAME : ")
                bf_ac= int(input("ENTER BENEFICIARY ACCOUNT NUMBER : "))
                bf_ac_r= int(input("RE-ENTER BENEFICIARY ACCOUNT NUMBER : "))
                if bf_ac == bf_ac_r:
                    while(True):
                        transfer_amt=int(input("ENTER AMOUNT TO TRANSFER : "))
                        
                        if transfer_amt > amount:
                            print("\n\n")
                            print("INSUFFICIENT AMOUNT IN YOUR ACCOUNT FOR TRANSFERRING RS  ",transfer_amt," TO ",bf_name)
                        elif transfer_amt > 50000:
                            print("\n\n")
                            print("TRANSFER LIMIT EXCEEDED..\n\nPLEASE ENTER AMOUNT OF LESS THAN RS 50,000.00")
                        else:
                            print("\n")
                            print("YOU HAVE  SUCCESSFULLY TRANSFERRED RS ",transfer_amt, " TO ",bf_name)
                            amount = amount - transfer_amt
                            print("YOUR TRANSACTION ID  IS : ",TID)
                            print("LEFT BALANCE IN YOUR ACCOUNT : ",amount)
                            print("\n")
                            print("PLEASE COLLECT YOUR RECEIPT....")
                            print("\n\n")
                    
                else:
                    print("ACCOUNT NUMBER DIDN'T MATCH .\n\nRE-ENTER BENIFICIARY ACCOUNT NUMBER..")
                    print("\n\n")
                    
                    

            elif ch1 == 4:
                print("YOUR SAVING ACCOUNT BALANCE IS : ",amount)
                print("\n\n")
            
            elif ch1 == 5:
                cuurent_pin_code=int(input("ENTER YOUR CURRENT PIN CODE : "))
                if cuurent_pin_code == pin_code:
                    while(True):
                        new_pin_code=int(input("ENTER YOUR NEW PIN CODE:"))
                        pin_code = new_pin_code
                        print("\n")
                        print("YOUR PIN CODE HAS BEEN  UPDATED SUCCESSFULLY  .\n")
                        print("YOUR NEW PIN CODE IS : ",pin_code,", KEEP REMEMBER IT FOR FUTURE USE")
                        print("\nFOR COUNTINUING START FROM STARTING AS YOUR PIN CODE GOT UPDATED")
                        print("THANK YOU")
                        
                        
                        
                else:
                    print("\n")
                    print("YOU HAVE ENTERED INVALID CURRENT PIN CODE ! , TRY AGAIN ..")
                    print("\n\n")
            
            
            elif ch1 == 6:
                exit()
            
            else:
                print("\n\n\tPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 6 !\n\nTRY AGAIN WITH VALID CHOICE ...\n\n")
                
                  #     BANKING   PARTS   ENDS      HERE       
                
    
                    
                    
                    
       #      STARTING   FIXED   DEPOSIT     PART            
                    
                    
            
            
        elif choice == 2:
            print("\n\n")
            print("\tWELCOME TO FIXED DEPOSIT  ZONE ...\n")
            print("1. OPEN A NEW FIXED DEPOSIT .")
            print("2. WITHDRAW EXISTING FIXED DEPOSIT .")
            print("3. VIEW YOUR FIXED DEPOSIT DETAILS .")
            print("3. EXIT .")
            print("\n\n")
            
            ch2 =int(input("ENTER YOUR CHOICE : "))
            if ch2  == 1:
                print("\n\n")
                print("YOU ARE WELCOME HERE TO OPEN A NEW FIXED DEPOSIT\n\n")
                print("PLEASE READ CAREFULLY AND  FILL OUT THE  DETAILS CORRECTLY\n\n")
                print("WE ACCEPT ONE OF THESE DOCUMENT AS KYC / ADDRESS PROOF .IT MUST BE IN YOUR NAME .\n\n")
                print("  ADHAAR CARD    |   PAN CARD    |     PASSPORT    |  VOTER ID  |  DRIVING LICENCE  | GOVT. ID CARD ")
                kyc_doc=input("ENTER YOUR KYC DOCUMENT NAME : ")
                kyc_doc_num=input("ENTER YOUR KYC DOCUMENT NUMBER : ")
                name=input("ENTER YOUR NAME : ")
                dob=input("ENTER YOUR DATE OF BIRTH (dd-mm-yyyy): ")
                fd_amt=input("ENTER A FIXED DEPOSIT AMOUNT : ")
                fd_time=input("FOR HOW LONG , YOU WANT TO FIX YOUR  FD : ")
                
                print("CONGRATULATIONS !!,  YOU HAVE SUCCESSFULLY CREATED YOUR FD WITH AMOUNT OF RS ",fd_amt,"WITH US .")
                print("YOUR FD  FOLIO NUMBER IS : ",FN)
                folio_number= FN
                print("\n\nTHANK YOU FOR SHOWING TRUST IN US .\n\n")
            
            
            elif ch2 == 2:
                del_fd_ac=int("PLEASE ENTER YOUR ACCOUNT NUMBER LINKED WITH FD : ")
                if  del_fd_ac == acc_no:
                    while(True):
                        decision=input("ARE YOU SURE TO WITHDRAW FD (y/n) : ")
                        if decision ==y or decision == Y or decision ==YES or decision ==yes:
                            print("\n\nSORRY TO HEAR , YOU'RE WITHDRAWING YOUR FD .")
                            print("\nPLEASE COLLECT YOUR AMOUNT FROM THE COUNTER WITH TOKEN NO. :",TID)
                            print("\nHOPE TO SERVE YOU IN A MORE BETTER WAY NEXT TIME\n\n")
                        else:
                            print("\n\nTHANK YOU STAYING INVESTED IN  FD..")
                else:
                    print("\n\nSORRY !, THERE IS NO ANY FD LINKED TO  ACCOUNT THAT YOU'VE ENTERED :",del_fd_ac)
                    print("\n\nPLEASE TRY AGAIN WITH VALID ACCOUNT NUMBER\n\n")
                
            elif ch2 == 3:
                print("\n\nYOUR FIXED DEPOSIT DETAILS ARE  GIVEN BELOW : \n\n")
                print("ACCOUNT HOLDER NAME : ",name)
                print("\nFOLIO NUMBER: ",folio_number)
                print("\nFIXED DEPOSIT AMOUNT : ",fd_amt)
                print("\nKYC DOCUMENT NAME :",kyc_doc)
                print("\nKYC NUMBER : ",kyc_doc_num)
                print("\nFIXED DEPOSIT TIME : ",fd_time)
                print("\nDATE OF BIRTH : ",dob)
                
            elif ch2 == 3:
                exit()
                
            else:
                print("\n\nPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 3 !\n\nTRY AGAIN WITH VALID CHOICE ...")
                
         
            
                         
       #      ENDING    FIXED   DEPOSIT     PART        
            
            
            
            
            
           #   PAY    UTILITY   BILLS     SECTION  STARTED HERE
            
            
            
            
            
            
            
        elif choice == 3:
            print("\n\n")
            print("\tWELCOME TO UTILITY BILL  ZONE ...\n")
            print("1. RECHARGE / PAY MOBILE BILL .")
            print("2. PAY ELECTRIC BILL .")
            print("3. PAY GAS BILL .")
            print("4. EXIT .")
            
            ch3 = int(input("ENTER YOUR CHOICE : "))
            
            if ch3 == 1:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR MOBILE RECHARGE / BILL PAYMENT \n\n")
                mobile_no = int(input("ENTER YOUR MOBILE NUMBER : "))
                operator = input("ENTER YOUR  OPERATOR : ") 
                recharge_amt=int(input("ENTER RECHARGE AMOUNT : "))
                print("\n\tYOUR RECHARGE FOR MOBLIE NO . - ",mobile_no,"AMOUNTING Rs ",recharge_amt," IS SUCCESSFULL !! \n") 
                print("YOUR TRANSACTION  ID IS : ",TID)
                print("\nTHANK YOU FOR USING OUR SERVICE.....\n")
                
                
            elif ch3==2:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR PAYING ELECTRIC BILL --- \n\n")
                provider = input("ENTER YOUR ELECTRIC PROVIDER NAME : ")
                ca_no = int(input("ENTER YOUR CONSUMER ACC. NUMBER : "))
                bill_amt=float(input("ENTER BILL AMOUNT : "))
                print("\n\tYOUR BILL FOR C/A NO. ",ca_no, " AMOUNTING Rs ",bill_amt," IS SUCCESSFULLY PAID !! \n")
                print("YOUR TRANSACTION  ID IS : ",TID)
                print("\n\tTHANK YOU FOR US.....\n")
                
            elif ch3==3:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR PAYING GAS BILL --- \n\n")
                provider = input("ENTER YOUR GAS PROVIDER NAME : ")
                ca_no = int(input("ENTER YOUR CONSUMER ACC. NUMBER : "))
                bill_amt=float(input("ENTER BILL AMOUNT : "))
                print("\n\tYOUR BILL FOR C/A NO. ",ca_no, " AMOUNTING Rs ",bill_amt," IS SUCCESSFULLY PAID !! \n")
                print("YOUR TRANSACTION  ID IS : ",TID)
                print("\n\tTHANK YOU FOR US.....\n")
            elif ch3==4:
                exit()
            else:
                print("\n\nPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 4 !\n\nTRY AGAIN WITH VALID CHOICE ...")
                
                
                
                
                
                
                
                
                
                
                
            
            
        elif choice == 4:
            print("\n\n")
            print("\tWELCOME TO INCOME TAX  ZONE ...\n")
            print("1. PAY YOUR INCOME TAX .")
            print("2. EXIT .")
            ch4 = int(input("\nENTER YOUR CHOICE : "))
            
            if ch4 == 1:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR INCOME TAX  PAYMENT \n\n")
                ac_no = int(input("ENTER YOUR ACCOUNT NUMBER : "))
                pan_no = input("ENTER YOUR  PAN NUMBER : ") 
                tax_amt=int(input("ENTER TAX  AMOUNT TO PAY : "))
                print("THANK YOU FOR PAYING INCOME TAX ....")
                print("\n\tYOUR TAX FOR PAN NO -  ",pan_no,"AMOUNT TO Rs ",tax_amt," IS SUCCESSFULLY PAID !! \n") 
                print("YOUR TRANSACTION  ID IS : ",TID)
                print("\nTHANK YOU FOR USING OUR SERVICE.....\n")
                
            elif ch4==2:
                exit()
            else:
                print("\n\nPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 2 !\n\nTRY AGAIN WITH VALID CHOICE ...")
            
            
            
            
            
        elif choice == 5:
            print("\n\n")
            print("\tWELCOME TO PAY INSURANCE PREMIUM  ZONE ...\n")
            print("1. PAY INSURANCE PREMIUM .")
            print("2. EXIT .")
            
            ch5 = int(input("\nENTER YOUR CHOICE : "))
            if ch5 == 1:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR PAYING YOUR INSURANCE PREMIUM \n\n")
                premium_name = input("ENTER YOUR PREMIUM NAME : ")
                premium_no = int(input("ENTER YOUR  PREMIUM NUMBER : ") )
                premium_amt=int(input("ENTER PREMIUM AMOUNT TO PAY : "))
                print("\n\tYOUR PREMIUM FOR PREMIUM NO. -  ",premium_no,"AMOUNTING  Rs ",premium_amt," IS SUCCESSFULLY PAID !! \n") 
                print("YOUR TRANSACTION  ID IS : ",TID)
                print("\nTHANK YOU FOR USING OUR SERVICE.....\n")
                
            elif ch5==2:
                exit()
            else:
                print("\n\nPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 2 !\n\nTRY AGAIN WITH VALID CHOICE ...")
            
            
            
            
        elif choice == 6:
            print("\n\n")
            print("\tWELCOME TO LOAN'S  ZONE ...\n")
            print("1. APPLY FOR LOAN .")
            print("2. EXIT .")
            
            ch6 = int(input("\nENTER YOUR CHOICE : "))
            if ch6 == 1:
                print("\n\n")
                print("ENTER YOUR DETAILS FOR LOAN APPLY \n\n")
                ac_no = int(input("ENTER YOUR ACCOUNT NUMBER WITH US: "))
                pan_no = input("ENTER YOUR PAN NO. : ")
                amount=int(input("ENTER AMOUNT FOR LOAN : "))
                print("\n\tTHANKS FOR APPLYING FOR LOAN \n")
                print("KINDLY UPLOAD & VERIFY THE REQUIRED DOCUMENT ON LINK SHARED WITH YOUR CONTACT NO. ")
                print("YOUR REFERENCE  NO. IS : ",FN)
                print("\nWE WILL CREDIT Rs ",amount," IN YOUR A/C NO. - ",ac_no," WITHIN 48 HOURS , ONCE YOUR DOCUMENT GETS VERIFIED !!")
                
                
            elif ch6==2:
                exit()
            else:
                print("\n\nPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 2 !\n\nTRY AGAIN WITH VALID CHOICE ...")
            
            
            
            

            
        elif choice == 7:
            exit()
            
        else:
            print("\n\n\tPLEASE ENTER A VALID CHOICE BETWEEN 1 TO 7 !\n\nTRY AGAIN WITH VALID CHOICE ...\n\n")
            
            
            
            
            
            
        
else:
    print("\n\tWRONG PIN CODE !\t\n\n\tTRY AGAIN WITH VALID PIN CODE \t")





