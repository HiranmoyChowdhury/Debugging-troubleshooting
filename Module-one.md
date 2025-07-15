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