# Virtual laboratory bench based on STM32F407 microcontroller

Working in Virtual environment with Virtual laboratory bench.

<details><summary>LAB 1</summary>
  
Set up the LEDs as follows:

If code N is set on the SW switches (see task option), animations should be displayed on the LED indicators LED1 ... LED8 according to the task option. In all other cases, the LED indicators reflect the value set on the SW switches.

The nBTN button of the processor module should pause the animation. One press pauses the animation, the next press the animation continues from the same point. When the animation is not displayed on the LEDs, pressing the button is ignored.

Processor module LED states during program operation:

![image](https://user-images.githubusercontent.com/42679553/172135490-b5c44a53-6b7d-42a2-bdc6-ffa6abfa80ce.png)

Green indicates the state when the corresponding LED is lit. Otherwise, it is not lit, that is, it is turned off.

The animation is displayed cyclically, that is, after the last frame of the animation is displayed, it starts over from the first frame. The display time of one frame is 0.5 s.

</details>

<details><summary>LAB 2</summary>
  
Animation should be displayed on the LED indicators LED1 ... LED8 according to the task variant.

The animation speed is set using the SW switches. If the code 0x0 is set on the switches, then the animation frames change every 500 ms. With an increase in the value set on the SW switches, the animation slows down by T ms. The value of T is given by the job option.

For example, if the variant specifies that T = 100 ms, this means that when the switches are set to SW = 0x1, frames start changing every 500+1*100= 600 ms, if SW = 0x5, then frames start changing every 500 +5*100 = 1000ms etc.

All delays must be implemented using interrupts from the basic timers TIM6 or TIM7.

![image](https://user-images.githubusercontent.com/42679553/172136248-40359ee5-a510-46d0-96e2-7bd63f8f4902.png)

Green indicates the state when the corresponding LED is lit. Otherwise, it is not lit, that is, it is turned off.

The animation is displayed cyclically, that is, after the last frame of the animation is displayed, it starts over from the first frame.
  
</details>

It consists of a green motherboard or carrier board, to which a processor module based on the STM32F407 microcontroller is connected. Also on the motherboard a keyboard, a display, a power button, a reset button, a line of switches are located. An expansion module is connected with an additional line of LEDs and switches. There are also two LEDs on the processor module: one is green, the other is two-color, which can glow either yellow or red. And a button that can be used as a trigger for some events. The processing of this button is carried out programmatically.

![image](https://user-images.githubusercontent.com/42679553/172133455-d671aab7-f42f-4690-b1ac-73fdd1cfbeb0.png)
