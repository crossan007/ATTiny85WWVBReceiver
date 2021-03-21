# References:
## Costas Loop - BPSK carrier-lock _AND_ demodulation
https://en.wikipedia.org/wiki/Costas_loop
https://www.southampton.ac.uk/~sqc/EZ412-612/RCL-6.pdf
https://www.youtube.com/watch?v=nBUs5V8adj4
https://www.tutorialspoint.com/digital_communication/digital_communication_phase_shift_keying.htm
GOOOD EXPLIATION: http://www.eng.auburn.edu/~troppel/courses/TIMS-manuals-r5/TIMS%20Experiment%20Manuals/Student_Text/Vol-A2/A2-16.pdf

## ATTiny Sine wave generation
https://forum.arduino.cc/index.php?topic=261129.0
https://www.avrfreaks.net/comment/1088196#comment-1088196
http://www.technoblogy.com/show?QVN
https://www.avrfreaks.net/forum/high-frequency-pll-clock-oh-really?name=PNphpBB2&file=viewtopic&t=45903

## ATTiny pinout:
https://www.componentsinfo.com/attiny85-pinout-features-datasheet/

## Low Pass filter tutorials
https://www.electronics-tutorials.ws/filter/filter_2.html


# Idea:
1) ATTiny85 PWM to implement the VCO portion of the Costas loop on PWM
2) ATTiny85 to parse demodulated BPSK time signals and output over I2C
3) Hardware implementation of Low Pass filter portion of Costas Loop


# Pinouts
*  Costas Loop SIN output PWM on pin 2 (PB3)
*  Costas Loop COS output PWM on pin 6 (PB1)
*  Costas Loop output to ADC input pin 1 (PB5)
*  I2C output on pin 7 (PB2/SCK) and ping 5(PB0/SDA)
*  Ground pin 4
*  VCC pin 8