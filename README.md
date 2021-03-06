# Bash-scripts
Collection of Bash scripts.

<h1>About Bash</h1>

* Scripting languages originated as extensions of command interpreters in operating systems.
* Bourne shell (sh) was the first significant shell. Bash, today's most used Unix shell, is a GNU/FSF enhancement on the Bourne shell.
* Other shells include: C shell (csh), TC shell (tcsh), Dash (dash), Korn shell (ksh), Z shell (zsh).

<h1> What's the purpose of shell scripts? </h1>

* When working on programming projects or doing administrative tasks on servers, usually several command sequences are regularly repeated. This is especially true when working with files and directories, processing text, or doing network configurations. Numerous times, those command sequences exist in many forms and must be adjusted with user input, necessitating the usage of scripts.
* Scripting languages such as Bash improve our processes by including variables, if statements, loops, arrays, and functions, allowing for more sophisticated program flow.
* The actual power of shell script comes from all of the accessible Unix commands.
* Eventually, scripts get too complicated for basic languages such as Bash. At this stage, you should consider utilizing more powerful programming languages, such as Python.
* Shell scripts may also be used to "glue" together more complex Python scripts.

<h1> When should you not use Bash? </h1>

* Complex applications.
* GUI.
* Cross-platform portability.
* Calculations.
* Anything complex.

<h1>Hello world </h1>

```bash
#!/bin/bash
echo "Hello world"
```

<h1>Executing script </h1>

Open the terminal in the directory containing your script.

```bash
chmod u+x filename.sh
./filename.sh
```

<h1>Variables </h1>
  
* Assign the value <i>var="Test"</i>.
* Retrive the value <i>$x</i> or <i>${x}</i>.
* Variables can be defined explicitly as int or array:

```bash
declare -i var      # var is an int
declare -a arr      # arr in an array
declare -r var2=5   # var2 is read only
```

* Variables can store the value of executed command:

```bash
var=$(whoami)
```

<h1>Command line arguments </h1>

* First argument: <i>$1</i>
* All command line arguments as array: <i>$@</i>
* Number of command line arguments: <i>$#</i>
* The exit status of the last executed command: <i>$?</i>

<h1>If statements </h1>

Comparison of strings and ints differs. Assume that all values are strings, unless proven otherwise.

```bash
if [ $i -eq 10 ]; then        # int comparison
if [ "$name" == "10" ]; then  # string comparison
```

<h1>For loop </h1>

A for loop repeats a sequence of steps a number of times.

```bash
for number in {1..10}
do
  echo "$number "
done
```

<h1>Pipes </h1>

The pipe is used to pass the output of one command as input to the next:

```bash
ps -x | grep chromium
```

<h1>Redirect </h1>

But what if you'd want to save the results to a file? Bash has a redirect operator > that may be used to control where the output is delivered.

```bash
cmd >out.log             # Redirect stdout to out.log
cmd 2>err.log            # Redirect stderr to file err.log
cmd 2>&1                 # Redirect stderr to stdout
cmd 1>/dev/null 2>&1     # Silence both stdout and stderr
```

<h1>Formatting</h1>
<a href="https://github.com/lovesegfault/beautysh">Beautysh</a> is a great way to keep your formatting consistent.

```bash
beautysh **/*.sh
```

<h1>Intro</h1>

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Description</th>
            <th>Code</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Hello world in Bash.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/hello_world.sh">Bash</a></td>
        </tr>
        <tr>
            <td>2</td>
            <td>Check if condition is true using if statements.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/conditionals.sh">Bash</a></td>
        </tr>
        <tr>
            <td>3</td>
            <td>Example with while loop.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/while_loop.sh">Bash</a></td>
        </tr>
        <tr>
            <td>4</td>
            <td>Example with for loop.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/for_loop.sh">Bash</a></td>
        </tr>
    </tbody>
</table>

<h1>Math</h1>

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Description</th>
            <th>Code</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Airthmetic operations.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/arithmetic_operations.sh">Bash</a></td>
        </tr>
        <tr>
            <td>2</td>
            <td>Sum arguments passed to the script.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/sum_args.sh">Bash</a></td>
        </tr>
        <tr>
            <td>3</td>
            <td>Convert a number from decimal system to binary representation.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/decimal_binary.sh">Bash</a></td>
        </tr>
        <tr>
            <td>4</td>
            <td>Calculate the factorial of an integer.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/factorial.sh">Bash</a></td>
        </tr>
    </tbody>
</table>

<h1>Files</h1>

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Description</th>
            <th>Code</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Count files in a directory.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/count_files.sh">Bash</a></td>
        </tr>
        <tr>
            <td>2</td>
            <td>Create a directory.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/make_dir.sh">Bash</a></td>
        </tr>
        <tr>
            <td>3</td>
            <td>Count number of line in a given text file.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/line_counter.sh">Bash</a></td>
        </tr>
        <tr>
            <td>4</td>
            <td>Bundle together given files.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/bundle_files.sh">Bash</a></td>
        </tr>
        <tr>
            <td>5</td>
            <td>Get middle line.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/middle.sh">Bash</a></td>
        </tr>
    </tbody>
</table>

<h1>System administration</h1>

<table>
    <thead>
        <tr>
            <th>#</th>
            <th>Description</th>
            <th>Code</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Basic system check.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/system_check.sh">Bash</a></td>
        </tr>
        <tr>
            <td>2</td>
            <td>Make a system backup. Compress files and encrypt the archive.</td>
            <td><a href="https://github.com/djeada/Bash-scripts/blob/master/src/backup.sh">Bash</a></td>
       </tr>
    </tbody>
</table>
