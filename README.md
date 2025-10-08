

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Virtual Garbage Collector (actual prototype) version 1.0 a garbage collector for python 
As a initial stage i have built a prototype VGC memory model which will runs in arduino uno (stage-1 proto-type) 
aims to use memory based on the object type which enables frequent access of an object and reduce memory fragmentation focus on increase in frequent usage of object (reusability) and with a few intergration of functions like JIT/AOT SIMD,WASM attaining maximum features along with performance if the device is capable to run CUDA the user can also intergrate that at VGC memory model  

#Working principles //prototype
the memory will be store in R,G,B //different types of memory locations 
based on the types of usage of the object and another is work complexity of the task which is categorised into three types 
criteria 1: (usage based)                                                                             priority:                       
1. very rarely & not will be used objects -> Red Zone                                       |  1st priority -> Green zone     |
2. Frequently used every time or most of the time majority in usage objects -> Green Zone   |  2nd priority -> Blue zone      |    
3. rarely used not frequent but will be used minority level of usage objects -> Blue Zone   |  3rd priority -> Red zone       |

criteria 2: (time & memory complexity based)                                                        priority:   
1. highest complexity task objects -> Red Zone                                              |  1st priority -> Red Zone       |
2. mid complexity task objects -> Blue Zone                                                 |  2nd priority -> Blue zone      |  
3. lowest complexity task objects -> Green Zone                                             |  3rd priority -> Green zone     |

(usage based -> functionality is like [Read Only Memory]) Active VGC 
(task complexity based -> functionality is like [Random Access Memory]) Passive VGC 

Test case : (output) // test case result of simple intial stage proto-type:
First image = Zone Creation & initial allocation of memory to R, G, B zones
<img width="1600" height="315" alt="image" src="https://github.com/user-attachments/assets/d24ace35-9bf5-45d1-9e12-75336fe44274" />

Second image = workload classification & dynamic object storage simulation 
<img width="773" height="344" alt="Screenshot 2025-09-15 151542" src="https://github.com/user-attachments/assets/c11ba6f9-0bd0-4fe8-95d3-a9de83631216" />





