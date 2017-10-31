# Java-Calculator-Simple
Developing Basic Calculator in Java Using Swing Components.

 By Sabihuddin XXXX XXXXXXX

Main Class: Calculator: (Calculator.java)

import javax.swing.JOptionPane;
import javax.swing.JFrame;
import javax.swing.JTextArea;

public class Calculator {// Main Class (Calculator Starts here)
public static void main(String []args){
control(); //program controller called.
}
//function/Methods goes here. (all methods below one-by-one, from addition to factorial.)
}//Main class Calculator ends here. (this bracket will appear as last bracket of the program. For     //instance, this bracket is used for explanation.

 

 test


Code for Calculator Class:


public static void control() //method starts here
{
try{   //Exception starts here
int ch;
ch=Integer.parseInt(JOptionPane.showInputDialog(null,"1-Additionn2-Subtractionn3-Multiplicationn4-Divisionn5-Create Tablen6-Factorialn7-Exit ","Calculator",JOptionPane.INFORMATION_MESSAGE));

switch(ch){  //conditional statement start here for options.
case 1: add();
break;
case 2: sub();
break;
case 3: mul();
break;

case 4: div();
break;
case 5: tables();
break;
case 6: fact();
break;
case 7:

JOptionPane.showMessageDialog(null,"Thanks for using the program","Thank You",JOptionPane.INFORMATION_MESSAGE);
System.exit(0);

break;
default: JOptionPane.showMessageDialog(null,"Invalid Choice","Incorrect Input",JOptionPane.ERROR_MESSAGE);
control(); //Main control called

}//switch ends here
} // try block ends here

 //catch starts here

catch(Exception ie){JOptionPane.showMessageDialog(null,"Invalid Operation","Invalid Activity Performed. Select Exit Option.",JOptionPane.ERROR_MESSAGE);
control(); //Main control called
} //catch ends here

} // method stops here.

 

Code for Addition: 

test

public static void add(){ // method starts here
int a,b,c;
a=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of A: ","Calculator-Addition",JOptionPane.INFORMATION_MESSAGE));
b=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of B: ","Calculator-Addition",JOptionPane.INFORMATION_MESSAGE));
c=a+b;
JOptionPane.showMessageDialog(null,"Addition of A+B is :"+c,"Addition-Output",JOptionPane.INFORMATION_MESSAGE);
control();

} //method stops here
 

Code for Subtraction:

test

public static void sub(){  // method starts here
int a,b,c;
a=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of A: ","Calculator-Subtraction",JOptionPane.INFORMATION_MESSAGE));
b=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of B: ","Calculator-Subtraction",JOptionPane.INFORMATION_MESSAGE));
c=a-b;
JOptionPane.showMessageDialog(null,"Subtraction of A-B is :"+c,"Subtraction-Output",JOptionPane.INFORMATION_MESSAGE);
control();
} // method ends here.


Code for Multiplication:

test 

 

public static void mul(){ method starts here.
int a,b,c;
a=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of A: ","Calculator-Multiplication",JOptionPane.INFORMATION_MESSAGE));
b=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of B: ","Calculator-Multiplication",JOptionPane.INFORMATION_MESSAGE));
c=a*b;
JOptionPane.showMessageDialog(null,"Multiplication of A*B is :"+c,"Multiplication-Output",JOptionPane.INFORMATION_MESSAGE);
control();
} // method ends here
 

Code for Division:

 test

public static void div(){   // method starts here
int a,b,c;
a=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of A: ","Calculator-Division",JOptionPane.INFORMATION_MESSAGE));
b=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter value of B: ","Calculator-Division",JOptionPane.INFORMATION_MESSAGE));
c=a/b;
JOptionPane.showMessageDialog(null,"Division of AB is :"+c,"Division-Output",JOptionPane.INFORMATION_MESSAGE);
control();

} //method ends here

 Code for Event-based Table (Table No, Start Value & End Value):

 test

 test

 

public static void tables(){ //method starts here
int a,b,c,d,e,f=0;
JFrame jf=new JFrame("Table Output"); //JFrame instantiated here (object created as 'jf')
JTextArea jta=new JTextArea(); //JTextArea Control instantiated here (object created as 'jta')

try{  // Exception starts here
a=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter Table No: ","Table Generation",JOptionPane.INFORMATION_MESSAGE));
b=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter Start Value: ","Table Generation",JOptionPane.INFORMATION_MESSAGE));
c=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter Stop Value: ","Table Generation",JOptionPane.INFORMATION_MESSAGE));
if(c>100){
JOptionPane.showMessageDialog(null,"Maximum value is limited to 100.","Max Value Limit",JOptionPane.ERROR_MESSAGE);
c=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter Stop Value: ","Table Generation",JOptionPane.INFORMATION_MESSAGE));
}
for(e=b; e<=c; e++){ //for loop starts here
f=a*e;
///// showing output ///
jf.add(jta); //JFrame used as output window and JTextArea Added onto it.
jf.setSize(400,400);
jta.append(a+" * "+ e +" = "+f+"n");
jf.setVisible(true);//displaying JFrame
}// for loop ends here
control(); // main program control calls
}//try block ends here.
catch(Exception ex){System.out.println("Error traced."+ex);

} // catch block ends here.
} // method ends here.

  Code For Recursion (Factorial):

 test

static void fact(){ / method starts here
int n,f=1,g;

// integer input is taken in n, using JOptionPane.
n=Integer.parseInt(JOptionPane.showInputDialog(null,"Enter Value to Generate Factorial.","Generate Factorial",JOptionPane.INFORMATION_MESSAGE));
if(n<0){
JOptionPane.showMessageDialog(null,"Invalid Number! Input Positive Numbers","Value Error",JOptionPane.ERROR_MESSAGE);
fact();
}
else{
for(g=1; g<=n; g++)
{
f=f*g;
}
JOptionPane.showMessageDialog(null,"The Factorial of the Input Value "+n+" is : "+ f);
control();
} // factorial method ends here

}// Main Class (Calculator Ends here)
