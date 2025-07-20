## debugging vs troubleshooting

debugging: is solving the code issue
troubleshooting: is related to the system

## problem solving steps

1. need to find every information I can
- how and when the problem appears. we can search questing or docs for this.
2. need to analyze the root cause
3. performing the necessary remediation
4. document what we do
5. if not solved, start from the 1st step again :D

## strace

this is a tool to know all the system calls a specific program make.
"strace -o <file_to_store_sys_calls> <program_name> -- to list a brief of those commands

## itrace

to look at library calls

## Understanding the problem
1. if it doesn't work get enough information as what he was doing
2. what steps did he took
3. what was the expected result
4. what he actually got

try to give and immediate solution for work. 

## Reproduction Case
If that problem is missing directory then create the program without that directory with the same version and same environment that program faced issue.

1. Reads the log available to me (on linux read sys log)
2. if no error message or err msg is not helpful(internal system error) then try to isolate it
3. analyse the problem and try to fix it with same environment
4. don't hesitate to ask the user about the problem and related information

## Finding the Root Cause

For long term remediation needs creativity and the exact problem we are having.
come up with the possibilities, if it is not then try different possibilities until we find that explains the problem.
searching online with error message or looking the documentation after testing with the same environment the issue occurs.

### iotop 
which processes taking most input and output
### vmtop
virtual memory operations
### ionice
allow backup system to reduce access the disk
### iftop
current traffic to the network interfaces
### rsync
often used to backing up the data
### trickle
limit the bandwidth to use
### nice cmd
reducing the priority of a program to access the cpu

## intermittent issue

- need to find when the issue happens and when not
### heisenbug
where just observing a phenomenon alters the phenomenon

this occurs randomly. such as restarts the program solves the issue. need a long term remediation.
This could happens due to bad memory allocation or poor resource management


## binary search or bisection

if there are several files causing issue, we need to find the faulty file.
Bisecting those could be a solution. if there are 6 files, take three and run the program, if it is fine, then the problem is with other three.

there are `git bisect` command which allows us to bisection search on commit history to find out the bad commit which creates the issue.
