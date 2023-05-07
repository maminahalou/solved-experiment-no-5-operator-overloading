Download Link: https://assignmentchef.com/product/solved-experiment-no-5-operator-overloading
<br>
<strong><u>Operator Overloading</u></strong>

<strong> </strong>Objectives

In this lab students will learn to overload,

<ul>

 <li>Arithmetic operators</li>

 <li>Relational operators</li>

 <li>Logical operators ➢ Unary operators</li>

</ul>




<strong>Equipment required</strong>

<ul>

 <li>Visual Studio/ Dev C++/Eclipse installed in Windows/PC</li>

</ul>

<h2>Operator Overloading</h2>

In C++ the overloading principle applies not only to functions, but to operators too. That is, of operators can be extended to work not just with built-in types but also classes. A programmer can provide his or her own operator to a class by overloading the built-in operator to perform some specific computation when the operator is used on objects of that class. The following set of operators is commonly overloaded for user-defined classes:

<ul>

 <li>= (assignment operator)</li>

 <li>+, -, *, , (binary arithmetic operators)</li>

 <li>+=, -=, *=, (compound assignment operators)</li>

 <li>==, !=, &gt;, &lt;, &gt;=, &lt;=, (comparison operators)</li>

</ul>

Operator overloading is a clear representation of operations performed, and is used because it allows the developer to program using notation closer to the target domain and allows userdefined types a similar level of syntactic support as types built into the language, for example, consider variables a, b, c of some user-defined type, such as matrices:

<strong>a + b * c </strong>

In a language that supports operator overloading, and with the usual assumption that the ‘*’ operator has higher precedence than ‘+’ operator, this is a concise way of writing:

<strong>add (a, multiply (b,c)) </strong>

You cannot create new operators like *&amp; and try to overload them; only existing operators can be overloaded. The precedence of an operator cannot be changed by overloading. The associativity (i.e., left-to-right, or right-to-left) of an operator cannot be changed. The arity (i.e., no. of operands) of an operator cannot be changed. The meaning of how an operator works on built-in types cannot be changed. Operator overloading works only on objects of user defined types or with a mixture of user-defined and built-in types.




<strong> </strong>

<strong>BEMTS-F20- A                                                                                                   Air University, Islamabad </strong>




<h2>Example</h2>

<table width="601">

 <tbody>

  <tr>

   <td width="302"><strong>Operator Overloading example </strong></td>

   <td width="299"> </td>

  </tr>

  <tr>

   <td width="302">class complex {int real, imag;  public: complex(): real(0),  imag(0) {}complex(int re, intim): real(re), imag(im)  {    } complex operator + (complex c) { int re2=real + c.real;                                  <strong>//note: </strong><strong>we aim not to change the  operands</strong> int im2=imag+c.imag;return complex(re2, im2);}};</td>

   <td width="299">void main() {complex c1, c2(1,2), c3, c4;    c1.setdata();c3=c1+c2;   <strong>//same as c1.operator + (c2)</strong>   c4 = c1+c2+ c3;   <strong>//note cascading</strong>   c4. showdata();} </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<h2>LAB TASKS</h2>

<strong>Q1. </strong>Create a class <strong>RationalNumber</strong> that stores a fraction in its original form (i.e., without finding the equivalent floating pointing result). This class models a fraction by using two data members: an integer for <strong>numerator</strong> and an integer for <strong>denominator</strong>. For this class, provide the following functions:

<ul>

 <li>A no-argument constructor that initializes the numerator and denominator of a fraction to some fixed values.</li>

 <li>A two-argument constructor that initializes the numerator and denominator to the values sent from calling function. This constructor should prevent a 0 denominator in a fraction, reduce or simplify fractions that are not in reduced form, and avoid negative denominators.</li>

 <li>A display function to display a fraction in the format a/b.</li>

 <li>An overloaded pre and post increment operator to increment the data members.</li>

 <li>An overloaded operator – for subtraction of two rational numbers. Two fractions a/b and c/d are subtracted from each other as:</li>

</ul>




<ul>

 <li>An overloaded operator / for division of two rational numbers. If fraction a/b is divided by the fraction c/d, the result is</li>

</ul>




<ul>

 <li>An overloaded relational operator &gt;= should return a variable of type bool to indicate whether 1st fraction is greater than or equal to 2nd or not</li>

 <li>Overloaded equality operator == should return a variable of type bool to indicate whether 1st fraction is equal to the 2nd fraction or not.</li>

</ul>