# CSCI 1250 Lab 0: Grade Calculator (Programming Fundamentals)

## Learning Objectives
By the end of this lab, you will be able to:
- **Declare** and **initialize** variables with meaningful names
- Use the `Console.ReadLine()` function to gather user data
- **Parse** string input into appropriate numeric data types
- Apply mathematical operators to perform basic calculations
- Use string interpolation to format and display results
- Apply proper C# syntax conventions
- **Define** and **call** functions with parameters and return values
- Implement basic control flow using while loops

---

# Basic Grade Calculator

## Scenario
You're a student in CSCI 1100, and you want to calculate your current grade in the class. Your final grade is calculated using the following weights:
- Exit Tickets Average: 1/6 (≈16.67%)
- Quiz Average: 1/6 (≈16.67%)
- Lab Average: 1/6 (≈16.67%)
- Final Project: 3/6 (50%)

Your task is to create a C# program that asks for your scores in each category and calculates your overall class grade.

## Part 1: Variable Declaration and Getting User Input

### Understanding Variables
Before we start coding, let's understand what we're doing when we work with variables:

- **Variable Declaration**: This is when we create a new variable name in our program
- **Variable Initialization**: This is when we assign a value to that variable for the first time

In C#, declaration and initialization happen together. When we write:
```csharp
string name = "Alice"
```
We are both **declaring** a variable called `name` AND **initializing** it with the value `"Alice"`.

### Your Task: Gather Input and Store in Variables

1. **Declare and initialize** a variable to store the exit tickets average:
   ```csharp
   Console.WriteLine("Enter your exit tickets average:");
   string exitTickets = Console.ReadLine();
   ```

2. **Declare and initialize** variables for the other grade components using meaningful variable names:
   - Quiz average
   - Lab average  
   - Final project score

**Syntax Reminder**: 
- End all statements/lines in ;
- Variable names should be descriptive (`quizAverage` not `q`)
- Use lowercase letters for the first word, with capital letters for the second (`finalProject` not `final_project`)
- No spaces in variable names (`exit tickets` ❌, `exitTickets` ✅)

## Part 2: Parsing Data Types

### Understanding Data Types and Parsing
Right now, all your variables contain **strings** (text), but we need **numbers** to do math! 

- **Parsing**: Converting data from one type to another (in this case, string to float)
- The `Console.Readline()` function takes strings as a data type
- We must **parse** these strings into floats before we can perform mathematical operations

### Your Task: Parse Strings to Floats

Convert each string input to a float by **reassigning** the variable. You can do this in two ways:

**Reassign the same variable to the new data type.**
```csharp
float exitTicketsAverage = Convert.ToSingle(exitTickets);
```

**Syntax Reminders**:
- Remember to end your statement in ;
- Methods end in ();
- Parentheses are required: `ToSingle(exitTickets)`
- Don't forget the assignment operator `=`
- Variable names are case-sensitive (`ExitTickets` ≠ `exitTickets`)

## Part 3: Mathematical Operations and Variable Assignment

### Understanding the Calculation
Now we'll perform the weighted average calculation. Remember, each component has a different weight:
- Exit Tickets: 1/6 of total grade
- Quizzes: 1/6 of total grade  
- Labs: 1/6 of total grade
- Final Project: 3/6 of total grade (half the grade!)

### Your Task: Calculate and Store the Result

Here's an example of how to calculate the weighted value for exit tickets:

```csharp
float exitTicketsAverage = Convert.ToSingle(exitTickets) * (1f/6f);
```

Now you need to:
1. Calculate the weighted value for each of the other three components (quizzes, labs, final project)
2. **Declare and initialize** a variable called `overallGrade` that adds all four weighted components together

**Syntax Reminders**:
- Use parentheses to control order of operations, if necessary.
- Multiplication operator is `*` 
- Addition operator is `+`
- Division operator is `/`
- C# follows standard mathematical order of operations (PEMDAS)

## Part 4: Output Formatting with String Concatenation

### Understanding Concatenation
String concatenation is the process of embedding variables directly into a printed output. 

### Your Task: Display the Results

Use string concatenation to display the final grade. The syntax is:
```csharp
Console.WriteLine($"Text {variableName}");
```

**String Concatenation Breakdown**:
- `$"..."` - The `$` before the quotes makes it a formatted string
- `{variableName}` - Curly braces contain the variable to display
- Everything else prints exactly as written

**Important Syntax Notes**:
- Don't forget the `$` before the opening quote!
- Curly braces `{}` are required around variable names
- The Console.WriteLine statement needs parentheses: `Console.WriteLine("...")`

## Sample Run

Here's what your program should look like when it runs:

```
Enter your exit tickets average: 
85
Enter your quiz average: 
92
Enter your lab average: 
88
Enter your final project score:
90
Your overall grade in CSCI 1100 is: 89.166664
```

## Key Programming Terminology Review

As you work through this lab, you're applying these important concepts:

- **Variable Declaration**: Creating new variable names in your program
- **Variable Initialization**: Assigning values to variables for the first time  
- **Parsing**: Converting data from one type (string) to another (float)
- **Assignment Operator**: The `=` symbol that stores values in variables
- **String Concatenation**: A formatted string that embeds variables using `$"..."` syntax

**Common Syntax Errors to Avoid**:
- Forgetting parentheses in function calls: `Convert.ToSingle exitTickets` ❌ vs `Convert.ToSingle(exitTickets)` ✅
- Missing the `$` in concatenation: `"Grade: {grade}"` ❌ vs `$"Grade: {grade}"` ✅  
- Using spaces in variable names: `exit tickets` ❌ vs `exitTickets` ✅
- Wrong quotation marks: `"Hello'` ❌ vs `"Hello"` ✅

## Submission Requirements

Submit your completed `gradeCalculator.cs` file. Make sure your code:
- [ ] Uses `Console.ReadLine()` to gather all four grade components
- [ ] Converts all inputs to floats
- [ ] Stores values in appropriately named variables
- [ ] Correctly applies the weighting scheme (1/6, 1/6, 1/6, 3/6)
- [ ] Uses string concatenation to display the final result
- [ ] Includes appropriate prompts so the user knows what to enter

## Testing Your Code

Test your program with these sample inputs to verify it's working correctly:

**Test Case 1:**
- Exit Tickets: 80, Quizzes: 85, Labs: 90, Final Project: 95
- Expected Result: 90

**Test Case 2:**
- Exit Tickets: 100, Quizzes: 100, Labs: 100, Final Project: 100
- Expected Result: 100

**Test Case 3:**
- Exit Tickets: 70, Quizzes: 75, Labs: 80, Final Project: 85
- Expected Result: 80

Good luck, and remember: this is your first step into the world of programming!

- Original Python Version Credit: Professor Ryan Haas, ETSU Dept. of Computing


