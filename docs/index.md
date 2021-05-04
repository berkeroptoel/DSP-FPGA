## Basic DSP applications on FPGA

[editor on GitHub](https://github.com/berkeroptoel/DSP-FPGA/edit/main/docs/index.md) 

All applications are implemented in ZYBO board. A custom board which has **TLV5627** and **AD7928** is connected to ZYBO.       
`TLV5627` Sampling Frequency 1Msps / SPI clock frequency: 20MHz / 8bit / 4 channel       
`AD7928`  Sampling Frequency 1Msps / SPI clock frequency: 20MHz / 12bit / 8 channel  

![board](board.jpg)





```markdown
# A/D applications

```

```
function [x, y, z] = cordic_rotation_kernel(x, y, z, inpLUT, n)
% Perform CORDIC rotation kernel algorithm for N iterations.
xtmp = x;
ytmp = y;
for idx = 1:n
    if z < 0
        z(:) = accumpos(z, inpLUT(idx));
        x(:) = accumpos(x, ytmp);
        y(:) = accumneg(y, xtmp);
    else
        z(:) = accumneg(z, inpLUT(idx));
        x(:) = accumneg(x, ytmp);
        y(:) = accumpos(y, xtmp);
    end
    xtmp = bitsra(x, idx); % bit-shift-right for multiply by 2^(-idx)
    ytmp = bitsra(y, idx); % bit-shift-right for multiply by 2^(-idx)
end
```



### D/A applications Links
[Sinewave generator LUT](https://www.google.com)    
[Sinewave generator LUT - 4 channel](https://www.google.com)    
[Sinewave generator DDS IP Core](https://www.google.com)  
[Sinewave generator CORDIC](https://www.google.com)  
[Sinewave generator DDS VHDL](https://www.google.com)  
[Convolution/Cross Correlation](https://www.google.com)   
[QAM modulation VHDL](https://www.google.com)    
[Summing 2 waveform](https://www.google.com)  
[Sinewave generator Taylor series expansion](https://www.google.com)  
[Sweep generator](https://www.google.com)  


### A/D applications Links
[A/D signal reading](https://www.google.com)    
[A/D signal reading - 8 channel](https://www.google.com)    
[FFT IP Core](https://www.google.com)  
[FIR-IIR filtering VHDL](https://www.google.com)  
[CIC filtering VHDL](https://www.google.com)  
[FFT VHDL](https://www.google.com)   
[ASK-FSK demodulation VHDL](https://www.google.com)    
[DFT VHDL](https://www.google.com)  
[DDC VHDL](https://www.google.com)  
[DUC VHDL](https://www.google.com)

