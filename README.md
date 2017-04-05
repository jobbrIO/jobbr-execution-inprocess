# jobbr-execution-inmemory [![Build status](https://ci.appveyor.com/api/projects/status/akvsehv0wvwbo08a?svg=true)](https://ci.appveyor.com/project/Jobbr/jobbr-execution-inmemory)
Components to execute Jobs within same process

## Idea
Let Jobs run withing the current process where also the JobbrServer runs, so that no additional processes are required.

## Challenges
* Don't crash the process --> AppDomains
* How to identify written files/artefacts at job completion --> ?
* How to handle process updates (24%, 99%, etc.) --> Is Console available / Multiple Jobs?, IProgressUpdate interface?
* How can log-files be separated into different files? --> Add JobRUnId to LogContext? (How is that mapped?)

## Knowhow
* Static Instances are per AppDomain only
* Threads can be named
* ThreadLocal could also help?

