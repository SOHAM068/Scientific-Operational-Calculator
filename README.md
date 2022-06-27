# Scientific-Operational-Calculator
This code is of a scientific calculator that can be used to calculate various arithmetic operations such as addition, subtraction, multiplication, division, factorial, modulus, square, square root, etc.

#include&lt;stdio.h&gt;
#include&lt;stdlib.h&gt;
#include&lt;math.h&gt;

#define note &quot;Enter the valid operation&quot;
void addition();
void subtraction();
void multiplication();
void squareroot();
void division();
int factorial(int);
void modulus();
void power();
void square();
void cube();

int main(){
    printf(&quot;\t\tWelcome to the scientific calculator!!\n\n&quot;);

    int choice;
    printf(&quot;\n******* Press 0 to quit the program ********\n&quot;);
    printf(&quot;Enter 1 for Addition \n&quot;);
    printf(&quot;Enter 2 for Subtraction \n&quot;);
    printf(&quot;Enter 3 for Multiplication \n&quot;);
    printf(&quot;Enter 4 for Division \n&quot;);
    printf(&quot;Enter 5 for Modulus\n&quot;);
    printf(&quot;Enter 6 for Power \n&quot;);
    printf(&quot;Enter 7 for Factorial \n&quot;);
    printf(&quot;Enter 8  for square \n&quot;);
    printf(&quot;Enter 9  for cube \n&quot;);
    printf(&quot;Enter 10 for squareroot\n\n&quot;);
   
    while(1){    
    printf(&quot;\n\nEnter the operation you want to do: &quot;);
   
    scanf(&quot;%d&quot;,&amp;choice);
           
    switch(choice)
    {
                case 1:
                    addition();
                    break;
                case 2:
                    subtraction();

                    break;
                case 3:
                    multiplication();
                    break;
                case 4:
                    division();
                    break;
                case 5:
                    modulus();
                    break;
                case 6:
                    power();
                    break;
                case 7:
              {  int n;
                 printf(&quot;Enter the number you want the factorial of: &quot;);
                  scanf(&quot;%d&quot;,&amp;n);
                      printf(&quot;\nFactorial of %d is %d&quot;,n,factorial(n));}
                    break;
                case 8:
                    square();
                    break;
                case 9:
                    cube();
                    break;

                case 10:
                    squareroot();
                    break;
                case 0:
                    exit(0);
                default:
                    printf(&quot;\n********** %s ***********\n&quot;,note);
        }
   
    }
    return 0;
}

void addition(){
    printf(&quot;Enter the numbers you want to add: &quot;);
    int a,b;
    scanf(&quot;%d%d&quot;,&amp;a,&amp;b);
    printf(&quot;The sum of a and b is %d\n&quot;,a+b);
}
void multiplication(){
    printf(&quot;Enter the numbers you want to multiply: &quot;);
    int a,b;
    scanf(&quot;%d%d&quot;,&amp;a,&amp;b);
    printf(&quot;The multiplication of a and b is %d\n&quot;,a*b);
}

void division(){
    printf(&quot;Enter the numbers you want to divide: &quot;);
    int a,b;
    scanf(&quot;%d%d&quot;,&amp;a,&amp;b);
    printf(&quot;The division of a and b is %f\n&quot;,(float)a/(float)b);
}
int  factorial(int n){
  if((n==1)||(n==0))
  return 1;
  else
  return(n*factorial(n-1));
}
void modulus(){
    printf(&quot;Enter the numbers you want to find modulus of: &quot;);
    int a,b;
    scanf(&quot;%d%d&quot;,&amp;a,&amp;b);
    printf(&quot;The modulus of a and b is %d\n&quot;,a%b);
}
void subtraction(){
    printf(&quot;Enter the numbers you want to subtract: &quot;);
    int a,b;
    scanf(&quot;%d%d&quot;,&amp;a,&amp;b);
    printf(&quot;The subtraction of a and b is %d\n&quot;,a-b);
}
void power(){

    double b;
    double p;
    printf(&quot;Enter the base and the power: &quot;);
    scanf(&quot;%lf%lf&quot;,&amp;b,&amp;p);
    double e=pow(b,p);
    printf(&quot;The power is %lf&quot;,e);
}
void square(){
    double b;
    printf(&quot;Enter the number you want the square of: &quot;);
    scanf(&quot;%lf&quot;,&amp;b);
    double p=pow(b,2);
    printf(&quot;The square of %lf is %lf&quot;,b,p);
}
void squareroot(){
    double b;
    printf(&quot;Enter the number you want the square root of : &quot;);
    scanf(&quot;%lf&quot;,&amp;b);
    double s = sqrt(b);
    printf(&quot;The square root of %lf is %lf&quot;,b,s);
}
void cube(){
    double b;
    printf(&quot;Enter the number you want the cube of: &quot;);
    scanf(&quot;%lf&quot;,&amp;b);

    double p=pow(b,3);
    printf(&quot;The cube of %lf is %lf&quot;,b,p);
}
