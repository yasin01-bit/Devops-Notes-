# Error Handling & Exit Codes

---

## Error Handling

In Bash Scripting, error handling is detecting, managing and responding to errors when a script runs, rather than letting them go unnoticed.

In the example below, I used arithmetic expansion to to divide the number 10 by the number 0. This shows an error in the output as 10 cannot be divided by 0 as this is a mathematical error.

<img width="2712" height="386" alt="image" src="https://github.com/user-attachments/assets/2a378e35-7314-4fc3-8e51-02e88a0c866d" />


To handle this error, I used an `if` statement which shows that if num2 is equal to 0, then output "Error: Division by zero is not allowed". This prints a clear error message to the terminal so the user understands why the calculation cannot continue.

This is useful in error handling because it provides feedback instead of leaving the user wondering what went wrong.

I also used an exit code, `exit 1`, which terminates the script immediately and indicates that an error has occurred. Without this, the script could continue executing and potentially fail when it attempts to divide by zero.

<img width="2712" height="510" alt="image" src="https://github.com/user-attachments/assets/e6fa7192-d09c-439d-a3a5-7e0d73593e8a" />


---

## Exit Codes

Exit codes are a numerical value which are returned to the system when a command or script ends.

An exit code of `0` represents success. Any non 0 exit code represents an error.

In the example below, I used the command `command -v` to check whether the `git` command is available on the system. `2>/dev/null` redirects error messages to /dev/null, preventing them from being displayed in the terminal.

`$?` is the exit status of the the last executed command.

`if [[ $? -ne 0 ]]` shows, that if the exit status of the last executed command is not equal to 0 then the terminal will output, "git is not installed. Please install git.". This is followed by `exit 1` to immediately terimante the script.

I then used the `else` statement to display "git is installed" if `if [[ $? -ne 0 ]]` was not true.

<img width="2758" height="428" alt="image" src="https://github.com/user-attachments/assets/36be9231-ae5f-42de-b183-0fcc2582413a" />


---

## Set -e

`set -e` is a way of handling errors by telling the script to exit when a command fails. This is useful because it will prevent the script from carrying on when something has gone wrong.

In the example below, the output shows "Before the script" and then an error. This is because we used `set -e` so the script will not carry on for a command which does not exist. In this case, "After the script" will not be displayed because the system does not recognise the command `nonexistentcommand`.

<img width="2716" height="358" alt="image" src="https://github.com/user-attachments/assets/50dc168c-6c8c-4ff7-ab54-2e04ed609ed9" />


---

## Set -u

`set -u` forces the script to stop if it encounters an unset variable.

It helps prevent scenarios where missing data could lead to unexpected results.

In the example below, the output shows an error. This is because I used `set -u` which forced the script to stop because `X` is an undefined variable.

<img width="2732" height="238" alt="image" src="https://github.com/user-attachments/assets/a8e5434c-fb59-4e83-91d5-e224ffc77df4" />


In another example, we see the same result because `W` is an undefined variable.

<img width="2704" height="342" alt="image" src="https://github.com/user-attachments/assets/66b51fca-d58c-477e-8857-f1b5bc54cd49" />



---

## set -x

`set -x` prints each command that will be executed to the terminal before it is executed. This is helpful to follow the flow of a script.

In the example below I used arithmetic expansion. In the terminal on the right, the commands have been printed. The value of Z is also printed.

<img width="2712" height="428" alt="image" src="https://github.com/user-attachments/assets/6be9b61a-6bc7-4d6a-b2f3-3d8e1ca89221" />


---

## Set -eux

This allows you to combine all the `set` commands listed above and use them together. This will stop the script if there is error because of `e`, an unset variable because of `u` and will print the commands in the terminal because of `x`.

In the below example, the terminal prints each command before executing. It does not proceed with an unset variable and stops at a command that doesn't exist.

<img width="2670" height="416" alt="image" src="https://github.com/user-attachments/assets/dda5a6cd-65e8-4b29-864d-bde4322146de" />


---

## More Set Commands

- `set -o nounset` which can be used in the same way as `set -u`.
- `set -o errexit` which can be used in the same way as `set -e`.
- `set -o pipefail` helps detect when a command fails inside a pipeline. In the example below, the `cat` command fails because of the file not existing, therefore causing the whole pipeline to fail so the `grep` command will not even run.

<img width="2716" height="350" alt="image" src="https://github.com/user-attachments/assets/03b376f7-c893-40a5-9842-f4c79537d16f" />
