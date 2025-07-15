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
