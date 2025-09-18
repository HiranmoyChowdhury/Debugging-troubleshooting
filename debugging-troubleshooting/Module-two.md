# Slowness

Creating too many applications makes the computer slow. Kill a process could help. But, is there any other solutions?

could be the following reasons:
- runs out of CPU time
- reading data from disk
- i/o through network
- moving data from disk to ram
- or other resource limiting performance
- hardware?

## cmds
top / iotop / iftop

## speed of accessing

- if the data is a variable, it is in cpu. retrieving the data is faster
- data is in another executing function, data is in ram
- from file, data is in disk. which is slow
- reading from network is much slower

if the data is reading from memory and we need to use this every time, we can store this in disk or cache

### look how ram works
:D you already know this from OS course. it freed the memory when this is out of the space. locate the data from ram to disk
swapping memory takes a lot of time dude...

## possible problems:
- too many open applications : close some of them
- if RAM is not enough, add extra ram to the computer
- one of program may have memory leak: if the program restart makes everything seems good, it may have memory leak

----

## possible causes

- try to figure out the problem
- if it is slow while starting up, probably too many application configured to start on boot. Disable some of them who aren't really needed.
- if computer become sluggish after running for days and problem solves after a reboot, this means it stores some state that's causing computer slow. change the program code or schedule a mitigate restart or try to rotate the program using some tool to reduce memory usage
- It could be user specific issue also. if it is read write issue. make the file local
- hard drive failure. if hard drive has error, computer can still use error corrections. but affect overall performance. Use OS utilities to diagnose problems on hard drive or ram
- malicious software.


## slow web server

- to check how slow a web server is to use ab(apache benchmark tool). ex. `ab -n <num of req> www.example.com`
- if it is, check where it is busy. If it is not busy with the priority task, set priority to each process. it will be execute according priority.
-- cmd: `nice/renice`
- look for how non prior processes are generated and what they are doing by `ps ax` and try to find an solution.

## monitoring tool linux

- to monitor cpu or disk i/o there are some monitoring tool need to use. can find on internet.
- SAR (System Activity Reporter) is especially useful for analyzing performance trends and identifying recurring issues over time
- the USE Method suggests creating a resource list and a `Functional Block Diagram`. This helps avoid data overload and provides a clear visualization of the system's components and their interactions.
- autogrouping optimizes desktop performance during CPU-intensive workloads by grouping processes and ensuring fair CPU cycle distribution.

## effiecient Code

- clear code
- make it faster if it is not fast enough
- Profiler is a tool which measures the resources that our code is using.
- gprofile to analyse c program. how many times a func is  called and how much time each of them took
- we can analyze the cost of code and how expensive it is

- using right data structure
- expensive loop
- keeping local result

## slow scripts problem

measure a binary spent time to run a process:

```bash
$ time <process name and args>
real time
user time
sys time
```
real : total time to execute the program
user : time spent doing operations on user space
sys : system time

real time = sys time + user time + some other process time

there are bunch of Profiler tool for golang. check those out [here](https://go.dev/blog/pprof)
there are some graphical interface too that to function to function call and time to execute each function

## parallelizing operation
- you know go-routine

# slowly growing in complexity

- make changes in solutions