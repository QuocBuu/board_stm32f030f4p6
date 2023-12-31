/**
  @page RTC_Timer RTC Timer example
  
  @verbatim
  ******************** (C) COPYRIGHT 2014 STMicroelectronics *******************
  * @file    RTC/RTC_Timer/readme.txt 
  * @author  MCD Application Team
  * @version V1.6.0
  * @date    13-October-2021
  * @brief   Description of the RTC Timer example.
  ******************************************************************************
  * @attention
  *
  * Copyright (c) 2014 STMicroelectronics.
  * All rights reserved.
  *
  * This software is licensed under terms that can be found in the LICENSE file
  * in the root directory of this software component.
  * If no LICENSE file comes with this software, it is provided AS-IS.
  *
  ******************************************************************************
  @endverbatim

@par Example Description 

  This example provides a short description of how to use the RTC peripheral�s with 
  Alarm sub seconds feature to simulate a timer with refresh time equal to 250 ms
  (1 second/ 8) * 2).
  The RTC is configured to generate sub seconds interrupt each 125ms (will have
  8 interrupt per 1 second).
  
  For this example an interactive human interface is developed using
  STM320xx_EVAL�s LCD and Push Buttons to allow user to use Timer with a real 
  progress bar display.

  After startup, the timer is equal to 1 Minute (60 Seconds) and by pressing on
  the Tamper button the progress bar start to be filled for each 2 successive
  interrupts (after each 250ms).
  After 480 interrupts (60 * 8) the progress bar will be full.

  User can manipulate the chronometer features using the Tamper and Wakeup buttons:
    - press Sel button to Start the timer.
    - press Tamper button to stop the timer.

 
@par Directory contents 

  - RTC/RTC_Timer/system_stm32f0xx.c   STM32F0xx system clock configuration file
  - RTC/RTC_Timer/stm32f0xx_conf.h     Library Configuration file
  - RTC/RTC_Timer/stm32f0xx_it.c       Interrupt handlers
  - RTC/RTC_Timer/stm32f0xx_it.h       Header for stm32f0xx_it.c
  - RTC/RTC_Timer/main.c               Main program
  - RTC/RTC_Timer/main.h               Main header file

@note The "system_stm32f0xx.c" is generated by an automatic clock configuration 
      tool and can be easily customized to your own configuration. 
      To select different clock setup, use the "STM32F0xx_Clock_Configuration_V1.0.0.xls" 
      provided with the AN3988 package available on <a href="http://www.st.com/internet/mcu/family/141.jsp">  ST Microcontrollers </a>
 
       
@par Hardware and Software environment 

  - This example runs on STM32F0xx Devices.
  
  - This example has been tested with STMicroelectronics STM320518-EVAL and
    STM32072B-EVAL including respectively STM32F051R8T6 and STM32F072VBT6 devices
    and can be easily tailored to any other supported device and development board.

  - STM320518-EVAL Set-up
    - Use SEL push button. 
    - Use the TAMPER push button connected to PC.13 pin (EXTI Line13).
    
  - STM32072B-EVAL Set-up
    - Use SEL push button. 
    - Use the TAMPER push button connected to PC.13 pin (EXTI Line13).

       
@par How to use it ? 

In order to make the program work, you must do the following :
 - Copy all source files from this example folder to the template folder under
   Project\STM32F0xx_StdPeriph_Templates
 - Open your preferred toolchain 
 - If the used device is STM32F051R8T6 choose STM32F051 project
    - Add the following files to the project source list
       - Utilities\STM32_EVAL\STM320518_EVAL\stm320518_eval.c
       - Utilities\STM32_EVAL\STM320518_EVAL\stm320518_eval_lcd.c
       
 - If the used device is STM32F072VBT6 choose STM32F072 project
    - Add the following files to the project source list
       - Utilities\STM32_EVAL\STM32072B_EVAL\stm32072b_eval.c
       - Utilities\STM32_EVAL\STM32072B_EVAL\stm32072b_eval_lcd.c
 - Rebuild all files and load your image into target memory
 - Run the example
    
 */
