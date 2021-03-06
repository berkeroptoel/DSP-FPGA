## Basic DSP applications on ZYBO FPGA Board

[editor on GitHub](https://github.com/berkeroptoel/DSP-FPGA/edit/main/docs/index.md) 


All applications are implemented in ZYBO board. A custom board which has **TLV5627** and **AD7928** is connected to ZYBO.  

|               | TLV5627(DAC)| AD7928(ADC) |
| -----------   | ----------- | ------------
| Sampling rate | 1 Msps      | 1 Msps      |
| SPI clock     | 20MHz       | 20MHz       |
| Resolution    | 8bit        | 12bit       |
| Channel       | 4           | 8           |

[TLV5627 datasheet](https://www.ti.com/product/TLV5627)  
[AD7928 datasheeet](https://www.analog.com/en/products/ad7928.html#)

![board](board.jpg)


```markdown
# D/A applications  
Waveform generator LUT based
Waveform generator LUT based 4 channel  
Waveform generator using DDS IP Core  
Waveform generator CORDIC VHDL     
Waveform generator DDS VHDL   
Convolution and Cross-Correlation VHDL   
QAM modulation VHDL  
Summing 2 waveform  
Waveform generator TAYLOR based  
Sweep waveform generator CORDIC based    
```


```markdown
# A/D applications
Signal reading    
Signal reading 8 channel  
Converting frequency domain using FFT IP Core  
FIR-IIR filtering VHDL  
CIC filtering VHDL  
DFT coding VHDL  
FFT coding VHDL        
ASK FSK Demodulation VHDL   
DDC down converter implementation VHDL  
DUC up converter implementation VHDL  
```



### D/A applications Links
[Sinewave generator LUT](waveform_lut1.md)    
[Sinewave generator LUT - 4 channel](waveform_lut4.md)    
[Sinewave generator DDS IP Core](waveform_dds_ip.md)  
[Sinewave generator CORDIC](waveform_cordic_vhdl)  
[Sinewave generator DDS VHDL](waveform_dds_vhdl)  
[Convolution/Cross Correlation](conv_cross_cor.md)   
[QAM modulation VHDL](qam_mod.md)    
[Summing 2 waveform](sum2.md)  
[Sinewave generator Taylor series expansion](waveform_taylor.md)  
[Sweep generator](waveform_sweep.md)  


### A/D applications Links
[A/D signal reading](https://www.google.com)    
[A/D signal reading - 8 channel](https://www.google.com)    
[FFT IP Core](https://www.google.com)  
[FIR-IIR filtering VHDL](https://www.google.com)  
[CIC filtering VHDL](https://www.google.com)  
[DFT VHDL](https://www.google.com)   
[FFT VHDL](https://www.google.com)   
[ASK-FSK demodulation VHDL](https://www.google.com)    
[DDC VHDL](https://www.google.com)  
[DUC VHDL](https://www.google.com)


### Contributers
Berker I??IK  
Birkan ??etinkaya  


