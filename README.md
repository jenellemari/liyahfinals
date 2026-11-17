import random

modules = [

    ["Introduction to Programming", [

        ["What is programming?",
         "Programming means writing step-by-step instructions that tell a computer what to do.",
         "A computer is very fast, but it cannot think for itself. It does exactly what the instructions say, in the exact order they are written. A programmer writes those instructions in a language the computer can understand.",
         'print("message")   # one simple instruction',
         'print("I am following an instruction!")',
         "I am following an instruction!",
         "Every app, game, and website you use was built from instructions written by programmers.",
         '''Mistake: Expecting the computer to guess what you mean.
        Fix: Be exact. The computer only does what you tell it to do.'''],

        ["What is Python?",
         "Python is a popular programming language that is easy to read and easy to learn.",
         "Python uses simple, English-like words, so beginners can start quickly. Professionals also use it every day. Python is an interpreted language: it reads your code and carries it out one line at a time.",
         "Python files are saved with the .py ending, for example: hello.py",
         '''print("Python is fun!")
        print("Let's learn it step by step.")''',
         '''Python is fun!
        Let's learn it step by step.''',
         "Python is used to build websites, analyze data, create games, control robots, and automate boring tasks.",
         '''Mistake: Saving the file as hello.txt.
        Fix: Save it as hello.py so your IDE knows it is a Python file.

        Mistake: Thinking you must be great at math to learn Python.
        Fix: Basic Python needs only simple arithmetic. Logic and practice matter more.'''],

        ["What is an algorithm?",
         "An algorithm is a list of clear steps for solving a problem or finishing a task.",
         "Think of a recipe. The steps must be clear and in the right order. Programmers plan the algorithm first, then turn each step into code.",
         '''1. Start
        2. Do step one
        3. Do step two
        4. Finish''',
        '''print("Step 1: Boil the water")
        print("Step 2: Add the noodles")
        print("Step 3: Wait three minutes")
        print("Step 4: Add the seasoning")''',
                 '''Step 1: Boil the water
        Step 2: Add the noodles
        Step 3: Wait three minutes
        Step 4: Add the seasoning''',

        "A GPS app uses an algorithm to find the fastest route. Online shops use one to sort products by price.",
        '''Mistake: Putting the steps in the wrong order, like adding the noodles before boiling the water.
        Fix: Read your steps the way a robot would. If the order is wrong, the result is wrong.'''],

                ["What can we build with programming?",
                 "An application (app) is a program that people use, such as a game, a website, or a mobile app.",
                 "Most programs follow three parts: they take input, process it, and give output. A shop program, for example, takes prices, adds them up, and shows the total.",
                 "Input -> Process -> Output",
                 'print("Total:", 50 * 3)',
                 "Total: 150",
                 "ATMs, calculators, school grading systems, and video games all work this way.",
                 '''Mistake: Thinking programs only run on computers.
        Fix: Phones, ATMs, TVs, and even cars run programs too.'''],
            ]],

    ["Getting Started with Python", [

        ["Installing Python",
         "Installing Python means putting the Python interpreter on your computer so it can run Python code.",
         "Download the installer from python.org. On Windows, tick the box 'Add Python to PATH' before clicking Install. Afterward, open a terminal and check that Python was installed.",
         "python --version",
         "python --version     (typed in a terminal, not in a .py file)",
         "Python 3.12.1     (your version number may be different)",
         "Every Python programmer starts by installing Python, whether they use Windows, Mac, or Linux.",
         '''Mistake: Forgetting to tick 'Add Python to PATH' and later seeing "'python' is not recognized".
Fix: Run the installer again, choose Modify or Repair, and tick the PATH box.'''],

        ["What is an IDE?",
         "An IDE (Integrated Development Environment) is a program where you write, run, and fix your code. PyCharm is an IDE.",
         "An IDE has a code editor with colors, hints that point out mistakes, and a Run button. It makes programming faster than using a plain notepad.",
         '''File > New Project
Right-click the project > New > Python File
Type your code, then click Run''',
         'print("My first program")',
         "My first program",
         "Professional programmers use IDEs every day because they catch mistakes early.",
         '''Mistake: Writing code in Word, which can change straight quotes into curly quotes.
    Wrong: print(“Hi”)
    Right: print("Hi")
Fix: Write your code in an IDE such as PyCharm.'''],

        ["Running a program",
         "Running a program means telling Python to read your file and carry out its instructions.",
         "In PyCharm, click the green Run button (or press Shift+F10). The output appears in the Run window at the bottom. You can also run a file from a terminal.",
         "python filename.py",
         '''print("Program started")
print("Program finished")''',
         '''Program started
Program finished''',
         "You run your program every time you want to test a change you made.",
         '''Mistake: Running the command from the wrong folder and seeing "can't open file".
Fix: Use cd folder_name to move into your project folder first, then run python main.py.'''],

        ["The Python interpreter",
         "The interpreter is the part of Python that reads your code and runs it, one line at a time.",
         "Python starts at the first line, runs it, then moves to the next. If it finds an error, it stops and shows a message. You can also type code straight into the interpreter by typing python in a terminal.",
         '''>>> print("Hi")
Hi''',
         '''print("First")
print("Second")
print("Third")''',
         '''First
Second
Third''',
         "Interactive mode is great for testing a small idea quickly before putting it in a program.",
         '''Mistake: Typing the >>> symbols inside your program file.
Fix: >>> is only the interpreter's prompt. Type just the code that comes after it.'''],
    ]],

    ["Basic Syntax", [

        ["What is syntax?",
         "Syntax is the set of rules for writing code correctly in a programming language.",
         "Just like English has grammar, Python has syntax. If you break a rule, Python cannot understand the line and shows a SyntaxError.",
         "function_name(value)",
         'print("Syntax matters")',
         "Syntax matters",
         "Knowing the syntax lets you write code that works the first time and fix errors faster.",
         '''Mistake: Writing print without brackets.
        Wrong: print "Hi"
        Right: print("Hi")'''],

        ["The print() function",
         "The print() function displays text or values on the screen.",
         "Text must be inside quotes. Text inside quotes is called a string. You can print several things at once by separating them with commas, and Python puts a space between them.",
         '''print(value)
        print(value1, value2)''',
         '''print("Hello")
        print("Age:", 15)
        print(2 + 3)''',
         '''Hello
        Age: 15
        5''',
         "Programs use print() to show messages, scores, and results to the user.",
         '''Mistake: Using a capital letter.
        Wrong: Print("Hi")
        Right: print("Hi")

    Mistake: Forgetting the closing bracket.
        Wrong: print("Hi"
        Right: print("Hi")'''],

            ["Comments",
             "A comment is a note for humans. Python ignores it completely.",
             "A comment starts with the # symbol. Programmers use comments to explain their code or to switch a line off for a moment. A comment can be on its own line or at the end of a line.",
             "# This is a comment",
             '''# This line is ignored
    print("Visible")  # a note at the end of a line
    # print("Hidden")''',
             "Visible",
             "In a team project, comments help other programmers (and your future self) understand why the code was written.",
             '''Mistake: Using the comment style of another language.
        Wrong: // This is a comment
        Right: # This is a comment'''],

            ["Indentation",
             "Indentation is the empty space at the start of a line. Python uses it to group lines of code together.",
             "Lines that belong together must be indented by the same amount. The standard is 4 spaces. A group of indented lines is called a block. Other languages use brackets for this, but Python uses spaces.",
             '''if condition:
        indented line''',
             '''if 5 > 3:
        print("Five is bigger")
        print("This is inside the block")
    print("This is outside the block")''',
             '''Five is bigger
    This is inside the block
    This is outside the block''',
             "Indentation is used in if statements, loops, and functions, which you will learn soon.",
             '''Mistake: Adding extra spaces for no reason.
        Wrong:   print("Hi")      (starts with spaces)
        Right: print("Hi")
    Python shows: IndentationError: unexpected indent
    
    Mistake: Forgetting to indent after a colon.
        Wrong: if 5 > 3:
               print("Yes")
        Right: if 5 > 3:
                   print("Yes")'''],

            ["Basic syntax rules",
             "A few simple rules apply to almost every line of Python code.",
             '''1. Python is case-sensitive: name and Name are different.
    2. Every opening bracket or quote needs a closing one.
    3. Lines that start a block (like if) end with a colon.
    4. Use 4 spaces for each level of indentation.''',
             '''print("text")      # lowercase name, brackets, quotes
    if condition:      # colon at the end''',
             '''print("Rules are easy")
    print('Single quotes work too')''',
             '''Rules are easy
    Single quotes work too''',
             "Following these rules means fewer error messages and less time spent fixing code.",
             '''Mistake: Mixing quote types.
        Wrong: print("Hi')
        Right: print("Hi")'''],
        ]],

    ["Variables and Data Types", [

        ["What is a variable?",
         "A variable is a named container in the computer's memory that stores a value.",
         "Think of a labeled box. The label is the variable's name, and what is inside is its value. You can look at the value, or replace it with a new one.",
         "variable_name = value",
         '''score = 10
        print(score)''',
         "10",
         "A game uses variables to remember your score, your lives, and your player name.",
         '''Mistake: Thinking = means "equals" like in math.
        Fix: In Python, = means "store the value on the right into the name on the left".'''],

        ["Why do programmers use variables?",
         "Variables let programmers store information once and use it again and again.",
         "Without variables you would type the same value everywhere. With a variable, you change it in one place and the whole program updates. Variables also let a program remember information that changes, like a score.",
         '''price = 20
        total = price * 3''',
         '''price = 20
        print(price * 2)
        print(price * 3)''',
         '''40
        60''',
         "An online store keeps each item's price in a variable so it can calculate totals and discounts.",
         '''Mistake: Typing the same number in many places.
        Wrong: print(20 * 2) and print(20 * 3)
        Right: price = 20, then use price everywhere
        Fix: Store the value once. Changing it later takes just one edit.'''],

        ["How to create a variable",
         "Creating a variable means giving a name to a value using the = sign.",
         "Python creates the variable the first time you give it a value. You do not have to say what kind of value it will hold. You can change the value later by assigning a new one.",
         "variable_name = value",
         '''name = "Ana"
age = 15
age = 16
print(name, age)''',
         "Ana 16",
         "Websites store your username and age in variables when you sign up.",
         '''Mistake: Putting the value on the left.
    Wrong: 15 = age
    Right: age = 15

Mistake: Using a variable before creating it.
    Wrong: print(score)    (Python shows a NameError)
    Right: score = 10 first, then print(score)'''],

        ["Rules for naming variables",
         "Variable names must follow a few rules so Python can understand them.",
         '''1. Use letters, numbers, and underscores only.
2. A name cannot start with a number.
3. No spaces or hyphens. Use an underscore instead (snake_case).
4. Names are case-sensitive: score and Score are different.
5. Do not use Python keywords such as if, for, or while.
Choose names that describe the value, like player_name.''',
         "my_variable_name = value",
         '''first_name = "Ana"
score1 = 90
print(first_name, score1)''',
         "Ana 90",
         "Clear names make code easier to read for you and for other programmers.",
         '''Mistake: Starting a name with a number.
    Wrong: 1score = 5
    Right: score1 = 5

Mistake: Using a hyphen or a space.
    Wrong: my-name = "Ana"
    Right: my_name = "Ana"'''],

        ["Understanding strings",
         "A string is text. In Python it is written inside quotation marks.",
         "You can use double quotes or single quotes. The + sign joins strings together, and len() counts how many characters a string has, including spaces.",
         '''text = "your words here"
len(text)''',
         '''first = "Hello"
second = "World"
print(first + " " + second)
print(len(first))''',
         '''Hello World
5''',
         "Names, emails, passwords, and chat messages are all strings.",
         '''Mistake: Forgetting the quotes.
    Wrong: name = Ana    (Python thinks Ana is a variable and shows a NameError)
    Right: name = "Ana"'''],

        ["Understanding integers",
         "An integer (int) is a whole number with no decimal point. It can be positive, negative, or zero.",
         "Integers are used for counting things. You can do math with them, like adding and subtracting.",
         "count = 10",
         '''apples = 5
oranges = 3
print(apples + oranges)
print(-4)''',
         '''8
-4''',
         "Ages, scores, and the number of items in a shopping cart are integers.",
         '''Mistake: Using a comma inside a big number.
    Wrong: population = 1,000
    Right: population = 1000
Python reads 1,000 as two separate values, not one number.'''],

        ["Understanding floats",
         "A float is a number with a decimal point.",
         "Use floats when you need parts of a whole, like prices or measurements. Dividing with / always gives a float.",
         "price = 19.99",
         '''price = 19.99
height = 1.5
print(price)
print(10 / 4)''',
         '''19.99
2.5''',
         "Money, temperatures, weights, and averages are floats.",
         '''Mistake: Using a comma as the decimal point.
    Wrong: pi = 3,14
    Right: pi = 3.14'''],

        ["Understanding booleans",
         "A boolean has only two possible values: True or False.",
         "Booleans answer yes-or-no questions. Comparing two values gives a boolean. Notice the capital first letter: True and False.",
         "is_ready = True",
         '''is_raining = False
print(is_raining)
print(5 > 3)''',
         '''False
True''',
         "A game checks booleans like game_over or has_key to decide what happens next.",
         '''Mistake: Writing the value in lowercase.
    Wrong: is_ready = true
    Right: is_ready = True'''],

        ["Difference between data types",
         "A data type tells Python what kind of value something is.",
         '''Python has different types for text (str), whole numbers (int), decimals (float), and True/False (bool). The type() function tells you which one a value is.
Types matter because they behave differently: 5 + 5 gives 10, but "5" + "5" gives "55".''',
         "type(value)",
         '''print(type("Hi"))
print(type(7))
print(type(7.5))
print(type(True))''',
         '''<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>''',
         "When a program gives a strange result, checking the type is often the fastest way to find the cause.",
         '''Mistake: Expecting "5" + "5" to equal 10.
    Wrong: print("5" + "5")    shows 55
    Right: print(5 + 5)        shows 10'''],

        ["Examples in real-life programming",
         "Real programs combine different data types to describe real things.",
         "A student record might use a string for the name, an integer for the age, a float for the average, and a boolean for the enrollment status.",
         "One variable for each piece of information.",
         '''student_name = "Ana"
student_age = 15
average = 92.5
is_enrolled = True
print(student_name, student_age, average, is_enrolled)''',
         "Ana 15 92.5 True",
         "School systems, online stores, and games all store information this way.",
         '''Mistake: Storing a number as a string and then trying to do math with it.
    Wrong: age = "15"
    Right: age = 15'''],

        ["Common mistakes with variables",
         "Most beginner errors with variables come from a few small slips.",
         "When you see an error, check these first: Is the name spelled the same everywhere? Are strings inside quotes? Did you use the right capital letters? Did you create the variable before using it?",
         "Checklist: spelling, quotes, capital letters, create first.",
         '''user_name = "Ben"
user_age = 14
print(user_name)
print(user_age)''',
         '''Ben
14''',
         "Running through this checklist solves most NameError messages in seconds.",
         '''Mistake: Misspelling the name.
    Wrong: score = 10 then print(scor)
    Right: print(score)

Mistake: Wrong capital letter.
    Wrong: score = 10 then print(Score)
    Right: print(score)'''],
    ]],

    ["Input and Output", [

        ["Output with print()",
         "Output is any information a program shows to the user. In Python, print() is the main way to show output.",
         "Besides text, print() can show numbers and the results of calculations. The special code \\n starts a new line inside a string.",
         'print("first line\\nsecond line")',
         '''print("Line 1\\nLine 2")
print("Name:", "Ana")''',
         '''Line 1
Line 2
Name: Ana''',
         "Menus, receipts, game messages, and reports are all made with output.",
         '''Mistake: Using a forward slash for a new line.
    Wrong: print("Line 1/nLine 2")
    Right: print("Line 1\\nLine 2")'''],

        ["Input with input()",
         "The input() function asks the user to type something and gives back what they typed.",
         "The program pauses until the user presses Enter. The text inside the brackets is the prompt the user sees. Save the answer in a variable so you can use it later.",
         'variable = input("prompt")',
         '''name = input("What is your name? ")
print("Hello,", name)''',
         '''What is your name? Ana
Hello, Ana''',
         "Login screens, search boxes, and quiz games all use input.",
         '''Mistake: Not saving the answer.
    Wrong: input("Name: ")
    Right: name = input("Name: ")
Without a variable, the answer is lost.'''],

        ["Type conversion",
         "Type conversion changes a value from one data type to another.",
         "input() always gives back a string, even if the user types digits. To do math, convert the text with int() for whole numbers or float() for decimals. Use str() to turn a number into text.",
         '''int(value)
float(value)
str(value)''',
         '''age = int(input("Age: "))
print("Next year you will be", age + 1)''',
         '''Age: 15
Next year you will be 16''',
         "A calculator must convert the numbers you type before it can add them.",
         '''Mistake: Doing math on text.
    Wrong: age = input("Age: ")     then age + 1 causes a TypeError
    Right: age = int(input("Age: "))'''],

        ["Putting input and output together",
         "Many programs follow the same pattern: ask for input, process it, and show output.",
         "First ask the user for values. Then convert them to the right type. Then calculate. Finally print the result.",
         '''value = float(input("..."))
print(result)''',
         '''price = float(input("Price: "))
quantity = int(input("Quantity: "))
print("Total:", price * quantity)''',
         '''Price: 2.5
Quantity: 4
Total: 10.0''',
         "A cashier program asks for a price and a quantity and shows the total.",
         '''Mistake: Using int() on a decimal number.
    Wrong: int("2.5")    causes a ValueError
    Right: float("2.5")

Mistake: Typing letters when a number is expected also causes a ValueError.'''],
    ]],

    ["Operators", [

        ["Arithmetic operators",
         "Arithmetic operators are symbols that do math.",
         '''+  add        -  subtract    *  multiply
/  divide (gives a float)
// floor division (drops the decimal part)
%  remainder        **  power''',
         "a + b     a // b     a % b     a ** b",
         '''print(10 + 3)
print(10 - 3)
print(10 * 3)
print(10 / 3)
print(10 // 3)
print(10 % 3)
print(2 ** 3)''',
         '''13
7
30
3.3333333333333335
3
1
8''',
         "Totals, change, discounts, and even/odd checks (number % 2) all use arithmetic operators.",
         '''Mistake: Using ^ for power.
    Wrong: 2 ^ 3
    Right: 2 ** 3

Mistake: Using x for multiply.
    Wrong: 4 x 5
    Right: 4 * 5'''],

        ["Comparison operators",
         "Comparison operators compare two values and give back True or False.",
         '''==  equal to        !=  not equal to
>   greater than    <   less than
>=  greater than or equal to
<=  less than or equal to''',
         "a == b     a != b     a >= b",
         '''age = 15
print(age == 15)
print(age != 15)
print(age >= 18)
print(age < 18)''',
         '''True
False
False
True''',
         "Programs compare values to check passwords, ages, scores, and prices.",
         '''Mistake: Using one = to compare.
    Wrong: age = 15      (this stores 15 in age)
    Right: age == 15     (this asks if age is 15)'''],

        ["Logical operators",
         "Logical operators combine True/False values.",
         '''and  gives True only if both sides are True.
or   gives True if at least one side is True.
not  flips True to False and False to True.''',
         "a and b     a or b     not a",
         '''age = 15
has_id = True
print(age >= 13 and has_id)
print(age >= 18 or has_id)
print(not has_id)''',
         '''True
True
False''',
         "A login system checks that the username is correct and the password is correct.",
         '''Mistake: Shortening a double comparison.
    Wrong: age >= 13 and <= 19
    Right: age >= 13 and age <= 19
Each side of and / or must be a full comparison.'''],

        ["Assignment operators",
         "Assignment operators store a value in a variable, and some also update it.",
         "= stores a value. += adds to the variable, -= subtracts, *= multiplies, and /= divides. x += 1 is a short way of writing x = x + 1.",
         '''x = 5
x += 1
x -= 1
x *= 2''',
         '''score = 10
score += 5
score -= 2
score *= 2
print(score)''',
         "26",
         "Scores, counters, and bank balances change over time with these operators.",
         '''Mistake: Writing the symbols in the wrong order.
    Wrong: x =+ 1     (this just stores +1)
    Right: x += 1'''],

        ["Order of operations",
         "Python follows rules about which operation to do first.",
         '''From first to last: brackets ( ), then **, then * / // %, then + -.
Comparisons come after math, and and / or come last. Use brackets when you want to be sure.''',
         "(a + b) * c",
         '''print(2 + 3 * 4)
print((2 + 3) * 4)
print(2 ** 3 * 2)''',
         '''14
20
16''',
         "Bills, averages, and formulas need the right order to give the right answer.",
         '''Mistake: Forgetting brackets when finding an average.
    Wrong: average = a + b / 2
    Right: average = (a + b) / 2'''],
    ]],

    ["Conditional Statements", [

        ["The if statement",
         "An if statement runs a block of code only when its condition is True.",
         "Python checks the condition. If it is True, the indented lines run. If it is False, Python skips them.",
         '''if condition:
    code to run''',
         '''temperature = 35
if temperature > 30:
    print("It is hot today")''',
         "It is hot today",
         "Apps use if statements to decide things like whether to show a warning or unlock a level.",
         '''Mistake: Forgetting the colon.
    Wrong: if temperature > 30
    Right: if temperature > 30:

Mistake: Forgetting to indent.
    Wrong: if temperature > 30:
           print("Hot")
    Right: if temperature > 30:
               print("Hot")'''],

        ["if and else",
         "The else part runs when the if condition is False.",
         "Together, if and else let your program choose between two paths. Exactly one of them runs.",
         '''if condition:
    code if True
else:
    code if False''',
         '''age = 15
if age >= 18:
    print("Adult")
else:
    print("Minor")''',
         "Minor",
         "A website shows 'Welcome back' if you are logged in, and a login form if you are not.",
         '''Mistake: Putting a condition after else.
    Wrong: else age < 18:
    Right: else:'''],

        ["Using elif",
         "elif checks another condition when the earlier conditions were False.",
         "Python reads from the top. The first condition that is True runs, and all the rest are skipped. If none is True, the else block runs.",
         '''if condition1:
    ...
elif condition2:
    ...
else:
    ...''',
         '''score = 85
if score >= 90:
    print("Grade A")
elif score >= 80:
    print("Grade B")
elif score >= 70:
    print("Grade C")
else:
    print("Keep trying")''',
         "Grade B",
         "Grading systems, ticket prices by age, and game difficulty levels use elif chains.",
         '''Mistake: Using separate if statements when you want only one result.
    Wrong: if score >= 90:      (a score of 95 would print both
               print("A")        "A" and "B")
           if score >= 80:
               print("B")
    Right: use elif for the second check.'''],

        ["Nested conditions",
         "A nested condition is an if statement placed inside another if statement.",
         "The inner if is only checked when the outer condition is True. Each level is indented 4 more spaces.",
         '''if outer_condition:
    if inner_condition:
        code''',
         '''age = 16
has_ticket = True
if age >= 13:
    if has_ticket:
        print("Welcome to the show")
    else:
        print("Please buy a ticket")
else:
    print("Too young for this show")''',
         "Welcome to the show",
         "An ATM checks that your card is valid, and then checks your PIN, and then checks your balance.",
         '''Mistake: Lining up else with the wrong if.
    Wrong: the inner else written at the same indentation as the outer if
    Right: indent the else to match the if it belongs to'''],
    ]],

    ["Loops", [

        ["What is a loop?",
         "A loop repeats a block of code many times.",
         "Instead of copying the same line again and again, you write it once and tell Python how many times to repeat. Python has two kinds of loops: for loops and while loops.",
         '''for variable in range(times):
    code to repeat''',
         '''for number in range(3):
    print("Hello")''',
         '''Hello
Hello
Hello''',
         "Games repeat the game loop many times every second. Apps repeat tasks like checking for new messages.",
         '''Mistake: Copying the same line many times.
    Wrong: print("Hello") written 100 times
    Right: use a loop and write it once'''],

        ["for loops",
         "A for loop repeats once for each value in a sequence.",
         "range(5) gives the numbers 0 to 4. range(1, 6) gives 1 to 5. The stop number is never included. The loop variable takes the next value each round.",
         '''for variable in range(start, stop):
    code''',
         '''for i in range(1, 6):
    print("Number", i)''',
         '''Number 1
Number 2
Number 3
Number 4
Number 5''',
         "Printing a multiplication table, counting down a timer, or going through every student in a class.",
         '''Mistake: Expecting range(1, 5) to include 5.
    Wrong: range(1, 5)    gives 1, 2, 3, 4
    Right: range(1, 6)    gives 1, 2, 3, 4, 5'''],

        ["while loops",
         "A while loop repeats as long as its condition is True.",
         "Python checks the condition before every round. Something inside the loop must eventually make the condition False, or the loop will never stop.",
         '''while condition:
    code''',
         '''count = 1
while count <= 3:
    print("Count is", count)
    count += 1''',
         '''Count is 1
Count is 2
Count is 3''',
         "Keep asking for a password until the user types it correctly.",
         '''Mistake: Forgetting to update the variable.
    Wrong: the loop never changes count, so it never ends (an infinite loop)
    Right: add count += 1 inside the loop
If this happens, press the red Stop button in PyCharm.'''],

        ["break",
         "The break statement stops a loop immediately.",
         "Use break when you have found what you were looking for and do not need to keep going. Python jumps to the first line after the loop.",
         '''for ... :
    if condition:
        break''',
         '''for number in range(1, 10):
    if number == 4:
        break
    print(number)''',
         '''1
2
3''',
         "A search program stops as soon as it finds the item you want.",
         '''Mistake: Using break outside a loop.
    Wrong: break written on its own
    Right: break only works inside a for or while loop'''],

        ["continue",
         "The continue statement skips the rest of the current round and goes to the next one.",
         "Unlike break, the loop does not stop. It just jumps back to the top for the next round.",
         '''for ... :
    if condition:
        continue''',
         '''for number in range(1, 6):
    if number == 3:
        continue
    print(number)''',
         '''1
2
4
5''',
         "A program can skip blank lines or invalid entries and keep going.",
         '''Mistake: Mixing up break and continue.
    break stops the whole loop.
    continue skips only the current round.

Mistake: Using continue in a while loop before updating the counter.
    Wrong: continue placed before count += 1 (the loop gets stuck)
    Right: update the counter first, then use continue'''],
    ]],
]

predict_list = [
    [3, '''print("Hi")
print("There")''', [
        ["Hi\nThere",
         "Each print() starts a new line, so the two words appear on separate lines."],
        ["Hi There",
         "That would happen only if both words were inside one print(). Each print() ends with a new line."],
        ["HiThere",
         "Nothing joins the two words. Separate print() calls display on separate lines."],
    ]],
    [4, '''x = 5
x = 8
print(x)''', [
        ["8",
         "The second line replaces the old value. x holds only its newest value."],
        ["5",
         "5 was the first value, but x = 8 replaced it before print() ran."],
        ["13",
         "Assigning a new value does not add to the old one. It replaces it."],
    ]],
    [5, '''age = int("15")
print(age + 1)''', [
        ["16",
         "int() turns the text '15' into the number 15, so + 1 gives 16."],
        ["151",
         "That would happen if age were still text. int() converted it to a number, so + 1 adds."],
        ["15",
         "The + 1 is part of the print, so the result is one more than 15."],
    ]],
    [6, "print(17 % 5)", [
        ["2",
         "17 divided by 5 is 3 with 2 left over, and % gives the remainder."],
        ["3",
         "3 is how many times 5 fits in 17 (17 // 5), not the remainder."],
        ["3.4",
         "3.4 is 17 / 5. The % operator gives only the remainder."],
    ]],
    [6, '''x = 10
x += 5
x *= 2
print(x)''', [
        ["30",
         "x starts at 10, += 5 makes it 15, and *= 2 makes it 30."],
        ["15",
         "15 is the value after x += 5, but x *= 2 runs after that and doubles it."],
        ["20",
         "20 would be 10 * 2 without the += 5. Both lines change x, one after the other."],
    ]],
    [7, '''score = 75
if score >= 90:
    print("A")
elif score >= 70:
    print("B")
else:
    print("C")''', [
        ["B",
         "75 is not >= 90, but it is >= 70, so the elif block runs."],
        ["A",
         "75 is not greater than or equal to 90, so the first block is skipped."],
        ["C",
         "else only runs when every earlier condition is False. 75 >= 70 is True."],
    ]],
    [8, '''for i in range(3):
    print(i)''', [
        ["0\n1\n2",
         "range(3) gives 0, 1, and 2. It starts at 0 and stops before 3."],
        ["1\n2\n3",
         "range(3) starts at 0, not 1. To get 1 to 3 you would write range(1, 4)."],
        ["0\n1\n2\n3",
         "range(3) never includes 3. It stops just before it."],
    ]],
    [8, '''for n in range(1, 6):
    if n == 3:
        continue
    print(n)''', [
        ["1\n2\n4\n5",
         "continue skips the rest of the round when n is 3, so 3 is not printed. The loop carries on."],
        ["1\n2",
         "That would happen with break, which stops the whole loop. continue only skips one round."],
        ["1\n2\n3\n4\n5",
         "When n is 3, continue skips the print, so 3 is missing from the output."],
    ]],
]

debug_list = [
    [3, 'print("Hello World"',
     "Look at the end of the line. Something was opened but never closed.",
     ['print("Hello World")'],
     "Every opening bracket needs a closing bracket. The ( after print was never closed with )."],
    [3, 'Print("Hi")',
     "Python is case-sensitive. Look at the first letter.",
     ['print("Hi")'],
     "Function names are lowercase. Print with a capital P does not exist, so Python shows a NameError."],
    [4, 'my score = 10',
     "Variable names cannot contain spaces.",
     ['my_score = 10'],
     "Spaces are not allowed in variable names. Use an underscore instead: my_score."],
    [4, 'name = Ana',
     "Text must be written inside quotation marks.",
     ['name = "Ana"'],
     "Without quotes, Python thinks Ana is a variable name and shows a NameError. Quotes make it a string."],
    [5, 'age = input("Age: ") + 1',
     "input() gives back text. You cannot add a number to text.",
     ['age = int(input("Age: ")) + 1'],
     "input() returns a string, so + 1 causes a TypeError. Wrap it in int() to turn the text into a number first."],
    [6, 'if score = 100:',
     "One = stores a value. Which operator compares two values?",
     ['if score == 100:'],
     "= is assignment (store a value). == is comparison (check if equal). Conditions need ==."],
    [7, 'if age >= 18',
     "Lines that start a block must end with a special symbol.",
     ['if age >= 18:'],
     "An if line must end with a colon (:). The colon tells Python that an indented block comes next."],
    [8, 'for i in range 5:',
     "range is a function. How do you call a function?",
     ['for i in range(5):'],
     "range needs brackets around its number because it is a function: range(5)."],
]

practice_list = [
    [1, "What do programmers write to tell a computer what to do?",
     ["Step-by-step instructions", "Random guesses", "Only pictures"],
     "A program is a list of step-by-step instructions. The computer follows them in order."],
    [1, "Most programs follow Input -> Process -> Output. Which part shows the result to the user?",
     ["Output", "Input", "Process"],
     "Output is the information a program shows to the user, like the total on a receipt."],
    [2, "Which file ending do Python files use?",
     [".py", ".txt", ".doc"],
     "Python files are saved with .py, for example hello.py."],
    [2, "What does the Python interpreter do?",
     ["Reads your code and runs it one line at a time",
      "Draws pictures on the screen",
      "Saves your file on the internet"],
     "The interpreter reads your code line by line and carries out each instruction."],
    [3, "Which symbol starts a comment in Python?",
     ["#", "//", "$"],
     "A comment starts with #. Python ignores everything after it on that line."],
    [3, "How many spaces is the standard indentation in Python?",
     ["4", "1", "10"],
     "The standard is 4 spaces for each level of indentation."],
    [4, "Which of these is a valid variable name?",
     ["my_score", "my score", "1score"],
     "Names cannot have spaces and cannot start with a number. Use an underscore: my_score."],
    [4, "Which data type is the value True?",
     ["bool", "str", "int"],
     "True and False are booleans (bool)."],
    [4, "Which of these values is a float?",
     ["3.14", "3", '"3.14"'],
     "A float is a number with a decimal point. 3 is an int, and \"3.14\" in quotes is a string."],
    [5, "What type of value does input() always give back?",
     ["A string", "An integer", "A float"],
     "input() always gives text, even when the user types digits. Use int() or float() to convert it."],
    [5, "Which function turns the text \"15\" into the whole number 15?",
     ["int()", "str()", "print()"],
     "int() converts text into a whole number. str() does the opposite."],
    [6, "Which operator gives the remainder of a division?",
     ["%", "//", "/"],
     "% gives the remainder. // drops the decimal part, and / gives a float."],
    [6, "Which operator checks if two values are equal?",
     ["==", "=", "!="],
     "== compares two values. A single = stores a value in a variable."],
    [7, "What must an if line end with?",
     ["A colon (:)", "A semicolon (;)", "A period (.)"],
     "The colon tells Python that an indented block comes next."],
    [7, "When does the else block run?",
     ["When the if condition is False", "Every time", "Only when the if condition is True"],
     "else is the other path. It runs only when the if condition is False."],
    [8, "Which loop repeats as long as its condition is True?",
     ["while loop", "if statement", "print()"],
     "A while loop checks its condition before every round and stops when it becomes False."],
    [8, "What does break do inside a loop?",
     ["Stops the loop immediately", "Skips only one round", "Starts the program again"],
     "break ends the whole loop. continue is the one that skips a single round."],
    [8, "Which numbers does range(1, 4) give?",
     ["1, 2, 3", "1, 2, 3, 4", "0, 1, 2, 3"],
     "range starts at the first number and stops before the last one, so 4 is not included."],
]


XP_CORRECT = 10
XP_LESSON = 20
XP_PERFECT = 25

level_names = ["Python Newbie", "Code Explorer", "Bug finder", "Syntax Master", "Python Pro"]

BANNER = "^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^-^"
LINE = "--------------------------------------------------"
ROUND_SIZE = 5

xp = 0
last_level = 0
lessons_read = []

module_correct = []
module_total = []

for i in range(len(modules)):
    module_correct.append(0)
    module_total.append(0)

while True:

    if xp >= 1000:
        level = 4
    elif xp >= 600:
        level = 3
    elif xp >= 300:
        level = 2
    elif xp >= 100:
        level = 1
    else:
        level = 0

    if level > last_level:
        print("\n*** LEVEL UP! You are now a " + level_names[level] + "! ***")
        last_level = level

    print("\n" + BANNER)
    print("          PYTHON LEARNING SYSTEM")
    print(BANNER)
    print("[1] LEARN PYTHON")
    print("[2] MINI GAMES")
    print("[3] MY PROGRESS")
    print("[0] EXIT")
    print(LINE)
    print("Level:", level_names[level], "| XP:", xp)

    choice = input("\nEnter your choice: ").strip()

    if choice == "1":

        while True:
            print("\n" + BANNER)
            print("LEARN PYTHON".center(50))
            print(BANNER)

            for i in range(len(modules)):
                status = ""

                if i + 1 in lessons_read:
                    status = " (Completed)"

                print("[" + str(i + 1) + "]", modules[i][0] + status)

            print("[0] Back to Main Menu")

            module_choice = input("\nChoose a module: ").strip()

            if module_choice == "0":
                break

            elif module_choice.isdigit() and 1 <= int(module_choice) <= len(modules):

                number = int(module_choice)
                pages = modules[number - 1][1]

                for i in range(len(pages)):
                    page = pages[i]

                    print("\n" + BANNER)
                    print(modules[number - 1][0])
                    print("Page", i + 1, "of", len(pages))
                    print(BANNER)

                    print("\n[DEFINITION]")
                    print(page[1])

                    print("\n[EXPLANATION]")
                    print(page[2])

                    print("\n[SYNTAX]")
                    print(page[3])

                    print("\n[EXAMPLE]")
                    print(page[4])

                    print("\n[EXPECTED OUTPUT]")
                    print(page[5])

                    print("\n[REAL-LIFE APPLICATION]")
                    print(page[6])

                    print("\n[COMMON MISTAKES]")
                    print(page[7])

                    if i < len(pages) - 1:
                        reply = input("\nPress Enter for next page or Q to stop: ")

                        if reply.lower() == "q":
                            break

                else:
                    print("\nModule", number, "completed!")
                    print("You earned", XP_LESSON, "XP!")

                    if number not in lessons_read:
                        lessons_read.append(number)
                        xp += XP_LESSON

                    input("\nPress Enter to continue...")

            else:
                print("Invalid choice!")

    elif choice == "2":

        while True:
            print("\n" + BANNER)
            print("MINI GAMES".center(50))
            print(BANNER)
            print("[1] DEBUGGING CHALLENGE")
            print("[2] PREDICT THE OUTPUT")
            print("[3] PRACTICE QUESTIONS")
            print("[0] BACK TO MAIN MENU")

            game = input("\nChoose a game: ").strip()

            if game == "1":

                print("\n" + BANNER)
                print("DEBUGGING CHALLENGE".center(50))
                print(BANNER)

                items = random.sample(debug_list, ROUND_SIZE)
                correct = 0

                for i in range(ROUND_SIZE):

                    number = items[i][0]
                    broken = items[i][1]
                    hint = items[i][2]
                    fix = items[i][3][0]
                    why = items[i][4]

                    print("\n" + LINE)
                    print("Question", i + 1, "of", ROUND_SIZE)
                    print("Module:", modules[number - 1][0])
                    print("\nBroken code:")
                    print(broken)

                    print("\nHint:", hint)
                    answer = input("Enter the corrected code: ").strip()

                    if answer == fix:
                        print("\nCorrect!")
                        correct += 1
                        module_correct[number - 1] += 1
                        xp += XP_CORRECT
                        print("+10 XP")
                    else:
                        print("\nIncorrect!")
                        print("Correct code:", fix)

                    print("Explanation:", why)
                    module_total[number - 1] += 1

                print("\n" + LINE)
                print("Your score:", correct, "/", ROUND_SIZE)

                if correct == ROUND_SIZE:
                    print("Perfect score! Bonus XP:", XP_PERFECT)
                    xp += XP_PERFECT
                else:
                    print("Keep practicing!")

                input("\nPress Enter to continue...")

            elif game == "2":

                print("\n" + BANNER)
                print("PREDICT THE OUTPUT".center(50))
                print(BANNER)

                items = random.sample(predict_list, ROUND_SIZE)
                correct = 0

                for i in range(ROUND_SIZE):

                    number = items[i][0]
                    code = items[i][1]
                    choices = items[i][2]

                    print("\n" + LINE)
                    print("Question", i + 1, "of", ROUND_SIZE)
                    print("Module:", modules[number - 1][0])

                    print("\nCode:")
                    print(code)

                    print("\nWhat will the code display?")
                    print("A.", choices[0][0])
                    print("B.", choices[1][0])
                    print("C.", choices[2][0])

                    answer = input("\nYour answer (A/B/C): ").strip().lower()

                    while answer not in ["a", "b", "c"]:
                        answer = input("Please enter A, B, or C: ").strip().lower()

                    if answer == "a":
                        print("\nCorrect!")
                        print(choices[0][1])
                        correct += 1
                        module_correct[number - 1] += 1
                        xp += XP_CORRECT
                        print("+10 XP")
                    else:
                        print("\nIncorrect!")
                        print("The correct answer is:", choices[0][0])
                        print(choices[0][1])

                    print("\nActual output:")
                    print(choices[0][0])

                    module_total[number - 1] += 1

                print("\n" + LINE)
                print("Your score:", correct, "/", ROUND_SIZE)

                if correct == ROUND_SIZE:
                    print("Perfect score! Bonus XP:", XP_PERFECT)
                    xp += XP_PERFECT
                else:
                    print("Keep practicing!")

                input("\nPress Enter to continue...")

            elif game == "3":

                print("\n" + BANNER)
                print("PRACTICE QUESTIONS".center(50))
                print(BANNER)

                items = random.sample(practice_list, ROUND_SIZE)
                correct = 0

                for i in range(ROUND_SIZE):

                    number = items[i][0]
                    question = items[i][1]
                    choices = items[i][2]
                    explanation = items[i][3]

                    print("\n" + LINE)
                    print("Question", i + 1, "of", ROUND_SIZE)
                    print("Module:", modules[number - 1][0])

                    print("\n" + question)
                    print("\nA.", choices[0])
                    print("B.", choices[1])
                    print("C.", choices[2])

                    answer = input("\nYour answer (A/B/C): ").strip().lower()

                    while answer not in ["a", "b", "c"]:
                        answer = input("Please enter A, B, or C: ").strip().lower()

                    if answer == "a":
                        print("\nCorrect!")
                        correct += 1
                        module_correct[number - 1] += 1
                        xp += XP_CORRECT
                        print("+10 XP")
                    else:
                        print("\nIncorrect!")
                        print("Correct answer:", choices[0])

                    print("Explanation:", explanation)

                    module_total[number - 1] += 1

                print("\n" + LINE)
                print("Your score:", correct, "/", ROUND_SIZE)

                if correct == ROUND_SIZE:
                    print("Perfect score! Bonus XP:", XP_PERFECT)
                    xp += XP_PERFECT
                else:
                    print("Keep practicing!")

                input("\nPress Enter to continue...")

            elif game == "0":
                break

            else:
                print("Invalid choice!")

    elif choice == "3":

        print("\n" + BANNER)
        print("MY PROGRESS".center(50))
        print(BANNER)

        if xp >= 1000:
            level = 4
        elif xp >= 600:
            level = 3
        elif xp >= 300:
            level = 2
        elif xp >= 100:
            level = 1
        else:
            level = 0

        print("Current Level:", level_names[level])
        print("Total XP:", xp)

        print("\nLESSON PROGRESS")
        print(LINE)

        for i in range(len(modules)):

            if i + 1 in lessons_read:
                status = "Completed"
            else:
                status = "Not Completed"

            print(modules[i][0], "-", status)

        print("\nLessons completed:", len(lessons_read), "/", len(modules))

        total_correct = 0
        total_questions = 0

        for i in range(len(modules)):
            total_correct += module_correct[i]
            total_questions += module_total[i]

        print("\nGAME PROGRESS")
        print("Correct answers:", total_correct)
        print("Total questions answered:", total_questions)

        print("\nMODULE SCORES")
        print(LINE)

        for i in range(len(modules)):

            print(modules[i][0])

            if module_total[i] == 0:
                print("No games played yet.")
            else:
                print("Score:", module_correct[i], "/", module_total[i])

        input("\nEnter to continue...")

    elif choice == "0":

        print("\nThank you for using!")
        print("Keep learning and keep coding!")
        break

    else:
        print("Invalid choice! Please try again.")
