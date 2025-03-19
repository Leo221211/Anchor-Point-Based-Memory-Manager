# Anchor-Point-Based-Memory-Manager
A memory management system based on dynamic hash table and anchor point array

## Description

The Memory Manager is originally the course project for CSCI2100 Data Structures.  
In the this project, I: 
1. Designed and implemented a memory management system using dynamic hash tables to optimize the allocation
and deallocation of computer memory.
1. Developed memory allocation algorithms with low amortized time complexity for address-based requests.
1. Designed a new data structure called anchor point array to achieve low time complexity for locating memory blocks
containing specific addresses.

To run the Memory Manager, see `Run Code` section. The implementation details are discussed in `project_report.pdf`.

## Run Code

1. Modify the total size of the memory by editing the final field maxSize in class MemMap in MemMap.java. The default size is set to 4GB

1. Set the field isDebugging in class Debug to true/false to turn on/off the debug mode. If debug mode turned on, the structure of memMap, 2 hash tables and the anchor point array will be printed out.

1. The code uses class BigInteger to store the address since the address might overflow. So the speed might be slower than those code implemented by class Integer. However in terms of big-O notation, the efficiency should be the same. Also, turning on the debug mode will make the execution time longer.

1. to compile and run the code, input the following commands
   
    ```
    cd Java/csci2100/
    javac HashTable.java MemoryOperation.java MemoryManager.java Debug.java MemMap.java Test.java

    cd ..
    java -ea csci2100.Test
    ```


## File Organizations
1. The memory map (implemented in linked list) and the hash table aided by anchor points is the main data structure of my algorithm.
The code for memory map is in file `MemMap.java`
The code for hash table is in `HashTable.java`

1. Other program files include:
   1. `Debug.java`: storing debugging functions.
   2. `MemoryManager.java`: the interface to perform memory managing operations. The detailed algorithm for managing request and release is inside.
   3. `MemoryOperation.java`: given file. Managing and translating different kinds of memory operations
   4. `Test.java`: given file. To perform tests on the memory manager.

1. Data and output files:
   1. `Data/` contains the test cases in .csv files.
   2. `Out/` contains the output of executing test cases with debug mode on and the total memory size set to 1024 bytes.