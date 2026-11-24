# Functions and Inputs

Functions and inputs help you **organise your code** and allow your scripts to work with different information.

---

## Functions

In the example below:

- I created a function called `hello_world` and used `echo` to display `Hello World!`.
- I then created another function called `greet_person` and used `local` to create a variable called `name`, assigning it the first argument passed to the function (`$1`).
- I then used `echo` to output `Hello`, followed by the value stored in the `name` variable.

Running `greet_person "Taimur"` will display: Hello, Taimur!

<img width="2686" height="506" alt="image" src="https://github.com/user-attachments/assets/729d1e4c-841a-414d-86f0-f52432efa5d6" />



## Parameters

Parameters allow us to **pass data to functions** so they can perform specific tasks based on the inputs provided.

In the example below, I created a function called `print_names` and used these special parameters:

| Parameter | Meaning |
|---|---|
| `$#` | The number (count) of arguments |
| `$0` | The name of the script |
| `$1` | The first argument |
| `$2` | The second argument |
| `$@` | All of the arguments |

I then called the `print_names` to call the script

<img width="2748" height="564" alt="image" src="https://github.com/user-attachments/assets/d79cca24-c1d3-4796-aef7-e5e32e6b9bc2" />





As you can see, the output shows:

- The number of names
- The script name
- The first and second names
- All of the names

<!-- IMAGE 4: terminal output for the Parameters example -->
> 📷 **Paste image 4 here (the Parameters terminal output)**

---

## User Inputs

User inputs allow the script to **interact with users**, making it more dynamic and responsive.

In the example below:

- I created a function called `greet_user`.
- I used the `read` command to capture the user's input and store it in the variable `name`.

<!-- IMAGE 5: screenshot of greet_user script and terminal side by side -->
> 📷 **Paste image 5 here (the User Inputs script and terminal)**

In the terminal on the right, I ran the script and it displayed `What is your name?`. I entered my name, and it then displayed: "Hello, Taimur!"

<img width="2654" height="480" alt="image" src="https://github.com/user-attachments/assets/e3891550-76a1-4e2b-badc-ac0d18b215eb" />
