# Variables and Parameters

## Variables

Variables allow you to **store and manipulate data**. They hold values that can be accessed and modified throughout the script.

In the example below, I created four variables: `greeting`, `count`, `fruits` and `name`.

> <img width="1876" height="490" alt="image" src="https://github.com/user-attachments/assets/184aa7e4-b685-4af5-b65f-ae44153018ea" />

- The `$` means "get the value stored in this variable".
- `echo "Hello" $name` displays the word `Hello` followed by the value stored in the `name` variable.

For example, if `name="Taimur"`, the output will be:

```
Hello Taimur
```

`$name` tells Bash to use the value stored in the `name` variable.

This is what the output looks like in the terminal:

> <img width="1776" height="272" alt="image" src="https://github.com/user-attachments/assets/6af82508-e86d-4ba3-939e-17aae96abc0a" />


---

## Parameters

Parameters are values that you give to a script **when you run it**. They allow the script to use different information without changing the script itself.

In this example I used three parameters:

| Parameter | Meaning |
|---|---|
| `$1` | The first argument passed to the script |
| `$2` | The second argument passed to the script |
| `$3` | The third argument passed to the script |
| `$@` | All of the arguments passed to the script |

> <img width="1932" height="358" alt="image" src="https://github.com/user-attachments/assets/94427536-c011-4f78-ba21-3b79701cbd49" />


This is how it was displayed when I ran the script in my terminal:

> <img width="1840" height="338" alt="image" src="https://github.com/user-attachments/assets/8a89151e-7781-4250-94e0-206efa5bf352" />


`hello`, `hi` and `hey` are the **arguments** passed to the script. Depending on their order, they correspond with the first, second or third parameter.




## Arithmetic Expansion

Arithmetic expansion in Bash allows you to perform maths calculations in a script.

In the example below:

1. I created two variables, `num1` and `num2`, and assigned them the values `3` and `15`.
2. I used arithmetic expansion `$(( ))` to add the two values together and store the answer in a variable called `result`.
3. I used `echo` to display the calculation in my terminal.

> <img width="1754" height="352" alt="image" src="https://github.com/user-attachments/assets/d51d7741-2942-417d-8f89-fd929b5d0645" />
<img width="1770" height="86" alt="image" src="https://github.com/user-attachments/assets/66207adb-5fbb-4659-9369-d4ff0379b0ab" />


### Rectangle Example

In the example below, I used arithmetic expansion to output the area and the perimeter of a rectangle.

> <img width="1722" height="466" alt="image" src="https://github.com/user-attachments/assets/1e087b38-5863-4708-bfe9-13fa234d5f89" />
<img width="1854" height="228" alt="image" src="https://github.com/user-attachments/assets/77b81d2d-d17c-4be0-9b1c-f593554e4ce6" />



> **Note:** I made a mistake with the perimeter. It should be:
>
> ```bash
> perimeter=$((2 * (length + width)))
> ```
>
> This should output `34` instead of `17`.

---

## Arithmetic Expansion (With Parameters)

Arithmetic expansion with parameters allows us to take input from the user, such as command arguments, and perform calculations based on those values.

In the example below, instead of using fixed values for the length and width, I used the arguments:

- `$1` for the length
- `$2` for the width
- When I ran the script followed by two numbers, Bash used these arguments as the length and width and calculated the area and perimeter.

> <img width="1680" height="386" alt="image" src="https://github.com/user-attachments/assets/959d1acf-6716-4504-b1a7-9cf3d5df479a" />
<img width="1548" height="118" alt="image" src="https://github.com/user-attachments/assets/b957d6dd-342f-4a1f-9914-ea1fb8bb7790" />


