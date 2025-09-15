# Multi-Interpreter 
theoritical part of my project since i didnt have a system with high range graphics card i didnt try that. concept of Multi-interpreter
types:
solo -> single interpreter work as a alone (single-core) will not divide and run them for lowest level complexity
duo -> two interpreter work as a team (dual-core) divides each tasks by 2 and run them for mid level complexity
squad -> four interpreter work as a team (quad-core) divides each tasks by 4 and run them for highest complexity

dividing as a group a part of program which starts from a line is defined as that part which is if a program stmt starts in odd part (1,3,5,7) a specific group of interpreters will work on that and in even part a specific group of interpreters will work 

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Virtual Garbage Collector (actual prototype) version 1.0 a garbage collector for python 
As a initial stage i have built a prototype VGC memory model which will runs in arduino uno (stage-1 proto-type) 
aims to use memory based on the object type which enables frequent access of an object and reduce memory fragmentation focus on increase in frequent usage of object (reusability) and with a few intergration of functions like JIT/AOT SIMD,WASM attaining maximum features along with performance if the device is capable to run CUDA the user can also intergrate that at VGC memory model  

#Working principles
the memory will be store in R,G,B //different types of memory locations 
based on the types of usage of the object and another is work complexity of the task which is categorised into three types 
criteria 1: (usage based)                                                                             priority:                       VGC Type
1. very rarely & not will be used objects -> Red Zone                                       |  1st priority -> Green zone     |
2. Frequently used every time or most of the time majority in usage objects -> Green Zone   |  2nd priority -> Blue zone      |    Active (permanent memory) // like rom 
3. rarely used not frequent but will be used minority level of usage objects -> Blue Zone   |  3rd priority -> Red zone       |

criteria 2: (time & memory complexity based)                                                        priority:   
1. highest complexity task objects -> Red Zone                                              |  1st priority -> Red Zone       |
2. mid complexity task objects -> Blue Zone                                                 |  2nd priority -> Blue zone      |   Passive (Temporary memory) // like ram 
3. lowest complexity task objects -> Green Zone                                             |  3rd priority -> Green zone     |

(usage based -> functionality like [Read Only Memory]) Active VGC 
(task complexity based -> functionality like [Random Access Memory]) Passive VGC 




