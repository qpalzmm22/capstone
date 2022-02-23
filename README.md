# Capstone Project

## User must provide
1. **Fuzzing config**(`fuzz.yml`)
   - Time limit
   - num of parellel fuzzing
   - 
2. **Fuzzing Drivers**(`~Driver.c`)
   1. if it receive file, add `File` in front of `~Driver.c` => `~FileDriver.c`
3. **Seeds**(`~Driverseeds.zip`) (optional) 
4. **Script to compile Drivers**
   - Makefile => we can compile it with `CC=afl-cc`?
5. **Run script**

how to create run shell script? 
-> per Driver, create a process and use the according seed(if exist)

## Fuzzing results
1. **UI** (coverage info, Fuzzing status)
2. **Fuzzing status** is in 4 states
   - **Build Failing** : Failing in building the project, fuzzing etc
   - **Fuzzing** : Running fuzzing for given time
   - **Bug Found** : bug is found while fuzzing
   - **All Pass** : Bug is not found for given time
3. **Seeds** : Creates new seeds whenever there is a bug found.
   -  crash causing bug will be added as new sed 
4. **Bug report** : Creates new github issue Whenever bug is found
   - **Commit ID**
   - **Fuzzer 종류**
   - **Fuzzing 시간**
   - **Crash 종류** : (hang, segfault …)
   - **Crash causing input**
