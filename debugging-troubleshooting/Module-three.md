## system that crash

there could be a lot of suspicious reasons. But, need to short the scope.

- need to try the easier and faster way to check first. Read the logs if any error pointing.
- try look at the behavior. suppose it works in some other machine then the problem is with the installation or config.
- if the issue is with ram test `memtest 86`. find the root cause man.
- test all the hardware one by one if needed. 

## understanding crashing application

- look at the logs and understand the crashing message with date-time and error message
- try online search
- if need more info try debug logging in cli
- to see inside the program and what the system doing - use debugging tool like `stace` in linux
- try analyze input, output, configuration

## what to do when I can't fix the problem

- see if the input is in write format as it can be for new version
- it can be for new service proxy. so, check if request and responses are well. user `wrapper` in this case.
- try check if that version problem. such as try changing os ;)
- `watchdog`: A process that checks whether a program is running and, when it's not starts the program again.

## internal server error

- look for server log at first
- logs in linux located at /var/log
- `ls -lt` will include last modified date file list
- look for syslog
- look for `sudo netstat -nlp | grep :<port no>`

## fix someone else's code

- read docs first
- reading code; try read comment; if comment is not there, try add comment while reading else's code
- try read test; will know the use cases
- try read the functions which cause the issue