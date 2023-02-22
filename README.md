# SimpleLinuxShell
### 示意圖
![image](https://user-images.githubusercontent.com/75492436/220569716-55abfab1-b586-4ffb-8dcf-6924388e7f4a.png)

### Fucntion
- int main();
set Boolean and decide which function to enter
- void run();
check the inputline if there have pipes run connectpipe, else run _run
with argument nopipe
- void separate(char *commands);
seperate the inputline into each string and store in command
- void prompt();
write the initial line
- void interact();
run prompt() and run()
- void connectpipe();
check the amount of pipe and separate it to three kind of argument and
run _run
- void _run(pipekind kind);
throw the pipekind and command to execute, after execute replace the co
mmand to next command
- void redirect();
check which sign it is and run the correspond function
- void redirect_in(size_t index);
redirect in
- void redirect_out(size_t index);
redirect out
- void redirect_err(size_t index);
redirect error
- void execute(char **command, pipekind kind);
use two pipe to get previous output and pass to current input and run
execvp after using pipe close it to end the process
- void erase(char **command);
free
- bool eof(int c);
end
