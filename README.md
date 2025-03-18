# **Implementing LLC partitioning on Champsim**
## **1A:2-way partitioning**
### **Approach**
The dualcore out-of-order processor being used on Champsim has 16 LLC ways.
8 LLC ways are assigned to each core by modifying the update and replacement policies such that no cross-core conflicts occur in the LLC.
In the code pa2/replacement/base_replacement.cc,
the functions lru_victim_llc() and lru_update_llc() are used to implement way partitioning.
### **Observations**
#### **1) Normalized IPC**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/IPC%20way%20partitioning.jpg?raw=true)
#### **2) LLC MPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/MPKI%20way%20partition.jpg?raw=true)
#### **3) LLC SEPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/SEPKI%20way%20partitioning.jpg?raw=true)
## **2A:Static set partitioning**
### **Approach**
There are 4096 LLC sets in the dualcore out-of-order processor used in Champsim.Here we modified get_set function and gave cpu as parameter.based on cpu number it will calculate offset and seperates set for 2 cpus

### **Observations**
#### **1) Normalized IPC**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/IPC%20static%20set%20partitioning.jpg?raw=true)
#### **2) LLC MPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/MPKI%20static%20set%20parttioning.jpg?raw=true)
#### **3) LLC SEPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/SEPKI%20static%20set%20partitioning.jpg?raw=true)
## **2B:Dynamic set partitioning**
### **Approach**
There are 4096 LLC sets in the dualcore out-of-order processor used in Champsim.Here we are observing total access count and after a fixed number of accesses,we are checking the core misses of each cpu and based on the ratio we are allocating sets to that cpu
### **Observations**
#### **1) Normalized IPC**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/IPC%20dynamic%20set%20partitioning.jpg?raw=true)
#### **2) LLC MPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/MPKI%20dynamic%20set%20parttioning.jpg?raw=true)
#### **3) LLC SEPKI comparision**
![](https://github.com/AdvaithKiran-3103/CS773pa2/blob/main/SEPKI%20dynamic%20set%20partitioning.jpg?raw=true)
