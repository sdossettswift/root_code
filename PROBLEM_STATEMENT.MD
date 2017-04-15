For the next step of the interview process, we'd like to have you write a little bit of code. We've tried to keep the problem statement minimal so that it shouldn't take too much time.

If you have any questions please send me an email at dan@joinroot.com. If the problem statement doesn't specify something, you can make any decision that you want. Your code *will not* be evaluated on its ability to handle anything that wasn't mentioned in the problem statement. You do not need to persist any data to disk.

Please include a short README with your submission describing your approach to solving the problem. We're looking for a solution that is representative of code that you would write on a real project, including tests. You can complete this at your convenience — there isn't a specific deadline for it.

Email your code to us as a tarball (`tar zcvf your-code.tgz your-code-dir`) or a gitbundle (`GIT_DIR=your-code-dir/.git git bundle create your-code.gitbundle --all`)

## Problem Statement

Let's write some code to track driving history for people.

The code will process an input file. You can either choose to accept the input via stdin (e.g. `cat input.txt | ruby yourcode.rb`), or as a file name given on the command line (e.g. `ruby yourcode.rb input.txt`).

Each line in the input file will start with a command. There are two possible commands.

The first command is Driver, which will register a new Driver in the app. Example:

`Driver Dan`

The second command is Trip, which will record a trip attributed to a driver. The line will be space delimited with the following fields: the command (Trip), driver name, start time, stop time, miles driven. Times will be given in the format of hours:minutes. We'll use a 24-hour clock and will assume that drivers never drive past midnight (the start time will always be before the end time). Example:

`Trip Dan 07:15 07:45 17.3`

Discard any trips that average a speed of less than 5 mph or greater than 100 mph.

Generate a report containing each driver with total miles driven and average speed. Sort the output by most miles driven to least. Round miles and miles per hour to the nearest integer.

Example input:

```
Driver Dan
Driver Alex
Driver Bob
Trip Dan 07:15 07:45 17.3
Trip Dan 06:12 06:32 12.9
Trip Alex 12:01 13:16 42.0
```

Expected output:

```
Alex: 42 miles @ 34 mph
Dan: 30 miles @ 36 mph
Bob: 0 miles
```
