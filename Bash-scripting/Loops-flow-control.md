# Loops and Flow Control

Loops allow you to repeat a set of commands multiple times. **Flow control** determines how a script runs, including when to repeat commands, make decisions, or stop.

---

## while Loops

`while` loops allow you to repeatedly execute a block of code as long as a certain condition stays true. The code keeps running until the condition becomes false.

For a `while` loop, the code is written between `do` and `done`.

### Example: Counting to 5

In this example, I created a variable called `count` and assigned it the value 1.

I then used `while` to repeat a set of commands as long as `count` was less than or equal to 5.

Inside the loop, I used `echo` to display the current value of `count`, followed by `((count++))`, which increased the value by 1 each time the loop ran.

<!-- Add screenshot here -->

The output shows that the loop repeats until `count` reaches 5. After displaying 5, `count` increases to 6, making the condition false and causing the loop to stop.

<img width="2566" height="374" alt="image" src="https://github.com/user-attachments/assets/bac0b3c3-5c98-456b-a070-e08d57f450f7" />


### Example: Looping Through an Array

In the example below, I created an array containing three items.

I then created a variable called `index` and assigned it the value 0. This is used to track the current position in the array.

The `while` loop repeats as long as `index` is less than the number of items in the array.

`echo` displays the fruit at the current index, and `((index++))` increases the index by 1 each time the loop runs.

Once `index` reaches the number of items in the array, the condition becomes false and the loop stops.

<img width="2572" height="360" alt="image" src="https://github.com/user-attachments/assets/5b447aff-eaa6-4991-9b2b-563e811579e8" />


---

## for Loops

`for` loops enable you to repeat a block of code for a specified number of iterations.

For a `for` loop, the code is written between `do` and `done`.

In the example below, I created a `for` loop that uses the `seq` command to generate numbers from 1 to 7. Each number is stored in the variable `number` as the loop runs.

<img width="2716" height="428" alt="image" src="https://github.com/user-attachments/assets/f24436c5-116a-41b4-8a01-407ec39eb483" />


---

## break and continue

These statements provide additional control within `for` and `while` loops. They allow you to interrupt or skip iterations based on specific conditions.

### break

The `break` statement immediately exits the innermost loop it is placed in, regardless of the loop's condition.

In the example below, I created a `for` loop:

- `i=1` creates the variable `i` and assigns it the value 1.
- `i<=5` means the loop continues as long as `i` is less than or equal to 5.
- `i++` increases the variable's value by 1 each time the loop runs.

`if [ $i -eq 3 ]` checks whether the variable's value is equal to 3. If the condition is true, the `break` statement stops the loop immediately.

<img width="2650" height="402" alt="image" src="https://github.com/user-attachments/assets/3651b286-bab1-41e6-b1cf-879bf539bc27" />


The output displays `Number: 1` and `Number: 2`, but nothing from 3 onwards, because the `break` statement ends the loop.

### continue

The `continue` statement skips the current iteration and moves on to the next iteration of the loop.

In the example below, I replaced the `break` statement with the `continue` statement. This skips the iteration when the variable's value is equal to 3.

<!-- Add screenshot here -->

The output therefore displays:

```
Number: 1
Number: 2
Number: 4
Number: 5
```

and skips `Number: 3`.


<img width="2652" height="386" alt="image" src="https://github.com/user-attachments/assets/86e253e0-9ef7-4fb4-8c8d-afddc8755e7d" />













- `i=1` creates the variable `i` and assigns it the value 1.
- `i<=5` means the
