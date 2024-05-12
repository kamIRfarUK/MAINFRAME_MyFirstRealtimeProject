# MAINFRAME_MyFirstRealtimeProject
Medical Insurance Processing System

 
**********************************************************************************************************************************************************************
4.2.2	Process Flow Details
The proposed application process flow is as below
1)	Split “Insurance Policy ” into 6 different files namely Medical Insurance file, Life Insurance file, Child Insurance file, Property Insurance file, Travel Insurance file and Motor Insurance file based on ‘Policy  Type’. (Hint: SORT Utility can be used to achieve this) This file will be internally referred by respective policy type processing Divisions.

2)	Create the Insurance Policy Table and load the details of Medical Insurance Policy file after validating the basic validations (check for format and mandatory values, numeric check) and write the error records into Error file with rejected reason.

Below details should be loaded to the table

i.	Policy Id
ii.	Policy Code
iii.	Policy Name
iv.	Type of Policy
v.	Term
vi.	Policy Amount

3)	Create the Agent Detail Table and load the details from Agent Detail file after validating the basic validations (check for format and mandatory values, numeric check) and write the error records into Error file with rejected reason.

Below details should be loaded to the table

i.	Agent Code
ii.	Agent Name
iii.	Registration Number
iv.	Street Name
v.	City
vi.	State
vii.	PIN Code
viii.	Phone Number
ix.	Registration Number
x.	Commission 

4)	Load the newly added  validated Policy detail in Master Policy VSAM KSDS file

5)	Split “Insurance Policy” file into different files based on ‘Term ‘and sort the file in the order of Policy Id and Policy code. These files will be internally referred by the processing Divisions.

6)	Extract the required details and generate a separate report file for the above applicants in the standard report format. Use page break logic. Maximum no: of lines to be displayed in a page are 10. 


Note:  
1.	Master Policy VSAM file contains the Details of all Policies
2.	Maintain Back up of all the input and output files in GDG File where GDG limit is 10 versions. No need to back up any intermediately output files.
3.	Refer the below attachment for the details about Insurance Policy Database and Agent Detail Database.


LAYOUT REPORT:
*****************************************************************************************************************************************************************
                                                           MEDICAL INSURANCE DETAIL REPORT

DATE : CCYYMMDD                                                                                                                     Page : 1  
Time : HH:MM:SS                                                                                                                         Report ID:1001                                                                                                                                                                

POLICY ID                POLICY CODE                 POLICY TYPE          TERM       
-------------------              -- ------------              ------------           --------------




           ---------------------       End of Page ---------------------------------
                                                                                                                                                 Page:2
                                                                                                                                                Report ID:1001  

POLICY ID                POLICY CODE                 POLICY TYPE          TERM       
-------------------              -- ------------              ------------           --------------





           ---------------------       End of Page ---------------------------------




                                                                                                                                                 Page:3
                                                                                                                                                Report ID:1001  

POLICY ID                POLICY CODE                 POLICY TYPE          TERM       
-------------------              -- ------------              ------------           --------------




           ---------------------       End of Page ---------------------------------
                                                           
                         ****** ******* END OF REPORT **********************
**********************************************************************************************************************************************************************

File	Insurance Policy Database				
					
Fields in the Insurance Policy Database					
S.No	Field Name	Type	Length	Format/Possible Values	Sample Data
1	Policy Id	CHAR	5	Trailing Spaces	M1011
2	Policy Code	CHAR	10	Trailing Spaces	MED100001Q
3	Policy Name	CHAR	25	Trailing Spaces	Jeevan Rakzha Policy
4	Type of Policy	CHAR	10	Trailing Spaces	Medical/Life/Child/Property/Travel/Motor
5	Term	CHAR	7	MONTHLY/QLY/YEARLY	QLY
6	Policy Amount	CHAR	13	Leading Zeroes	0,001,000,000



File	Agent Details Database				
					
Fields in the Agent Details Database					
S.No	Field Name	Type	Length	Format/Possible Values	Sample Data
1	Agent Code	CHAR	5	Trailing Spaces	0043278A
2	Agent Name	CHAR	10	Trailing Spaces	R. Rajesh
3	Street	CHAR	20	Trailing Space	15th Street
4	City	CHAR	20	Trailing Space	Chennai
5	State	CHAR	20	Trailing Space	Tamil Nadu
6	PIN	NUM	6	Leading Zeroes	600006
7	Phone No	CHAR	12	Leading Zeroes	99-4055-1867
8	Registration Number	CHAR	15	Trailing Spaces	TNCHN201310005
9	Commission %	NUM	2	Leading Zeroes	10




VSAM File	Master Policy File			
				
Fields in the File				
S.No	Field Name	Key	Type	Length
1	Policy Id	Key Field	CHAR	5
2	Policy Code		CHAR	10
3	Type of Policy		CHAR	10


********************************************************************************************************************************************************************

 






