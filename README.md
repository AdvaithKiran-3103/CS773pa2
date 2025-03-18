# **Implementing LLC partitioning on Champsim**
## **1A:2-way partitioning**
### **Approach**
The dualcore out-of-order processor being used on Champsim has 16 LLC ways.
8 LLC ways are assigned to each core by modifying the update and replacement policies such that no cross-core conflicts occur in the LLC.
In the code pa2/replacement/base_replacement.cc,
the functions lru_victim_llc() and lru_update_llc() are used to implement way partitioning.
### **Observations**
#### **1) Normalized IPC**
#### **2) LLC MPKI comparision**
#### **3) LLC SEPKI comparision**

## **2A:Static set partitioning**
### **Approach**
There are 4096 LLC sets in the dualcore out-of-order processor used in Champsim.

### **Observations**
#### **1) Normalized IPC**
#### **2) LLC MPKI comparision**
#### **3) LLC SEPKI comparision**
