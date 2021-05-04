## Basic DSP applications on FPGA

[editor on GitHub](https://github.com/berkeroptoel/DSP-FPGA/edit/main/docs/index.md) 

All applications are implemented in ZYBO board. A custom board which has **TLV5627** and **AD7928** is connected to ZYBO.       
`TLV5627` Sampling Frequency 1Msps / SPI clock frequency: 20MHz / 8bit / 4 channel       
`AD7928`  Sampling Frequency 1Msps / SPI clock frequency: 20MHz / 12bit / 8 channel  

![board](board.jpg)
[Sinewave generator LUT](https://www.google.com)  

```markdown
# D/A applications
[Sinewave generator LUT](https://www.google.com)
[Sinewave generator LUT - 4 channel](https://www.google.com)
Sinewave generator DDS IP Core
Sinewave generator CORDIC
Sinewave generator DDS VHDL
Convolution/Cross Correlation  
QAM modulation VHDL  
Summing 2 waveform  
Sinewave generator Taylor series expansion
Sweep generator  
```


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

