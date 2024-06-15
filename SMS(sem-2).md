# Student Management System (SMS) Second Semester projects


#include <iostream>
#include<stdlib.h>
#include <string>
#include<fstream>
#include<conio.h>
#include<cstdlib>
#include<cmath>
#include <iomanip>
#include <windows.h>



using namespace std;

class password
{
    public:

    void pass()
    {
         
    string username;
    string Password;
    int loginAttempt = 0;

    while (loginAttempt < 3)
    {
        
        
        cout<<"\t\t\t\t\t\tWELCOME TO THE STUDENT INFORMATION SYSTEM OF AMITY SCHOOL \n\n\n";
        
        cout << "\t\t\tPlease enter your user name: ";
        cin >> username;
        
        cout << "\t\t\tPlease enter your user password: ";
        cin >> Password;

        if (username == "abhishek" && Password == "abhishek")
        {
            cout << "Welcome back ABHISHEK SHARMA!\n";
            break;
        }
        else if (username == "sumit" && Password == "sumitpat")
        {
            cout << "Welcome back SUMIT PATHWAR!\n";
            break;
        }
        else if (username == "vivek" && Password == "vivekdha")
        {
            cout << "Welcome back VIVEK DHAKAR!\n";
            break;
        }
        else
        {
            cout << "Invalid login attempt. Please try again.\n" << '\n';
            loginAttempt++;
        }
    }
    if (loginAttempt == 3)
    {
            cout << "Too many login attempts! The program will now terminate...... \n try again later";
            exit(0);
            
          
    }

    cout << "Thank you for logging in.\n";
    }

////////////////faculty
void passfac()
    {
         
    string username;
    string Password;
    int loginAttempt = 0;

    while (loginAttempt < 3)
    {
        
        
        cout<<"\t\t\t\t\t\tWELCOME TO THE STUDENT INFORMATION SYSTEM OF AMITY SCHOOL \n\n\n";
        
        cout << "\t\t\tPlease enter your user name: ";
        cin >> username;
        
        cout << "\t\t\tPlease enter your user password: ";
        cin >> Password;

        if (username == "nikhlesh" && Password == "nikhlesh")
        {
            cout << "Welcome back Dr. NIKHLESH PATHIK!\n";
            break;
        }
       
        else
        {
            cout << "Invalid login attempt. Please try again.\n" << '\n';
            loginAttempt++;
        }
    }
    if (loginAttempt == 3)
    {
            cout << "Too many login attempts! The program will now terminate...... \n try again later";
            exit(0);
            
          
    }

    cout << "Thank you for logging in.\n";
    }
};



class student_info
{
 public:

    string name;
    string full_name;
    string father_name;
    string uni_name;
    string caurse;
    int roll_no;
    int dd ,mm,yyyy;
    string grade;
    string result;
    float per;
    int phy;
    int chem;
    int maths;
    int cse;
    int total;
    int age;
    char gender;
    string address;
    string contactNo;
    string department;
    string  sec,branch;
    string doep,doem ,doec,doecs;

    ///////////////////////////////////basic information class this class contain information about the student////////////////

 
		
	public:

		void basic_info()
		{
			int n;
            
            system("CLS");
			cout<<"\n\t+----------------------------------------------------------------------------------------+";               //
   		 	cout<<"\n\t|                            BASIC INFORMATION FOR STUDENT                              |";
   		 	cout<<"\n\t+----------------------------------------------------------------------------------------+\n";

   		 	cout<<"\n\t\tEnter first name of the student                :: ";
   		 	cin>>name;
   		 	cout<<"\n\t\tEnter sur-name of the student                  :: ";
   		 	cin>>full_name;
   		 	cout<<"\n\t\tEnter father name of the student               :: ";
   		 	cin>>father_name;
   		 	cout<<"\n\t\tEnter residential address of the student       :: ";
   		 	cin>>address;

   		 	do
   		 	{
   		 		
	   		 	cout<<"\n\t\tEnter contact number of the student's family   :: ";
	   		 	cin>>contactNo;
	   		 	n=0;
	   		 	if(contactNo.length()<10 || contactNo.length()>10)
	   		 	{
					cout<<"\nERROR : contact number must be of 10 digits ";
					++n;
	   			}
   		    }
            while(n);
   		 	
            cout<<"\n\t\t-->> Enter Birth Date (DD/MM/YY) : ";
   cin>>dd>>mm>>yyyy;
    try
   {
    if(dd>31)
    {
        throw dd;

        cout<<"something went wrong";
    }
   }
   catch(int c)
   {
    cout<<"\t\tdate can't be :"<<c<<"\nenter date again : ";
    
    cin>>dd;
   }
    try
   {
    if(mm>12)
    {
        throw mm;

        cout<<"something went wrong";
    }
   }
   catch(int p)
   {
    cout<<"\t\tmonth can't be :"<<p<<"\nenter month again : ";
    
    cin>>mm;
   }
    try
   {
    if(yyyy>2023)
    {
        throw chem;

        cout<<"something went wrong";
    }
   }
   catch(int a)
   {
    cout<<"\t\tyear can't be :"<<a<<"\nenter year again : ";
    
    cin>>yyyy;
   }
   		 	cout<<"\n\t\tEnter university name                          :: ";
   		 	cin>>uni_name;
   		 	cout<<"\n\t\tEnter gender of the student                    :: ";
   		 	cin>>gender;
   		 	cout<<"\n\t\tEnter age of the student                       :: ";
   		 	cin>>age;
   		 	
   		}
		
		void display_basic()
		{
            system("CLS");
            
			cout<<"\n\t+----------------------------------------------------------------------------------------+";               //
   		 	cout<<"\n\t|                             BASIC INFORMATION OF STUDENT                              |";
   		 	cout<<"\n\t+----------------------------------------------------------------------------------------+\n";
            cout<<"\n\t**+\n";
            cout<<"\n\t\tStudent name is ::"<<name<<" "<<full_name;
            cout<<"\n\t**+\n";
   		 	cout<<"\n\t\tFather's name of the student is:: "<<father_name;
            cout<<"\n\t**+\n";
            
   		 	cout<<"\n\t\tResidential address of the student :: "<<address;
            cout<<"\n\t**+\n";
            
   		 	cout<<"\n\t\tContact number of student's family :: "<<contactNo;
            cout<<"\n\t**+\n";
            
   		 	//cout<<"\n\t\tDate of Birth of the student :: "<<DoB;
   		 	cout<<"\n\t\tUniversity name :: "<<uni_name;
            cout<<"\n\t**+\n";
            
   		 	cout<<"\n\t\tGender of the student :: "<<gender;
            cout<<"\n\t**+\n";
            
			cout<<"\n\t\tAge of the student :: "<<age; 
            cout<<"\n\t**+\n";
            
		}
        
};

/*ABOVE CODE CONTAINS THE BASIC INFORMATION ABOUT A STUDENT IN CLASS NAME AS student_info THIS CLASS IS 
THE MAIN CLASS FOR THE STUDENT MANAGEMENT SYSTEM AND THIS CLASS IS INHERITED TO MARKSHEET AND ALL OTHER IMP CLASSES*/

///////////STUDENT MARKSHEET PROGRAM///////////////////

class Mstudent : virtual public student_info
{

    //////////public members///////////////

    public:
    void main_menu();
    void add_data();
    void display();
    void deleted();
    

};

void Mstudent::main_menu()
{
    start:
    system("cls");
    int choice;
    char n;
    cout<<"\n\n\t\t\t\t-------------------------------------"<<endl;
	cout<<"\t\t\t\t |    STUDENT MANAGEMENT SYSTEM    | "<<endl;
    cout<<"\t\t\t\t-------------------------------------"<<endl;	
    cout<<"\t\t\t\t 1. Enter New Record "<<endl;
    cout<<"\t\t\t\t 2. display Record "<<endl;
    cout<<"\t\t\t\t 3. Delete Record "<<endl;
    cout<<"\t\t\t\t 4. Exit "<<endl;
    
    cout<<"\t\t\t\t-------------------------------------"<<endl;
    cout<<"\t\t\t\t  Choose Option : [ 1 / 2 / 3 / 4 ]"<<endl;
    cout<<"\t\t\t\t-------------------------------------"<<endl;
    cout<<" <<-->> Please Enter Your Choice : ";
    cin>>choice;

    switch(choice)
    {
        case 1:
        do
        {
            add_data();
            cout<<"\n --- Add new student or/ record (Y/N)";
            cin>>n;
        } while (n=='Y' || n=='y');
        break;

        case 2:
        display();
        break;

        case 3:
        deleted();
        break;

        case 4:
        exit(0);
       break;
        default:
    
        cout<<"\n -->> oops invalid choice please try again later"<<endl;
    }
        getch();
        goto start;
    
}

///////////add student function to enter the details of student///////////
void Mstudent:: add_data()
{
    fstream file;

   system("cls");
   cout<<"-----------------------------------------------------------------------------------------------------------------------"<<endl;	
   cout<<"\t\t\t\t\t\t | Add Student Details |"<<endl;
   cout<<"-----------------------------------------------------------------------------------------------------------------------"<<endl;
   
   cout<<"\t\t\t-->> Enter Your Name : ";
   cin>>name;
   cout<<"\t\t\t-->> Enter your surname Name : ";
   cin>>full_name;
   cout<<"\t\t\t-->> Enter Father Name : ";
   cin>>father_name;
   cout<<"\t\t\t-->> Enter collage Name : ";
   cin>>uni_name;
   cout<<"\t\t\t-->> Enter Course Name : ";
   cin>>caurse;
   cout<<"\t\t\t-->> Enter Roll Number  : ";
   cin>>roll_no;
   
   cout<<"\t\t\t-->> Enter Birth Date (DD/MM/YY) : ";
   cin>>dd>>mm>>yyyy;
    try
   {
    if(dd>31)
    {
        throw dd;

        cout<<"something went wrong";
    }
   }
   catch(int c)
   {
    cout<<"\t\tdate can't be :"<<c<<"\nenter date again : ";
    
    cin>>dd;
   }
    try
   {
    if(mm>12)
    {
        throw mm;

        cout<<"something went wrong";
    }
   }
   catch(int p)
   {
    cout<<"\t\tmonth can't be :"<<p<<"\nenter month again : ";
    
    cin>>mm;
   }
    try
   {
    if(yyyy>2023)
    {
        throw chem;

        cout<<"something went wrong";
    }
   }
   catch(int a)
   {
    cout<<"\t\tyear can't be :"<<a<<"\nenter year again : ";
    
    cin>>yyyy;
   }
    
    
   ////////marks of subjects ////////
   cout<<"\t\t\t-----------------------------------------------"<<endl;	
   cout<<"\t\t\t\t Enter Your Marks Subject Wise "<<endl;
   cout<<"\t\t\t-----------------------------------------------"<<endl;	
   total=0;
   cout<<"\t\t\t-->>PHYSICS  : ";
   cin>>phy;
   try
   {
    if(phy>100)
    {
        throw phy;

        cout<<"something went wrong";
    }
   }
   catch(int p)
   {
    cout<<"\t\tphysics marks can't be :"<<p<<"\nenter physics marks again : ";
    cin>>phy;
   }
   
   cout<<"\t\t\t-->> CHEMISTRY : ";
   cin>>chem;

   try
   {
    if(chem>100)
    {
        throw chem;

        cout<<"something went wrong";
    }
   }
   catch(int c)
   {
    cout<<"\t\tchemistry marks can't be :"<<c<<"\nenter chemistry marks again : ";
    
    cin>>chem;
   }
   cout<<"\t\t\t-->> MATHS : ";
   cin>>maths;

   try
   {
    if(maths>100)
    {
        throw maths;

        cout<<"something went wrong";
    }
   }
   catch(int m)
   {
    cout<<"\t\tmaths marks can't be :"<<m<<"\nenter maths marks again : ";
    
    cin>>maths;
   }
   cout<<"\t\t\t-->> COMPUTER SCIENCE  : ";
   cin>>cse;
   try
   {
    if(cse>100)
    {
        throw cse;

        cout<<"something went wrong";
    }
   }
   catch(int cs)
   {
    cout<<"cse marks can't be :"<<cs<<"\nenter CSE marks again : ";
    cout<<"enter maths marks again";
    cin>>cse;
   }
   

   
   ////calculation of total marks & % percentage///
   total= phy+chem+maths+cse;
   per= total/4;

   if(per>=80)
   {
   	 grade="A";
   	 result="PASS";
 //    cout<<"passed with first devision";

   }
   else if(per>=60)
   {
   	grade="B";
   	result="PASS";
    //cout<<"passed with second devision";
   }
   else if(per>=35)
   {
   	grade="C";
   	result="PASS";
  //  cout<<"passed with third devision";

   }
   else
   {
   	grade="-";
   	result="FAIL";
    
   }

                           //creating a file projectmain.txt to store the record of students//

   file.open("projectmain.txt" ,ios::out | ios::app);
  // file>>"  ">>name>>"  ">>full_name>>"  ">>father_name>>"  ">>uni_name>>"  ">>caurse>>"  ">>roll_no>>"  ">>dd>>"  ">>mm>>"  ">>yyyy>>"   ">>grade>>"  ">>result>>"  ">>per>>"  ">>phy>>"  ">>chem>>"  ">>maths>>"  ">>cse>>"  ">>total;
   file<<"||\n"<<name<<""<<full_name<<"||"<<father_name<<"||"<<uni_name<<"||\n "<<caurse<<"|| "<<roll_no<<" "<<dd<<" /"<<mm<<"/ "<<yyyy<<" ||"<<cse<<" ||"<<maths<<"|| "<<phy<<"|| "<<chem<<"||\n "<<total<<" ||"<<result<<" ||"<<per<<" ||"<<grade<<"\n";
   file.close();
}

                                                     // display functon//
void Mstudent::display()
{
    system("cls");
    fstream file;

   cout<<"\t\t-----------------------------------------------------------------------------------------------------------------------"<<endl;	
   cout<<"\t\t|\t\t\t\t\t\t | Student Result Table |"<<endl;
   cout<<"\t\t-----------------------------------------------------------------------------------------------------------------------"<<endl;
   
   file.open("projectmain.txt",ios::in);
   if(!file)
   {
      cout<<"\n\t\t\t No Data Is Found ......";
	  file.close();	
   
   }
   else
   {
    /// file>>name>>full_name>>father_name>>uni_name>>caurse>>roll_no>>dd>>mm>>yyyy>>grade>>result>>per>>phy>>chem>>maths>>cse>>total;
   ///while(!file.eof())
  // {
  
   		 cout<<"\t\t\t COLLAGE  : "<<uni_name<<endl;
   		 
   		 
   		 cout<<"\n\n\t\t\t STUDENT'S NAME : "<<name;
   		 cout<<"\t\t\t\t\t\t\t ROLL NO : "<<roll_no<<endl;
   		 
   		 cout<<"\t\t\t\t\t\t\t                   DATE OF BIRTH : "<<dd<<" / "<<mm<<" / "<<yyyy<<endl;
   		 cout<<"\n\t\t\t FATHER'S NAME : "<<father_name;
   		 
   		 
   		 cout<<"\n\t\t\t+----------------------------------------------------------------------------------------+";               //whole structure of the result table........
   		 cout<<"\n\t\t\t|   Subject Name      |\t  Marks Obtained  |\tOut-Of   |  Percentage   |\tGrade    |";
   		 cout<<"\n\t\t\t+----------------------------------------------------------------------------------------+";
   		 cout<<" \n\t\t\t|  MATHEMATICS        |\t      "<<maths<<"  \t  |\t "<<100 <<"     |"<<"\t\t |"<<"\t\t |"<<endl;
   		 cout<<"  \t\t\t|  PHYSICS            |\t      "<<phy<<"     \t  |\t "<<100 <<"     |"<<"\t\t |"<<"\t\t |"<<endl;
   		 cout<<"  \t\t\t|  CHEMISTRY          |\t      "<<chem<<"     \t  |\t "<<100 <<"     |"<<"\t"<<per<<"%      |\t"<<grade<<"\t |"<<endl;
   		 cout<<"  \t\t\t|  COMPUTER SCIENCE   |\t      "<<cse<<"     \t  |\t "<<100 <<"     |"<<"\t\t |"<<"\t\t |"<<endl;
   		 
   		 cout<<"\t\t\t+----------------------------------------------------------------------------------------+\n";
   		 cout<<"\n\t\t\t\t\t Total - "<<total<<"\t\t\t\t\t RESULT - "<<result<<endl;
   	
   		cout<<"\n\t\t\t\t Date : "<<_DATE_<<endl;
   		cout<<"\t\t\t\t\t\t\t\t\t\t  Principle Signatures : "<<endl;
   		
   		cout<<"\n\n\t----------------------------------------------------------------------------------------------------------------------------------";
   		file>>name>>full_name>>father_name>>uni_name>>caurse>>roll_no>>dd>>mm>>yyyy>>grade>>result>>per>>phy>>chem>>maths>>cse>>total;
   }
   
file.close();
   
}

                                                       ///delete student////////
void Mstudent::deleted()
{
    system("cls");
    system("color 24");
    fstream file,file1;
    int roll_no;
    int found=0;

   cout<<"-----------------------------------------------------------------------------------------------------------------------"<<endl;	
   cout<<"\t\t\t\t\t\t | Delete Student Record |"<<endl;
   cout<<"-----------------------------------------------------------------------------------------------------------------------"<<endl;
   

   file.open("projectmain.txt",ios::in);
   if(!file)
   {
    cout <<"\n\t\t\t\t\tNo data is found.............";
    file.close();

   }
   else
   {
    cout<<"\n\t\t\t--->>Enter the roll number of the student whose data you want to delete";
    cin>>roll_no;

    file.open("temp.txt",ios::out | ios::app);

file>>name>>full_name>>father_name>>uni_name>>caurse>>roll_no>>dd>>mm>>yyyy>>grade>>result>>per>>phy>>chem>>maths>>cse>>total;

   while(!file.eof())
   {
	if(roll_no!=roll_no)
    
    {
       file1<<" "<<name<<" "<<full_name<<" "<<father_name<<" "<<uni_name<<" "<<caurse<<" "<<roll_no<<" "<<dd<<" "<<mm<<" "<<yyyy<<" "<<cse<<" "<<maths<<" "<<phy<<" "<<chem<<" "<<total<<" "<<result<<" "<<per<<" "<<grade<<"\n";
   
    }
    else
    {
        found++;
        cout<<"\n\t\t\t Record is deleted successfully...........";
        file.close();
		file1.close();
		
		remove("projectmain.txt");
		rename("temp.txt","projectmain.txt");
        main_menu();
    }

    file>>name>>full_name>>father_name>>uni_name>>caurse>>roll_no>>dd>>mm>>yyyy>>grade>>result>>per>>phy>>chem>>maths>>cse>>total;
   }
   main_menu();
   if(found==0)
		{
			cout<<"\n\t\t\t Student Roll Number Is Not found...!!! ";
		}
		//file.close();
		//file1.close();
		
		//remove("projectmain.txt");
		//rename("temp.txt","projectmain.txt");
        
   }
   
}                                               
                                                     /examination class/


class exams :virtual public student_info

{  
    public:
      
    void date_of_exam()
    {
         system("color 68");
        cout<<"\n\t\t\t\t\t:::::::::AMITY UNIVERSITY MADHYPRADESH::::::::::::::::";
        cout<<"\n\t\t\t\tFINAL EXAM SCEDULE FOR UG CAURSES IN ASET";

        cout<<"\nEnter the date of the physics exam: ";
        cin>>doep;
        cout<<"\nEnter the date of the chemistry exam: ";
        cin>>doec;

        cout<<"\nEnter the date of the mathematics exam: ";
        cin>>doem;
      //  cout<<"..................................................................................................";
        cout<<"\nEnter the date of the computer science exam: ";
        cin>>doecs;


    }

void put_date()
{
    system("cls");

cout<<"\n||--------------------------------------------------------------------------------------------------||";
cout<<"\n||                                            Exam dates are                                        ||";
cout<<"\n||..................................................................................................||";
cout<<"\n||date of physics exam are:                            "<<doep<<"                                   ||";
cout<<"\n||..................................................................................................||";
cout<<"\n||date of chemistry exam are:                          "<<doec<<"                                   ||";
cout<<"\n||..................................................................................................||";
cout<<"\n||date of maths exam are:                              "<<doem<<"                                   ||";
cout<<"\n||..................................................................................................||";
cout<<"\n||date of computer science exam are:                   "<<doecs<<"                                  ||";
cout<<"\n||..................................................................................................||";

}

};

                                              /RESULTS/
                                      
class result :public exams ,public Mstudent
 {
    public:
    string name ,grade,result;
    float phy,mat,cse,ece,per,total;

    void getmarks();
    void showmarks();

};   
void result::getmarks()
{
      cout<<"enter your name"<<endl;
      cin>> name;
      cout<<"enter your Physics marks"<<endl;
      cin>>phy;
      cout<<"enter your Maths marks"<<endl;
      cin>>maths;
      cout<<"enter your Cse marks"<<endl;
      cin>>cse;
      cout<<"enter your chemistry marks"<<endl;
      cin>>chem;
      total=phy+mat+cse+chem;
      per=total/4;
}

void result::showmarks()
{
    cout<< "name ------- "<<name<<endl;
    cout<<"-------------------------------------------------------------------"<<endl;
    cout<<"subject                      |                             marks"<<endl;
    cout<<"-------------------------------------------------------------------"<<endl;
  
    cout<<"phyics                       |                          "<<phy<<endl;
    cout<<"maths                        |                          "<<maths<<endl;
    cout<<"cse                          |                          "<<cse<<endl;
    cout<<"chemistry                    |                          "<<chem<<endl;
    cout<<"------------------------------------------------------------------------"<<endl;
    cout<<"total                        |                          "<<total<<endl;
    cout<<"percentage                   |                          "<<per<<endl;

    

   if(per>=80)
   {
   	 grade="A";
   	 result="PASS";
 //    cout<<"passed with first devision";

   }
   else if(per>=60)
   {
   	grade="B";
   	result="PASS";
    //cout<<"passed with second devision";
   }
   else if(per>=35)
   {
   	grade="C";
   	result="PASS";
  //  cout<<"passed with third devision";

   }
   else
   {
   	grade="-";
   	result="FAIL";
    
   }

   cout<<"grade:                                        "<<grade<<endl;
   cout<<"result                                        "<<result<<endl;

 }
             
                                       /ACCOUNTS/
                                       
 class Account :public student_info
{
	//protected:
   
                                        /ACCOUNTS/

    public:
		
		int fees;
		int T_fees;       //TOTAL FEES
		int f_fine;       //FINE ON LATE FEES DEPOSITE 
		int D_fine;       //FINE ON DAMAGING OR BROKING ANY UNIVERSITY PROPERTY 
		int T_fine;       //TOTAL FINE
		int Ex_days;      //NUMBER OF EXTENDED DAY'S FROM THE LAST DAY OF FEES SUBMMITION
		int n_sem;        //NUMBER OF SEMESTER STUDYING IN
        int inst1,inst2,inst3,n_inst;   //inst FOR INSTALMENT 1,2&3
        char inst_d;
		//string caurse;
		int s_deposite;   //SECURITY DEPOSITE
		char fees_d;      //FEES DEPOSITED OR NOT 
		
	public:
		
		 void Acc()
		{ 
            int n;

			s_deposite = 15000;
			n_inst=0;
			cout<<"\n\n\t+----------------------------------------------------------------------------------------+";               //
   		 	cout<<"\n\t|                              FEES INFORMATION OF STUDENT                              |";
   		 	cout<<"\n\t+----------------------------------------------------------------------------------------+\n";
   		 	
            
   		 	cout<<"\n\t\tEnter student  name   :: ";
			cin>>name;
            
   		 	cout<<"\n\t\tEnter student Father's name   :: ";
			cin>>father_name;
            do
   		 	{
   		 		
	   		 	cout<<"\n\t\tEnter contact number of the student   :: ";
	   		 	cin>>contactNo;
	   		 	n=0;
	   		 	if(contactNo.length()<10 || contactNo.length()>10)
	   		 	{
					cout<<"\nERROR : contact number must be of 10 digits ";
					++n;
	   			}
   		    }
            while(n);

            cout<<"\n\t\tEnter student roll number   :: ";
			cin>>roll_no;
   		 	
            cout<< "\n\t\t Enter student's department name:: ";
            cin>>department;

            cout<< "\n\t\tEnter students residential address ::";
            cin>>address;

   		 	cout<<"\n\t\tEnter course   :: ";
			cin>>caurse;
			cout<<"\n\t\tEnter semester :: ";
			cin>>n_sem;
			
   		 	if(caurse=="Btech"||caurse=="btech")
   		 	fees=95000;
   		 	else if(caurse=="Mtech"||caurse=="mtech")
   		 	fees=120000;
   		 	else if(caurse=="Mba"||caurse=="mba")
   		 	fees=110000;
   		 	else if(caurse=="Bba"||caurse=="bba")
   		 	fees=55000;
   		 	else if(caurse=="Bca"||caurse=="bca")
   		 	fees=50000;
   		 	else if(caurse=="Mca"||caurse=="mca")
   		 	fees=70000;
   		 	else
   		 	{
   		 		cout<<"\n\tAMITY UNIVERSITY DOES NOT PROVIDES THE COURSE YOU HAVE ENTERED";
                cout<<"\n\tPLEASE ENTER CORRECT COURSE",Acc();
   		 		
   			}
   		 	T_fees = fees+fees*(n_sem*5)/1000;
   		 	
   		 	fine();
   		 	
   		 	int i;
   		 	
   		 	cout<<"\n\t\tIf you want to go with the EMI scheme \n\t\tfor fees installment enter 1\t\t\t      ::";
   		 	cin>>i;
   		 	
			if(i==1)
			EMI();
			T_fees = T_fees+T_fine;
			
   		 	cout<<"\n\n\t\tTOTAL FEES OF THE STUDENT                         :: "<<T_fees;
   		 	if(i==1)
			{
	   		 	cout<<"\n\t\tEnter (P) to pay the first instalment";
	   		 	cout<<"\n\t\tof your fees                                              :: ";
	   		 	cin>>inst_d;
	   		 	if(inst_d=='p'||inst_d=='P')
	   		 		++n_inst;
	   		 	if	(inst_d=='p'||inst_d=='P')
				{				
		   		 	cout<<"\n\t\tEnter (P) to pay the second instalment";
		   		 	cout<<"\n\t\tof your fees                                              :: ";
		   		 	cin>>inst_d;
                    
		   		 	if(inst_d=='p'||inst_d=='P')
		   		 		++n_inst;
		   		 		
		   		 		if(inst_d=='p'||inst_d=='P')
		   		 	if(inst3>0)
		   		 	{
			   		 	cout<<"\n\t\tEnter (P) to pay the third instalment";
			   		 	cout<<"\n\t\tof your fees                                          :: ";
			   		 	cin>>inst_d;
			   		 	if(inst_d=='p'||inst_d=='P')
			   		 		++n_inst;
		   		 	}
				}
   		 	
			}
   		 	else{				
   		 	cout<<"\n\n\t\tEnter (P)to pay fees right now                   ";
   		 	cout<<"\n\t\telse enter(NO)                                      ::";
			cin>>fees_d;
			}
   		 	feesof();
		}
		
		void EMI()
		{
			char n;
			
			inst1=inst2=inst3=0;
			
			cout<<"\n\t\tWe have two EMI schemes\n";
			cout<<"\n\t\t1:\tTwo times instalment with 10% interest";
			cout<<"\n\t\t2:\tThree times instalment with 15% interest\n";
			
			cout<<"\n\t\tChoose the plane wisely according to your perfect fit  ::";
			cin>>n;
			
			switch(n)
			{
				case '1':inst1=(T_fees+T_fees*0.1)/2;
						inst2=inst1;
						break;
				case '2':inst1=(T_fees+T_fees*0.15)/3;
						inst3=inst2=inst1;
						break;
				default: cout<<"\n\n\t\tYOU HAVE ENTERED SOMETHING WRONG PLEASE DO IT AGAIN";
						EMI();
			}
			
		}
		
		void fine()
		{
			cout<<"\n\t\tNumber of extended days from the last day of fees   ";
			cout<<"\n\t\tsubmission if not enter 0                               ::";
			cin>>Ex_days;                                                    
			switch(Ex_days)        
			{
				case 0 :f_fine=0;
				 break;
				case 1 :f_fine=500;
				 break;
				case 2 :f_fine=1000;                                         
				 break;
				case 3 :f_fine=1500;
				 break;
				case 4 :f_fine=2000;
				 break; 
				case 5 :f_fine=2500;
				 break; 
				case 6 :f_fine=3000;
				 break; 
				case 7 :f_fine=4000;
				 break;      
				default:f_fine=10000; 
			}
			
			cout<<"\n\t\tEnter amount of fine on student if any             ";
			cout<<"\n\t\telse enter=0                                       ::";
			cin>>D_fine;
			
			T_fine=f_fine+D_fine;
		}
		
		void feesof()
		{   
            
			char F,I;
			F=fees_d;
			I=inst_d;
			if(F=='p'||F=='P'||n_inst>0)
			{			
				
				cout<<"\n\n\t+----------------------------------------------------------------------------------------+";               //
	   		 	cout<<"\n\t|                                FEES RECEIPT OF STUDENT                                 |";
	   		 	cout<<"\n\t+----------------------------------------------------------------------------------------+\n";
	   		 	cout<<"\n\t\tReceipt No:-863207 ";
	   		 	cout<<"\n\t\tName                            :: "<<name;
	   		 	cout<<"\n\t\tfather's Name                   :: "<<father_name;
	   		 	cout<<"\n\t\tContact No.                     :: "<<contactNo ;
	   		 	cout<<"\n\t\tRecidential Address             :: "<<address;
	   		 	cout<<"\n\t\tRoll No.                        :: "<<roll_no;
	   		 	cout<<"\n\t\tDepartment                      :: "<<department;
	   		 	cout<<"\n\t\tCourse                          :: "<<caurse;
				cout<<"\n\t\tTotal Amount of fees            :: "<<T_fees;
				if(n_inst)
				{
					cout<<"\n\t\tNo. of instalment paid are      :: "<<n_inst;
					cout<<"\n\t\tTotal fees paid with interest is :: "<<n_inst*inst1;
				}	 
	   		 	cout<<"\n\t+----------------------------------------------------------------------------------------+\n";
	   		 	
			}
			else
		
			cout<<"\n\tFEES NOT PAID  TOTAL PAYABLE AMOUNT    :: "<<T_fees;
			
		}
		
};
 
                               ////////////ATTENDANCE OF STUDENT SYSTEM/////////////////


class attendance :public student_info
{

    public:
    int present = 0, total = 0;
    public:
        void enter();
        void calculate();  
        void fileattend();  
};

void attendance::enter()
{
    fstream file;
    system("color B1");
    int date, month, year;
    int nop;   // no of periods
    int i;
    int a;     //attendance each period
    int check;    //checking valid date
    int k[20];  
    
    cout << "enter any number to give the date" << endl;
    cin >> i;
    while(i)
    { 
        cout << "enter date/month/year" << endl;
        cin >> date >> month >> year;
       i=i-i;
       
        if(month == 1 || month == 3 || month == 5 || month == 7 || month == 8 || month == 10 || month == 12)
        {
            if(date > 31 || date == 0)
            {
              check = 0;
            }
            else
            {
                check = 1;
            }
            if(month == 4 || month == 6 || month == 9 || month == 11)
            {
                if(date > 30 || date == 0)
                {
                    check = 0;
                }
                else
                {
                    check = 1;
                }
                if(month == 2)
                {
                    if(date > 29 || date == 0)
                    {
                        check = 0;
                    }
                    else
                    {
                        check = 1;
                    }
                }
                if(month == 0 || year == 0 )
                {
                    check = 0;
                }
            }
        }
	}

    switch(check)
    {
        case 0:
            cout << "please enter valid date" << endl;
            cout << "enter date/month/year" << endl;
            cin >> date >> month >> year;
          break;
            
            case 1:
            cout << "date is valid" << endl;
          
        case 2:
            cout << "enter no. of periods in the day" << endl;
            cin >> nop;
            for (i = 1; i < nop + 1; i++)
            {
                cout << "enter '1'if present else '0' to update the attendance of period" << i << "::";
                cin >> a;

                if(a == 1)
                {
                    present++;
                    total++;
                    k[i] = 1;
                    cout << "student is present";
                }

                else
                {
                    total++;
                    k[i] = 0;
                    cout << "student is absent";
                }
            }
            cout << "attendance of the day is marked as:";

            for(i = 1; i < nop + 1; i++)
            {
                cout << "*";
            }
            cout << endl;
            cout << "MM/DD/YYYY";

            for(i = 1; i < nop + 1; i++)
            {
                cout << "P" << i << "  ";
            }
            cout << date << "/" << month << "/" << year << "";
            for(i = 1; i < nop + 1; i++)
            {
                if(k[i] == 1)
                {
                    cout << "P" << endl;
                }
                else
                {
                    cout << "A" << endl;
                }
            }
            for(i = 1; i < nop + 1; i++)
            {
                cout << "*";
            }
            break;

        default:
            exit(0);
    }
    cout << "enter 1 to mark attendance of another day else press 0";
    cin >> i;

} 
                                          ////////////Another function..............///////////////////

    void attendance::calculate() 
{
  // attendance attendance;
  fstream file;
   // ifstream infile;
   // ofstream outfile;
   // attendance.calculate();
    file.open("projectmain.txt");
    float percentage = (present * 100.0)/total;

    cout << "Attendance percentage: " << percentage << "%" << endl;

    if (percentage < 75 && percentage >= 65) 
    {
        int classes_to_attend = (int)ceil(total * 0.75 - present);

    cout << "You need to attend " << classes_to_attend << " more classes to improve your attendance." << endl;
    }
    else if (percentage < 65)
     {

        int classes_to_attend = (int)ceil(total * 0.65 - present);

        cout << "You need to attend " << classes_to_attend << " more classes to avoid being detained." << endl;
    
    }
    file.open("projectmain.txt" ,ios::out | ios::app);
     file<<"  "<<percentage;
    file.close();
    file>>percentage;
}


 void attendance ::fileattend() 
 {
    //attendance a;
    //a.enter();
    fstream file;
    int choice;
    attendance attendance;
   // ifstream infile;
   // ofstream outfile;

    cout << "STUDENT ATTENDANCE MAINTENANCE SYSTEM" << endl << endl;
    while (true)
     {
        cout << "Select an option:" << endl;
        cout << "0. View attendance" << endl;
        cout << "1. Update attendance" << endl;
        cout << "2. Exit" << endl;
        cin >> choice;
        
        switch (choice) 
        {
            case 0:
                attendance.calculate();
                file.open("projectmain.txt");
                if (!file) 

                {
                    cout << "Error: Unable to open file." << endl;
                    break;
                }

                file >> attendance.total >> attendance.present;
                
                file.close();
                break;

            case 1:

                attendance.enter();
                file.open("projectmain.txt");
                if (!file) 

                {
                    cout << "Error: Unable to open file." << endl;
                    break;
                }

                file << attendance.total << " " << attendance.present;
                file.close();
                break;

                default:
                cout << "Invalid choice." << endl;
                break;
        }
    }
    ///return 0;
}

//////////////////////////////////OTHERS////////////////////OTHERS////////////OTHERS///////////////////////////
/////////////////////////////TIME TABLE/////////////////////////////////////////////////
class others
{

public:
void static timetable()
{
         system("CLS");
    system("color 31");
	
	cout<<"\n\n|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||";
	cout<<"\n                                                    AMITY UNIVERSITY MADHYA PRADESH AMITY SCHOOL OF ENGINEERING & TECHNOLOGY                                               ";
	cout<<"\n|||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||\n";
	cout<<"\n_";
	cout<<"\n||DAY/TIME	|	09:15-10:10		|	10:15-11:10		|	11:15-12: 10	|	12: 15-01: 10	|	01:15-02:10		|	02:10-03:10		|	03: 15-04: 10	 | 	04: 15-05: 10 ||";
	cout<<"\n||-----------------------------------------------------------------------------------------------------------------------------------------------------------------------||";
	cout<<"\n||MONDAY	|   Minor Track/ 	|       EVS242      |   	BCU241  	|         L         |          CSE224 E2(Lab 112A)          |       CSE204       |	   ECE101     ||";
	cout<<"\n||         |   Specialization  |                   |                   |                   |         BME224 AI  [Wo0rkshop]        |                    |                ||";
	cout<<"\n||-----------------------------------------------------------------------------------------------------------------------------------------------------------------------||";
	cout<<"\n||TUESDAY  |     MAT201        |      LIB/CCA      |     BCU241        |         U         |        ECE121 A1 [Block C-204]        |       ECE101       |     PHY101     ||";
	cout<<"\n||         |                   |                   |                   |                   |        PHY121 A2 [Room No.102]        |                    |                ||";
	cout<<"\n||-----------------------------------------------------------------------------------------------------------------------------------------------------------------------||";
	cout<<"\n||WEDNESDAY|  Minor Track/     |   Minor Track/    |     BSU243        |         N         |          CSE224 A1 (Lab 112A)         |       PHY101       |     MAT201     ||";
	cout<<"\n||         |  Specialization   |   Specialization  |                   |                   |         BME224 A2  [Workshop]         |                    |                ||";
	cout<<"\n||-----------------------------------------------------------------------------------------------------------------------------------------------------------------------||";
	cout<<"\n||THURSDAY |     MAT201        |      CSE204       |      FLU244       |         C         |        ECE121 A1 [Block C-204]        |       ECE101       |     PHY101     ||";
	cout<<"\n||         |                   |                   |                   |                   |        PHY121 A2 [Room No.102]        |                    |                ||";
	cout<<"\n||-----------------------------------------------------------------------------------------------------------------------------------------------------------------------||";
	cout<<"\n||FRIDAY   |     MAT201        |      LIB/CCA      |     EVS242        |         H         |     PHY 101      |       CSE204       |      LIB/CCA       |    LIB/CCA     ||";
	cout<<"\n||_||";
	
}
};

                                                  /COURSES OFFERED IN UNIVERSITY/

class caurses
{
public:

void static caurse()
{  
     cout<<"================================================================================================= "<<endl;
	cout<<"  Courses                      Total Tuition Fees                        Eligibility"<<endl;
	cout<<"================================================================================================= "<<endl;
	cout<<"  B.E./B.Tech                    INR 2.6L-5.68L                       10+2 : 50-60%           "<<endl;
	cout<<"  (7 courses)                     (for 4 years)                       Exams:JEE Main,CBSE 12th "<<endl;
	cout<<"                                                                      MPBSE 12th               "<<endl;
	cout<<"_________________________________________________________________________________________________ "<<endl;
	cout<<"  B.Pharma                        INR 2.08L                            10+2: 50%              "<<endl;
	cout<<" (1 course)                      (for 4 years)                         Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"  B.A.LL.B                         INR 2.35L                           10+2: 50%              "<<endl;
	cout<<" (1 course)                      (for 5 years)                         Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"   BCA                          INR 1L-1.71L                           10+2: 50%              "<<endl;
	cout<<" (2 courses)                    (for 3 years)                          Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"  MCA                            INR 1L-3.32L                                                 "<<endl;
	cout<<" (1 course)                      (for 5 years)                           -                       "<<endl;
	cout<<"_"<<endl;
	cout<<"  B.A.                          INR 1L-1.77L                           10+2: 55%              "<<endl;
	cout<<" (6 courses)                      (for 3 years)                        Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"  B.sc                          INR 99K-1.65L                          10+2: 50%             "<<endl;
	cout<<" (5 courses)                     (for 3-5 years)                       Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"  B.Com                          INR 77K-1.71L                         10+2: 50%              "<<endl;
	cout<<" (2 courses)                      (for 3 years)                        Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl; 
	cout<<"  BBA                            INR 1L-4.26L                          10+2: 50%              "<<endl;
	cout<<" (3 courses)                      (for 3 years)                        Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl; 
	cout<<" MBA/PGDMA                        INR 1L-10.72L                        Graduation: 40%-50%       "<<endl;
	cout<<"(7 caurse)                      (for 2years)                           Exams:MAT,CAT,GMAT,CMAT,XAT"<<endl;
	cout<<"                                                                             NMAT                 "<<endl;
	cout<<""<<endl; 
	cout<<"  Ph.D.                          INR 2.35L                             10+2: 50%-60%              "<<endl;
	cout<<"                                                                       Graduation: 55%"         <<endl;
	cout<<"(22 course)                   (for 3 years-54 months)                  Exams:GATE,UGC NET,GPAT "<<endl;
	cout<<"                                                                              CSIR NET,ICMR JRF"<<endl;
	cout<<""<<endl;
	cout<<"  M.A.                           INR 1L-2.24L                          Graduation: 50%              "<<endl;
	cout<<"(4 course)                      (for 2 years)                                                      "<<endl;
	cout<<""<<endl;
	cout<<"  M.Sc.                           INR 1L-1.9L                          10+2: 50%              "<<endl;
	cout<<"(3 course)                      (for 2-5 years)                        Exams:CBSE 12th,MPBSE 12th "<<endl;
	cout<<"_"<<endl;
	cout<<"  M.Phil                          INR 4.52L                                                       "<<endl;
	cout<<"(1 course)                      (for 2 years)                            -                         "<<endl;
	cout<<""<<endl;
	cout<<"  B.Arch                         INR 1.95L                             10+2: 50%              "<<endl;
	cout<<"(1 course)                      (for 5 years)                          Exams:NATA              "<<endl;
	cout<<""<<endl; 
    cout<<"  LL.B.                          INR 1.38L                                                       "<<endl;
	cout<<"(1 course)                      (for 3 years)                             -                        "<<endl;
	cout<<""<<endl;
	cout<<" M.E./M.Tech                     INR 2.14L-3.16L                       10+2: 60%              "<<endl;
	cout<<"(6 course)                      (for 2 years)                          Graduation: 60%              "<<endl;
	cout<<""<<endl;  
	cout<<"                                                                                                  "<<endl;
	cout<<"                                                                                                  "<<endl;
	cout<<" THANK YOU    THANK YOU    THANK YOU   THANK YOU   THANK YOU   THANK YOU    THANK YOU    THANK YOU"<<endl;
	cout<<"===================================================================================================="<<endl;                                                                  
	                                                                  
	
}
};

                                         /CALENDER OF THE YEAR 2023 INCLUDES BASIC INFO/

class calender
 {
    // Define the number of months in a year and the number of days in each month
    public:
       
void calender1()
{
    system("CLS");
	const int M = 12;       //no of months in the year

    const int dw = 7;  //no of days per week

    const int dm[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31}; 

          //no of days in a particular month

    const string mn[] = {"January", "February", "March", "April", "May", "June","July", "August", "September", "October", "November", "December"};         
                                       
                                       /months name/

    const string wd[] = {
        "Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"
    };               
                                      /* week days*/

    int sd = 0; 

    cout << "\t\t\t\t==================== 2023 ====================" << endl;

    for (int m = 0; m < M; m++) 
    {
        
        cout << "\n--------------------- " << mn[m] << " ---------------------\n" << endl;

        
       	for(int i=0;i<7;i++)

		cout<<setw(10)<<wd[i]<<setw(10);

		cout<<endl;
        cout << endl;

        
        int daysInMonth = dm[m];

        if (m == 1 && ((2023 % 4 == 0 && 2023 % 100 != 0) || (2023 % 400 == 0))) 
        {
            daysInMonth = 29;
        }

         int day = 1;  

         for (int wd = 0; wd < dw; wd++) 
          {
            if (wd < sd)
             {
                cout << setw(10) << " ";
             } 

            else
             {
                cout << setw(10) << day;
                day++;
            }

          }
        cout << endl;

        while (day <= daysInMonth) 
        {
            for (int wd = 0; wd < dw && day <= daysInMonth; wd++) 
            {
                cout << setw(10) << day;
                day++;
            }
            cout << endl;
        }

          sd = (sd + daysInMonth) % dw;
    }

    cout << "====================================================" << endl;
	
    }
};

                                  /CALLING FUNCTION FOR FACULTY AND STUDENT/
class calling
{

public:

void faculty() 
{

     system("CLS");
    system("color 0F");
    
    password a;
     a.passfac();

     system("CLS");
    cout << "|-----------------------------------------------------------------------------------------------------------------------------------------|\n";
    cout << "|\t\t\t\t\t\tWELCOME TO THE FACULTY LOGIN SECTION\n";                                   
    cout << "|-----------------------------------------------------------------------------------------------------------------------------------------|\n";
      
      calling cg;
    student_info bi;
    Mstudent s;
    exams ex;
    Account fs;
    attendance at;
   others oth;
   caurses cau;
    result obj;
    calender c;
           
    int choice, rollNo;

 while (true)
  {
        cout << "|------------------------------------------------------------------------------------------------------------------------------------------\n";
        cout << "|            1.Main menu for marksheet                             |";
        cout << "|            2.Basic information\t\t\t\t\t  |\n\n";
        cout << "|            3.Display basic  information                          |";  
        cout << "|            4. Examination Dates and related information\t\t  |\n\n";
        cout << "|            5.View exam time table of exams                       |";
        cout << "|            6.Accounts and information of student\t\t\t  |\n\n";
        cout << "|            7.Reciept of deposited fees of student                |";
        cout << "|            8.Attendance of student\t\t\t\t  |\n\n";
        cout << "|-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-++-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-++-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-\n\n";
        cout << "|            9.Calculate attendance of student                     |";
        cout << "|            10.See the file of student\t\t\t\t  |\n\n";
        cout << "|            11.Results based on exams..                           |";
        cout << "|            12.Show results..\t\t\t\t\t  |\n\n";
        cout << "|            13.Time table of classes                              |";
        cout << "|            14.Courses available in university\t\t\t  |\n\n";
        cout << "|            15.Calender                                           |";
        cout << "|            16.student login via a faculty\t\t\t\t  |\n\n ";
        cout << "|           17.exit                                               ||                                                          \t         |\n\n ";
        cout << "|------------------------------------------------------------------------------------------------------------------------------------------\n";
        cout<<"Choose Option : [ 1 / 2 / 3 / 4 / 5 / 6 / 7/ 8/ 9 / 10 / 11 / 12 / 13 / 14 / 15 / 16 / 17  ]"<<endl;
        cin >> choice;
        
        switch (choice)
         {
            
            case 1:
                s.main_menu();
                break;

            
             case 2:
                bi.basic_info();
                break;

            case 3:
                 bi.display_basic();
                 break;  

            case 4:
                  ex.date_of_exam();
                  break;

            case 5:
                  ex.put_date();
                  break;      

            case 6:
                fs.Acc();
                 
                 break;
               
            case 7:
               fs.feesof();
                 break;


            case 8:
               at.enter();
              
            case 9:
               at.calculate();
               break;

            case 10:
               at.fileattend();
               break;

            case 11:
               obj.getmarks();
               break;
               
            case 12:
                obj.showmarks();
                break;

            case 13:
               oth.timetable();
                break;

            case 14:
               cau.caurse();
               break;
                
            case 15:
               c.calender1();
               break;
            
            case 16:
               cg.studen();
               break;
            case 17:
             exit(0);

            default:
                cout << "Invalid choice. Please try again.\n";
        }
    }

}

void studen()
{
    password a;
    a.pass();
     system("CLS");

     system("color 0F");

      cout<<"\t\t\t\t\t\tWELCOME TO THE STUDENT INFORMATION SYSTEM OF AMITY SCHOOL\n\n\n\n";
      cout<<"                  DATE:-"<<_DATE_<<endl;
      cout<<"                  TIME:-"<<_TIME_<<endl;
    student_info bi;
    Mstudent s;
    exams ex;
    Account fs;
    attendance at;
   others oth;
   caurses cau;
    result obj;
    calender c;
           
    int choice, rollNo;
    while (true)
    {
    cout<<"\t\t\t\t\tWELCOME TO STUDENT LOGIN SECTION";
    cout<<"\n\n";
    cout<<"\t\t\t\t\tEnter your choice..\n";
    cout << "\t\t\t|-------------------------------------------------------------------------------------------------------------|\n";
    cout << "\t\t\t|       1.Display your information     |                     ";
    cout << "\t\t\t|2.Display fees reciept                         \t\t\t|\n";
    cout << "\t\t\t|       3.your attendance              |                     ";
    cout << "\t\t\t|4.view your mark sheet                         \t\t\t|  \n";
    cout << "\t\t\t|       5.time table                   |                     ";
    cout << "\t\t\t|6.caurse                                       \t\t\t|\n";
    cout << "\t\t\t|                                  7.calender                                                                 |\n";
    cout << "\t\t\t|-------------------------------------------------------------------------------------------------------------|\n";

    cin>>choice;
    switch (choice)
    {
             case 1:
            bi.display_basic();
            break;
 
            case 2:
             fs.feesof();
             break;
            case 3:
               at.fileattend();
               break;

            case 4:
               s.display();
               break;
               
            case 5:
               oth.timetable();
                break;

            case 6:
               cau.caurse();
               break;
                
            case 7:
               c.calender1();
               break;
            default:
                    cout << "Invalid choice. Please try again.\n";
       exit(0);
    }

    }
    
    
}
};

int main()
{
    
     system("CLS");
    system("color 4");
    ///login page//
     //password a;
    // a.pass();
    for(int i=0;i<60;i++)
     {
        
        cout<<"*+";
        Sleep(15);
     }
     system("CLS");
     int choice;
    calling cg;

    while (true)
    {
        cout<<"----------------------------------------------------------------------------------------------------------------------------------------------------\n\n\n\n\n";
        cout<<"            DATE:-"<<_DATE_<<endl;
        cout<<"            TIME:-"<<_TIME_<<endl;
        
        cout<<"\t\t\t\t\t\tWELCOME TO THE STUDENT INFORMATION SYSTEM OF AMITY SCHOOL \n\n\n\n\n";
        cout <<"\t\t\t\t\t                               CREATED BY \n\n";
        cout<<"    \tVivek Dhakar  \t\t";
        cout<<"    Abhishek Sharma \t\t";
        cout<<"  Sumit Pathwar  \t\n\n";
        cout <<"\t\t\t\t\tCreated under the guidance of Dr.Nikhlesh Pathik (Associate Professor ASET CSE)\n\n\n\n";
        cout<<"                                    |--------------------------------------------------------------------|\n";
        cout<<"                                    |                             1.Faculty login                        |\n";
        cout<<"                                    |                             2.Student login                        |\n";
        cout<<"                                    |                             3.Exit                                 |\n";
        cout<<"                                    |--------------------------------------------------------------------|\n\n\n\n\n";
        cout<<"----------------------------------------------------------------------------------------------------------------------------------------------------\n\n\n\n\n";

        cin>>choice;
        switch (choice)
        {
        case 1:
            cg.faculty();
            break;
        
        case 2:
        cg.studen();
        break;

        case 3:
        exit(0);
       return 0;
        default:
            cout<<"invalid choice";
            exit(0);
        }
    }
    

}
