# COP-3003-Assignments
This is a collection of Assignments to showcase progression within C++.
//#################################################[Stack Operations]#################################################
/*
* [Prompt] - Use Stack operations to:
*  (a)	Display the elements in stack
*  (b)	get the size of stack
*  (c)	Print top of the stack
*  (d)	Pop some stack values and display the stack.
*/
#include <iostream>
#include <stack>
using namespace std;

//stores stack to be able to edit it
class stackoperations{
public:
    stack<string> stack1;
    string stack_elem;
};
//derived class for UI funtions
//not helpful, just throwing it in
class ui_elem: public stackoperations{
public:
    //Adds enough blank lines to make it seem as if the console was cleared.
    //Every other built-in function I know of or could find was OS-dependant.
    void clear_console(){
        cout << string(10, '\n') << endl;
    }
    //visually separates the output from the following menu prompt.
    void in_out_sep(){
        cout << string(100, '#') << "\n" << endl;
    }
    //Wraps user's menu selection with brackets.
    void input_box(){
        cout << "[ ]\b\b";
    }
};
//to access objects within class
stackoperations s{};
ui_elem ui{};
//(a)Display the elements in stack
void displ_menu(){
    ui.in_out_sep();
    cout << "Enter\n[1]Add Element\n[2]Remove Previous Element\n[3]Display Quantity of Elements\n[4]Call previously added Element\n"
            "[5]Display All Elements\n[0]Exit" << endl;
}
//(1/2(d))Pop some stack values.
void add_elem(){
    cin >> s.stack_elem;
    s.stack1.push(s.stack_elem);
    ui.clear_console();
}
void rem_elem(){
    s.stack1.pop();
    ui.clear_console();
}
//(b)get the size of stack
void displ_stack_size(){
    //clearing before so that user can see ouput
    //could use a continue-verification or timer
    ui.clear_console();
    cout << "Quantity: " << s.stack1.size() << "\n" << endl;
}
//(c)Print top of the stack
void displ_last_elem(){
    ui.clear_console();
    cout << s.stack1.top() << "\n" << endl;
}
//(a)&(1/2(d))Display the elements in stack
void displ_all_elem(){
    ui.clear_console();
    //creating a copy of stack to use in function so that the original stack does not get modified.
    stack<string> copy_stack1 = s.stack1;
    while(!copy_stack1.empty()){
        cout << copy_stack1.top() << "\n";
        copy_stack1.pop();
    }
}

int main(){
    int usr_choice;
    do{
        //Outputs menu options
        displ_menu();
        ui.input_box();
        cin >> usr_choice;
        switch(usr_choice){
            case 0:
                break;
            case 1:
                add_elem();
                break;
            case 2:
                rem_elem();
                break;
            case 3:
                displ_stack_size();
                break;
            case 4:
                displ_last_elem();
                break;
            case 5:
                displ_all_elem();
                break;
        }
    }while(usr_choice != 0);
    return 0;
}
//#####################################################[END]#####################################################

//#################################################[Inheritence]#################################################
  //Show two type of Inheritance program of your own choice(1.1, 1.2).
[Question 1.1]

# #include <iostream>
#include <stack>
using namespace std;

//stores stack to be able to edit it
class stackoperations {
public:
    stack<string> stack1;
    string stack_elem;
};
//derived class for UI funtions
//not helpful, just throwing it in
class ui_elem : public stackoperations {
public:
    //Adds enough blank lines to make it seem as if the console was cleared.
    //Every other built-in function I know of or could find was OS-dependant.
    void clear_console() {
        cout << string(10,[In Class Assignment Week 12-1.docx](https://github.com/alexanderfatjo/COP-3003-Assignments/files/10126186/In.Class.Assignment.Week.12-1.docx)
 '\n') << endl;
    }
    //visually separates the output from the following menu prompt.
    void in_out_sep() {
        cout << string(100, '#') << "\n" << endl;
    }
    //Wraps user's menu selection with brackets.
    void input_box() {
        cout << "[ ]\b\b";
    }
};
//to access objects within class
stackoperations s{};

ui_elem ui{};
//(a)Display the elements in stack
void displ_menu() {
    ui.in_out_sep();
    cout << "Enter\n[1]Add Element\n[2]Remove Previous Element\n[3]Display Quantity of Elements\n"
            "[4]Call previously added Element\n[5]Display All Elements\n[0]Exit" << endl;

}
//(1/2(d))Pop some stack values.
void add_elem() {
    cin >> s.stack_elem;
    s.stack1.push(s.stack_elem);
    ui.clear_console();
}
void rem_elem() {
    s.stack1.pop();
    ui.clear_console();
}
//(b)get the size of stack
void displ_stack_size() {
    //clearing before so that user can see ouput
    //could use a continue-verification or timer
    ui.clear_console();
    cout << "Quantity: " << s.stack1.size() << "\n" << endl;
}
//(c)Print top of the stack
void displ_last_elem() {
    ui.clear_console();
    cout << s.stack1.top() << "\n" << endl;
}
//(a)&(1/2(d))Display the elements in stack
void displ_all_elem() {
    ui.clear_console();
    //creating a copy of stack to use in function so that the original stack does not get modified.
    stack<string> copy_stack1 = s.stack1;
    while (!copy_stack1.empty()) {
        cout << copy_stack1.top() << "\n";
        copy_stack1.pop();
    }
}
int main() {
    int usr_choice;
    do {
        //Outputs menu options
        displ_menu();
        ui.input_box();
        cin >> usr_choice;
        switch (usr_choice) {
            case 0:
                break;
            case 1:
                add_elem();
                break;
            case 2:
                rem_elem();
                break;
            case 3:
                displ_stack_size();
                break;
            case 4:
                displ_last_elem();
                break;
            case 5:
                displ_all_elem();
                break;
        }
    } while (usr_choice != 0);
    return 0;
}

//#####################################################[END]#####################################################
//[Question 1.2]

#include <iostream>
using namespace std;

class Shapes{
public:
    int area;
};
Shapes s{};
class triangle : public Shapes{
public:
    int area(int l, int w){
        int area_triangle = (l * w) / 2;
        return s.area = area_triangle;
    }
};
class rectangle : public Shapes{
public:
    int area(int l, int w){
        int area_rectangle = (l * w);
        return s.area = area_rectangle;
    }
};

int main() {
    int l, w;
    triangle tri{};
    rectangle rect{};
    cout << "Enter Length and Width: " << endl;
    cin >> l >> w;
    tri.area(l, w);
    cout << "Area if Triangle: " << s.area << endl;
    rect.area(l, w);
    cout << "Area if Rectangle: " << s.area << endl;
    return 0;
}
//#######################################################[END]#######################################################

//2. Using multilevel inheritance write a program to manage patient bills in a hospital.
#include <iostream>
#include <string>
using namespace std;

class patient {
    //members within protected are accessible to derived classes, not to outside of class
protected:
    int patient_id;
    string name;
public:
    int cover_charge = 250;
    patient(int pat_id, string pat_name) {
        patient_id = pat_id;
        name = pat_name;
    }
    void pat_inf() {
        cout << "Patient ID: " << patient_id << endl;
        cout << "Patient Name: " << name << endl;
    }
};
class newpatient : public patient {
protected:
    int days;
    double daily_rate;
public:
    //constructor for newpatient class
    newpatient(int patient_id, string name, int d, double dr) : patient(patient_id, name) {
        days = d;
        daily_rate = dr;
    }
};
//derived class from child class newpatient. Parent class is patient.
class payment: public newpatient {
public:
    double amount_paid;
    double subtotal = days * daily_rate + cover_charge;
    //constructor
    payment(int patient_id, string name, int d, double dr) : newpatient(patient_id, name, d, dr) {}
    //function to calculate call to pay bill and update amount due
    double pay(int amt){
        subtotal = subtotal - amt;
        return subtotal;
    }
    void bill_inf(){
        //patient name and id are protected
        patient::pat_inf();
        cout << "Number of days in hospital: " << days << endl;
        cout << "Daily rate: " << daily_rate << endl;
        cout << "Total bill: " << subtotal << endl;
    }
    double bill_pay() {
        cout << "Amount due: " << subtotal << "\nEnter Amount Paid: " << endl;
        cin >> amount_paid;
        pay(amount_paid);
        cout << "Amount due: " << subtotal << endl;
    }
};
int main() {
    newpatient p1(1001, "John Smith", 5, 250.00);
    p1.pat_inf();
    payment p2(1001, "John Smith", 5, 250.00);
    p2.bill_inf();
    p2.bill_pay();
    return 0;
}

//#######################################################[END]#######################################################
//3. Use friend function to find the maximum of two numbers from different classes.
#include<iostream>
using namespace std;
class y_nums;
class x_nums;

class x_nums {
private:
    int x;
public:
    x_nums(int x) {
        this->x = x;
    }
    //can access private members of y_nums & x_nums
    friend void compare(x_nums,y_nums);
};
class y_nums {
private:
    int y;
public:
    y_nums(int y) {
        this->y=y;
    }
    friend void compare(x_nums,y_nums);
};
void compare(x_nums a,y_nums b){
    if(a.x > b.y) {
        cout<< "Maximum: x = " << a.x <<endl;
    }
    else if (a.x < b.y) {
        cout<< "Maximum: y = " << b.y <<endl;
    }
    else {
        cout<< "Both are equal." << endl;
    }
}

int main() {
    x_nums x(10);
    y_nums y(9);
    compare(x,y);
    return 0;
}

//#######################################################[END]#######################################################
#include <iostream>
using namespace std;
class Shapes{
public:
    int area;
};
Shapes s{};
class triangle : public Shapes{
};
//derived class 'right_triangle' from base class 'triangle' which is derived from base class 'Shapes'
class right_triangle : public triangle{
public:
    int area(int l, int w){
        int area_right_triangle = (l * w) / 2;
        return s.area = area_right_triangle;
    }
};
class rectangle : public Shapes{
public:
    int area(int l, int w){
        int area_rectangle = (l * w);
        return s.area = area_rectangle;
    }
};
int main() {
    int l, w;
    triangle tri{};
    rectangle rect{};
    right_triangle rt{};
    cout << "Enter Length and Width: " << endl;
    cin >> l >> w;
    rt.area(l, w);
    cout << "Area if Right Triangle: " << s.area << endl;
    rect.area(l, w);
    cout << "Area if Rectangle: " << s.area << endl;
    return 0;
}

//#######################################################[END]#######################################################


//#####################################################[Assignment 3]#################################################
//1. Using pass value, reference and prototype to return data

#include <iostream>
#include <string>
using namespace std;

//proto to output the switch case options to choose from
void intro() {
    string intro = "-----Choose Return Method:-----\n[1] value\n[2] reference\n[3] prototype";
    cout << intro << endl;
}
//return by prototype
void sqr_proto(double x) {
    double sqrX = (x * x);
    cout << sqrX << endl;
}
//return by reference
int sqr_ref(double &x) {
    return x * x;
}
int main() {
    int method;
    double x{0};
    bool exit = false;
    string user_exit;
    do {
        intro();//calls the prototype 'intro' to list return-method options
        cin >> method;
        cout << "Enter a number: " << endl;
        cin >> x;
        //cleaner way of combining the three ways of squaring a number into one working program
        switch (method) {
            case 1: //return by value
                cout << (x * x) << endl;
                break;
            case 2: //return by reference
                cout << sqr_ref(x) << endl;
                break;
            case 3: //for return by prototype
                sqr_proto(x);
                break;
        }
        cout << "Continue?(y/n): ";
        cin >> user_exit;
        if (user_exit != "y") { exit = true; }
    } while (exit != true);
    return 0;
}

//#######################################################[END]#######################################################
//
#include <iostream>
#include <climits>
using namespace std;
int main() {
  //[SOURCE]--> https://www.geeksforgeeks.org/int_max-int_min-cc-applications/
  //using INT_MAX & INT_MIN from <climits>
  //These two will block/only allow for the greatest(for INT_MAX) and least(for INT_MIN) to be stored in memory
  float num_min = INT_MAX, num_max = INT_MIN;
  float arr1[] = { -333.12, 324523, 4233.3376, 9, 2.22556, -356.843 };
  //using 'auto' will accept any types of numbers from 'arr1' for 'i' that are previously declared
  // By using a loop, we are comparing each value stored in 'i' from 'arr1'...
  //...to what is currently held in 'INT_MIN' until the end of the array has been reached.
  for (auto i: arr1) {
    if (i < num_min) {num_min = i;}
  }
  for (auto i : arr1){
    if (i > num_max) {num_max = i;}
  }
  cout << "Minimum: " << num_min << endl;
  cout << "Maximum: " << num_max << endl;
  return 0;
}

//#######################################################[END]#######################################################
//array operations

#include <iostream>
#include <algorithm>
using namespace std;
//[SOURCE] --> https://www.tutorialspoint.com/cplusplus-program-to-implement-sorted-array
int main()
{
    float arr[] = { 1.76, 7.33, 6.11, 9.76, 5.99, 12.22};
    float arr_median;
    int numofElem = sizeof(arr) / sizeof(arr[0]);
    sort(arr, arr + numofElem);

    cout << "Array: {";
    //for sorting 'arr' using recursion
    for (int i = 0; i < numofElem; ++i){
        cout << arr[i] << ", ";
    }

    //for median
    if(numofElem % 2 != 0){
        //'\b\b' remove the last comma from the ouput of the sorted 'arr'
        cout << "\b\b}\nArray is odd"<< endl;
        //outputs the middle number of 'arr'
        arr_median = arr[numofElem/2];
        cout << "Median: [" << arr_median << "]" << endl;
    }
    else{
        cout << "\b\b}\nArray is even"<< endl;
        //outputs the product of the two middle numbers of 'arr' divided by 2(avg or mean)
        arr_median = (arr[numofElem/2] + arr[(numofElem/2) - 1])/(2);
        cout << "Median: [" << arr_median << "]" << endl;
    }
    return 0;
}
//#######################################################[END]#######################################################
//Sources -> [1]-https://www.softwaretestinghelp.com/bubble-sort/   [2]-https://www.programiz.com/dsa/bubble-sort
#include <iostream>
using namespace std;
//[Source](for 'swap' info and implementation) --> https://www.programiz.com/dsa/bubble-sort
void bubbleSort(float arr[], int num_of_elem);
void bubbleSort(float *arr, int num_of_elem) {
    int i, j;
    //using the built-in function 'swap' to compare two values, if condition is met, the values are then swapped positions.
    //this will repeat sequentially(starting from comparing first and second value onwards) until the end of 'arr' has been reached.
    //once the end of 'arr' has been reached, the loop will repeat and continue this until there are no more valid swap-arguments.
    for (i = 0; i < num_of_elem; i++) {
        for (j = 0; j < num_of_elem - i - 1; j++) {
            if (arr[j] < arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
            }
        }
    }
}
//mostly reused code
int main() {
    float arr[] = {1.76, 7.33, 6.11, 9.76, 5.99, 34.5, 6, 9, 0};
    int num_of_elem = sizeof(arr) / sizeof(int);

    bubbleSort(arr, num_of_elem);

    cout << "Descending Array {";
    // Print the Sorted Array
    for (int i = 0; i < num_of_elem; i++) {
        cout << arr[i] << ", ";
    }
    //for better output format
    cout << "\b\b}" << endl;
    return (0);
}
//#######################################################[END]#######################################################
/*
* Creating arrays and pointers:
* [Sources] -> [1]-https://www.programiz.com/cpp-programming/pointers-arrays  [2]-https://www.softwaretestinghelp.com/new-delete-operators-in-cpp/
*              [3]-https://stackoverflow.com/questions/35532427/how-to-dynamically-allocate-arrays-in-c
*/
#include <iostream>
#include <algorithm>
#include <new>
using namespace std;

int main() {
    //creating array & pointers
    int num_of_elem;
    int *ptr;
    ptr = new int();

    cout << "Enter number of array elements[1,100]: ";
    cin >> num_of_elem;
    *ptr = num_of_elem;
    if (num_of_elem <= 100 && num_of_elem >= 1) {
        float *arr = nullptr;//clears any value/data from 'arr' by pointing to a 'null'/empty value. Is not used here specifically, though, would be useful depending on the implementation
        arr = new float[num_of_elem]; //creates a placeholder for array 'arr' with size = 'num_of_elem'
        for (int input_elem_cnt = 1, n = 0; n < num_of_elem; n++, input_elem_cnt++ ) {
            cout << "Element[" << input_elem_cnt << "] =  ";//to keep a live count for the user to know how many elements have been inputted
            cin >> *(arr + n); //stores number from input to memory
        }
        sort(arr, arr + num_of_elem);
        cout << "Your Array: {";
        for (int i = 0; i < num_of_elem; i++) {
            cout << *(arr + i) << ", "; //outputs the numbers which are pointed to by their values
        }
        cout << "\b\b}" << endl;
        delete ptr, delete[] arr;
    }
    return 0;
}
//#######################################################[END]#######################################################
/*
* 1.Write an object-oriented C++ program to create a class for room and three objects to calculate the area and volume of three rooms. Use public access specifier and * methods for calculations.
*/

#include <iostream>
using namespace std;
class room{
public:
    float length, width, height;
    void set_var(float LENGTH, float WIDTH, float HEIGHT){
        length = LENGTH;
        width = WIDTH;
        height = HEIGHT;
    }
    //Object for calculating Volume
    //not passing parameter
    float vol_noPass(){
        return length * width * height;
    }
    //Object for calculating Area
    float area_noPass(){
        return length * width;
    }
};

int main() {
    float l, w, h, volume, area;
    room c{};

    cout << "Enter Length, Width, Height Values: " << endl;
    //set variables
    cin >> l >> w >> h;
    c.set_var(l, w,h);

    volume = c.vol_noPass();
    area = c.area_noPass();
    cout << "No-Passing Parameter Volume: " << volume << " units" << "\nNo-Passing Parameter Area: " << area << " units"<< endl;
    return 0;
}
//#######################################################[END]#######################################################

// 2. Write a program to find the volume of a rectangle using constructor (with and without passing parameters).

#include <iostream>
using namespace std;

class room{
private:
    float length, width, height;
public:
    /*void set_var(float LENGTH, float WIDTH, float HEIGHT){
        length = LENGTH;
        width = WIDTH;
        height = HEIGHT;
    }*/
    //not passing parameter
    float vol_noPass(){
        cout << "Enter Length, Width, Height Values: " << endl;
        cin >> length >> width >> height;
        return length * width * height;
    }
    //passing parameter
    void vol_pass(float length,float width,float height){
        cout << "Passing Parameter Volume: " << length * width * height << " units" << endl;
    }
};

int main() {
    float l{5}, w{10}, h{3}, volume;
    room c{};

    /*//set length, width, height variables from main
    c.set_var(l, w,h);*/

    //find volume with passing a parameter
    c.vol_pass(5, 10, 3);
    //find volume without passing a parameter
    volume = c.vol_noPass();
    cout << "No-Passing Parameter Volume: " << volume << " units" << endl;
    return 0;
}
//#######################################################[END]#######################################################
//3. Write a C++ Program to show counter using Constructor.

#include <iostream>
using namespace std;
class counter{
public:
    int count{0}, count_incr{1};
    int get_counterIncr(){
        int incr;
        cout << "Enter counter increment: [ ]\b\b";
        cin >> incr;
        count_incr = incr;
    }
    void counter_up(){
        count += count_incr;
    }
    void counter_down(){
        count -= count_incr;
    }
    int disp_counter(){
        cout << "Count [" << count << "]" << endl;
    }
};

int main() {
    int usr_choice;
    counter c{};
    c.get_counterIncr();
    cout << "\nEnter Choice\n[1]Count Up\n[2]Count Down\n" << endl;
    cin >> usr_choice;

    if(usr_choice == 1){
       c.counter_up();
    }
    else if(usr_choice == 2){
       c.counter_down();
    }
    else{
       cout << "Error: Invalid Input" << endl;
    }
    c.disp_counter();
    return 0;
}
//#######################################################[END]#######################################################



//#####################################################[Assignment 2]################################################


//#######################################################[END]#######################################################


//#####################################################[Assignment 1]################################################


//#######################################################[END]#######################################################

//#######################################################[END]#######################################################

//#######################################################[END]#######################################################

/* 1.Write a C++ program to handle multiple errors and exceptions with different throw ids and multiple catches like the previous program.
=========================SourceCode================================ */
#include <iostream>
using namespace std;
int main() {
    //move decimal of inputted number to the right(when positive) left(when negative) *(divides by 10)*
    try {
        float x, y{10};
        cout << "Enter a number: ";
        cin >> x;
        if (x != 0) {
            float prod = x / y;
            cout << prod << endl;
        } else {       //'101' is the 'throw_id'
            throw(101);//if 'x = 0' then throw '101'.
        }
    }
    //When x != 0, then no error is thrown/caught
    catch (int div_err) { cout << "Error: X cannot be 0."
                               << "\n\t\tException/Throw ID: " << 101 << endl; }
    try {
        string usr_inp{""};
        cout << "Input 'y' or 'n':" << endl;
        cin >> usr_inp;
        if ("y" == usr_inp) {
            string output = "Valid";
            cout << "Input: " << output << endl;
        } else {
            //throw ID->'201' when else input is not 'y';
            throw 201;
        }
    }
    catch (int inp_err) {
        cout << "Exception occurred. \n\t\tException/Throw ID: " << 201 << '\n';
    }
    return 0;
}
/*=========================Output====================================
Enter a number:0
 Error: X cannot be 0.
                Exception/Throw ID: 101
Input 'y' or 'n':
n
Exception occurred.
                Exception/Throw ID: 201

Process finished with exit code 0
===================================================================*/
//#####################################################[END]#####################################################

2. Write a C++ program to build a simple calculator using templates.
=========================SourceCode================================
#include <iostream>
using namespace std;
//Can use any 'keyword' as long as it remains consistent.
template<typename C>
class Calculator {
public:
    C Add(C x0, C x1);
    C Substract(C x0, C x1);
    C Multiply(C x0, C x1);
    C Divide(C x0, C x1);
};
template<typename c>
c Calculator<c>::Add(c x0, c x1) {return (x0 + x1);}
template<typename C>
C Calculator<C>::Substract(C x0, C x1) { return (x0 - x1); }
template<typename C>
C Calculator<C>::Multiply(C x0, C x1) { return (x0 * x1); }
template<typename C>
C Calculator<C>::Divide(C x0, C x1) { return (x0 / x1); }

int main() {
    float prod;            //result of calculations with float type variables
    Calculator<float> calc;//create an object of Calculator class

    prod = calc.Add(8, 3);//call Add function
    cout << "Product = " << prod << endl;

    prod = calc.Substract(2, 97);
    cout << "Product = " << prod << endl;

    prod = calc.Multiply(4, 44);
    cout << "Product = " << prod << endl;

    prod = calc.Divide(18, 3);
    cout << "Product = " << prod << endl;

    //Adding char type variables
    prod = calc.Add('a', 'f');
    cout << "Product = " << prod << endl;

    //Creating new object of Calculator class for specific data type's
    //(not needed but can help in organization/readability).
    Calculator<char> calc_alpha;
    prod = calc_alpha.Add('a', 'f');
    cout << "Product = " << prod << endl;

    Calculator<string> calc_str();
    prod = calc.Divide('Alex', 'Fatjo');
    float str1 = 'Alex';
    float str2 = 'Fatjo';
    cout << "Steps: \n\t'Alex' = [" << str1 << "]\n\t'Fatjo' = [" << str2 << "]\n\t\tproduct = ["
         << str1 << "] / [" << str2 << "]\n\t\t\t->" << prod << endl;
    return 0;
}

/*=========================Output====================================
Product = 11
Product = -95
Product = 176
Product = 6
Product = 199
Product = -57
Steps:
        'Alex' = [1.09762e+09]
        'Fatjo' = [1.63502e+09]
                product = [1.09762e+09] / [1.63502e+09]
                        ->0.671321

Process finished with exit code 0
===================================================================
*/
//#####################################################[END]#####################################################

3. Write a C++ program to create, open, write and read a text file.
=========================SourceCode================================
#include <fstream>
#include <iostream>
#include <string>
using namespace std;
class library {
public:
    library() {};
    struct book {
        string title{""};
        string author{""};
        int price{};
        int id{};
    };
    book b;//to access the book structs members from functions
    void add_book() {
        ofstream outFile;
        outFile.open("book.txt", ios::app);

        cout << "ID: ";
        cin >> b.id;
        outFile << b.id << " ";

        cout << "Title: ";
        cin >> b.title;
        outFile << b.title << " ";

        cout << "Author: ";
        cin >> b.author;
        outFile << b.author << " ";

        cout << "Price: ";
        cin >> b.price;
        outFile << b.price << ">\n";

        outFile.close();
        cout << "Book added successfully!" << endl;
    }
    void delete_book() {
        int idtmp;
        cout << "Enter book ID to delete: ";
        cin >> idtmp;
        if (idtmp == b.id) {
            ifstream inFile;
            inFile.open("book.txt");
            ofstream outFile;
            remove("book.txt");
            rename("temp.txt", "book.txt");
            cout << "Deleted" << endl;
        }else {
            try{throw 1;}
            catch(int x){cout << "Book ID not found" << endl;}
        }
    }
    void edit_book() {
        ofstream outFile;
        outFile.open("book.txt", ios::app);
        cout << "ID: ";
        cin >> b.id;
        outFile << b.id << " ";
        cout << "Price: ";
        cin >> b.price;
        outFile << b.price << ">\n";
        outFile.close();//closes file once done writing
    }
    //to override the book struct members with 'NULL' values.
    void reset_book() {
        int id{NULL}, price{NULL};
        string title{NULL}, author{NULL};
        this->b.id = id;
        this->b.title = title;
        this->b.author = author;
        this->b.price = price;
    }
    void display_book() {
        ifstream inFile;
        inFile.open("book.txt");
        cout << "ID: " << b.id << "\nTitle: " << b.title << "\nAuthor: " << b.author << "\nPrice: " << b.price << endl;
    }
};
class ui_menu : public library {
public:
    void menu_opt() {
        cout << "[1]-Add book"
             << "\n[2]-Edit Book"
             << "\n[3]-Display Book"
             << "\n[4]-Delete Book"
             << "\n[0]-Quit" << endl;
    }
    virtual void main_menu() {
        int user_input;
        do {
            menu_opt();
            cin >> user_input;
            switch (user_input) {
                //cout << "[1]-Add book" << "\n[2]-Edit Book" << "\n[3]-Delete Book" << "\n[0]-Quit" << endl;
                //cin >> user_input;
                case 1:
                    library::add_book();
                    break;
                case 2:
                    library::edit_book();
                    break;
                case 3:
                    library::display_book();
                    break;
                case 4:
                    library::delete_book();
                    library::reset_book();
                    break;
                case 0:
                    EXIT_SUCCESS;
                    break;
                default: //if user doesnt enter an int between 0-4
                    try {throw user_input;} //tests if user input is valid
                    //if not then this will catch the error and prints the error message
                    catch (int user_input) {cout << "Error occurred: \n\tLocation: ui_menu::main_menu->'switch'" << endl;}
                    break;
            }
        }while (user_input != 0);//loops
    }
};

int main() {
    library::book b{};//create a book object
    ui_menu menu{};   //create a menu object
    menu.main_menu(); //call the main menu function
    return 0;
}
//#####################################################[END]#####################################################
