# API_WordChecker-Public_tests
This repository is related to a mandatory project for the degree "Computer science and engineering" at Politecnico di Milano.

## Details
Course: Algoritmi e principi dell'informatica - API

AY: 2021-2022

Project title: Word checker

## Alternative download link
https://polimi365-my.sharepoint.com/:u:/g/personal/10730627_polimi_it/ETlFMtwbiABAhagIIFR4v5QB7DLZN5fqYpZoXtfgR4WAsQ

Due to quota limitations set by GitHub, it's possibile that large files stored on LFS will become unavailable. I've uploaded the whole repo on OneDrive, students from polimi can access the .zip file using their Microsoft account.

## Repo purpose
This repo contains input files generated using the _input_gen.py_ script provided by the professor and, for each input file, the corresponding output returned by my script.
I hope these files help the students who need to troubleshoot their solution.

## Useful commands
### Flags for gcc to avoid stupid mistakes
```
gcc -Werror -Wall -Wmaybe-uninitialized -Wuninitialized -pedantic 
```
### To use valgrind memory checker
```
gcc -Werror -Wall -Wmaybe-uninitialized -Wuninitialized -pedantic -g3 file.c
valgrind --leak-check=full --track-origins=yes --show-leak-kinds=all ./a.out < /path/to/input/file > output.txt
```

### To use kcachegrind
```
gcc -Werror -Wall -Wmaybe-uninitialized -Wuninitialized -pedantic -g3 file.c
valgrind --tool=callgrind ./a.out < /path/to/input/file > output.txt
kcachegrind callgrind.out.XXXXX
```

### To use the address sanitizer
```
gcc -Werror -Wall -Wmaybe-uninitialized -Wuninitialized -pedantic -g3 -fsanitize=address -lasan file.c
./a.out < /path/to/input/file > output.txt
```

## Disclaimer
Although my solution successfully passed each test available in the valutation software, I cannot gurantee that the code is bug-free.

In order to avoid copyright issues, the script _input_gen.py_ is not uploaded here; students with their credentials can download the file through the website of the valutation software.
