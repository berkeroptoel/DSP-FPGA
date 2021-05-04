## LUT based Waveform generation
This is the simplest way of waveform generating. Any type of signal e.g.,sine,cosine,square,triangular... can be saved in a memory block.   


Which parameters specify the frquency of sine wave?  
-Sample period raw data  
-DAC sampling frequency  

In this example; Sine wave period is 100 sample. DAC sampling frequency is 1MHz. This means the time between every sample is 1us. 
1us x 100 sample = 100us. As a result waveform frequency is 10kHz at the output.     




   
*Exercises*
1) Generate same wave using ***BRAM memory block*** instead of Distributed memory. Think about the differences.  
2) Generate a 1kHz wave using the ***same COE file***. 
3) What is the maximum frequency limit of analog signal at the output?
4) 
