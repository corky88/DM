---------------------------------------------------------------------------------------------
This is an example of AR algorithm implementation in Java.

Thomas Corkum - B00467335
Justin Trainor - B00620850
---------------------------------------------------------------------------------------------

- What is this program for?

 This is a associatation rule program

 
- Overview of the program code:

There are 2 files A_R.java & Item.java

File Name					Function Names
===============================================================================================
1. A_R.java					
					public static void main(String[])
					public static void prune(HashMap<TreeSet<Item>,Integer>, HashSet<TreeSet<Item>>, int) 
					public static HashSet<TreeSet<Item>> createNewCandidates(HashSet<TreeSet<Item>>) 
					public static void count(HashMap<TreeSet<Item>, Integer>, HashSet<TreeSet<Item>>, ArrayList<TreeSet<Item>>)
					public static HashSet<TreeSet<Item>> buildPowerSet(TreeSet<Item>)
					public static void buildPowerSetHelper (HashSet<TreeSet<Item>>, ArrayList<Item>, int)
					public static TreeSet<Item> difference(TreeSet<Item>, TreeSet<Item>)
					public static void printHeader(int,int,double,double)
					public static void printRule(TreeSet<Item>, TreeSet<Item>, double, double, int) 
									
2. Item.java
					Structure class for a keyvalue pair. 




- The following is the  program structure:
				
				Run A_R:
					A_R loads data into memory, generates association rules and outputs text to src/Rules.txt

main()	----> Input filename, support, confidence
		----> Build first item set
		----> Generates rest of item sets of the frequent item sets
		----> Generates association rules from the item sets 
		----> Outputs result to src/Rules.txt 



-How to run the program:
	make 
	mkdir src
	java -cp . a3.A_R <data file> <support rate> <coonfidence rate> 
	
Demo example: 

Script started on Wed 08 Mar 2017 05:06:17 PM AST
tcorkum@bluenose:~/assign3$ java -cp . a3.A_R data1 .25 .6
tcorkum@bluenose:~/assign3$ cat src/Rules.txt 
Summary:
Total rows in the original set: 14
Total rules discovered: 12
The selected measures: Support=0.25, Confidence=0.6
-------------------------------------------------
Discovered Rules: 

Rule#1: (Support=0.29, Confidence=0.67)
{temperature=mild} ---> {Humidity=high}
Rule#2: (Support=0.29, Confidence=0.67)
{temperature=mild} ---> {PlayTennis=P}
Rule#3: (Support=0.29, Confidence=0.8)
{PlayTennis=N} ---> {Humidity=high}
Rule#4: (Support=0.29, Confidence=1.0)
{outlook=overcast} ---> {PlayTennis=P}
Rule#5: (Support=0.43, Confidence=0.86)
{Humidity=normal} ---> {PlayTennis=P}
Rule#6: (Support=0.43, Confidence=0.67)
{PlayTennis=P} ---> {Humidity=normal}
Rule#7: (Support=0.43, Confidence=0.67)
{PlayTennis=P} ---> {Windy=false}
Rule#8: (Support=0.43, Confidence=0.75)
{Windy=false} ---> {PlayTennis=P}
Rule#9: (Support=0.29, Confidence=1.0)
{temperature=cool} ---> {Humidity=normal}
Rule#10: (Support=0.29, Confidence=0.67)
{PlayTennis=P, Windy=false} ---> {Humidity=normal}
Rule#11: (Support=0.29, Confidence=1.0)
{Windy=false, Humidity=normal} ---> {PlayTennis=P}
Rule#12: (Support=0.29, Confidence=0.67)
{PlayTennis=P, Humidity=normal} ---> {Windy=false}
tcorkum@bluenose:~/assign3$ exit
exit

Script done on Wed 08 Mar 2017 05:06:33 PM AST


Task Partition:
    Work was divided evenly between Thomas and Justin. All code was collaborated on in person.
