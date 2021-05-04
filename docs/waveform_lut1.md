## LUT based Waveform generation
This is the simplest way of waveform generating. Any type of signal e.g.,sine,cosine,square,triangular... can be saved in a memory block.   


Which parameters specify the frquency of sine wave?  
-Sample period raw data  
-DAC sampling frequency  

In this example; Sine wave period is 100 sample. DAC sampling frequency is 1MHz. This means the time between every sample is 1us. 
1us x 100 sample = 100us. As a result waveform frequency is 10kHz at the output.       
*Exercises*      
1) Generate the same waveform(100kHz) given in the example using ***BRAM memory block*** instead of Distributed memory.  
2) Generate a 1kHz wave using the ***same COE file*** in the example.   
3) What is the maximum frequency limit of analog signal at the output?  
4) Generate the same waveform(100kHz) given in the example using symmetry property(quarter/half) of sine wave. Think over LUT memory utilization.  
5) Learn about Linear-feedback shift register(LFSR) structure. Add LFSR output signal with the sine signal given in the example. Output the signal from D/A.   
6) Acquire the signal with oscilloscope and measure THD, SFDR, SINAD, ENOB parameters of it. Which extra devices need for measuring listed parameters?  
7) Why the size distributed memory must be multiple of 2?  
8) Generate a ramp signal from D/A output. Load 0-255 digital numbers to DAC. Acquire the signal with oscilloscope. Measure the linarity.  
