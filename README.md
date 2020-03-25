# direct_mapped_cache_simulator

A.	About the Overall procedures
I made the direct mapped cache simulator and here are the steps how I made it. 
First, I read all the lines from input file. 
Second, I added the lists to save the 16bit addresses in the input file, converted into 32bit and saved them. 
Third, I split each of the 32bit addresses into the cache index and tag. 
Also, I converted the parts of the address bits, which are the cache indexes, to decimal number because the cache index on the block address is a binary form so it needed to be change to compare with index numbers in the direct mapped cache, which are forms of decimal. 
After, I started to make the frame of direct mapped cache. I used ‘DataFrame’ data structure from ‘pandas module’, because it is similar with the ideal frame of direct mapped cache that I learned from the lecture. The frame contains 128 indexes from 0 to 127, which is same as the number of the blocks, the space for valid bits and tags for each index. After adding columns and indexes, I set all the valid bits to 0. The reason why is that initiating of the cache simulator, the valid bits are all set by 0.

To write the results, I made the list named ‘output’ to save the results in each address and variables to add how many hits and misses are risen. 
After, I made the codes for the simulation of a cache. The procedures are: 
1.	Put the index number which are made from input address.
2.	Compare the index number.
3.	If the index number is same for both input address and cache index on the cache, there are the result of hit and miss.
4.	Hit occurs when the value of a cache valid bit is ‘1’ and the tag of the cache is same as from the input address.
5.	Miss occurs in two conditions. First, it occurs when the value of a cache valid bit is ‘1’ and the tags are discorded each other. Also, when a value of the cache valid bit is ‘0’, (not ‘1’) it occurs.
6.	If the case 1 occurs, the tag has to be updated into the recent one and if the case 2 occurs, the valid bit has to be changed by ‘1’, and tag of the cache has to be updated to that of the input address.

At last, I made the output file which is named after the input file, it prints out each results of the input address whether it hit or missed. 
After that, I added the result of the total counts of hit and misses.

If you guys have any feedbacks, pls let me know.
All feedbacks are welcome!