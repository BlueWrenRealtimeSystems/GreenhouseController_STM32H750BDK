# GreenhouseController_STM32H750BDK
 Example controller, uses ITCM/DTCM, Ethernet, SDRAM, RTC

This project has been posted to assist developers with TouchGFX process control projects.  It is incomplete, however it will run on the above board.

The project provides:

- TouchGFX GUI
- Ethernet with SNTP and ICMP
- The real time clock set by the ethernet time
- ADC's in circular DMA mode with union data structures to ease debugging
- PWM Timer to drive a H-Bridge with enable inputs
- Uses ITCM and DTCM memory for stack, bas heap and selected functions
- CubeIDE is set up with SWV and FreeRTOS aware debugging with task counters and stack monitoring
- Debug Console using SVW ITM outputs
- Timer driven control task using task notify (bot semaphores)
- Modified interrupt service routine files to avoid call to HAL interrupt handling for time critical interrupts
- A file called osPriorities.h to consolidate operating system interrupt and task pririties.
- A version control module version.c and version.h which are forced to compile each build using prebuild:
  C:ST\STM32CubeIDE_1.15.0\STM32CubeIDE\plugins\com.st.stm32cube.ide.mcu.externaltools.make.win32_2.1.300.202402091052\tools\bin\busybox.exe touch version.c

 - Set memory to Close Coupled Memory (CCM) to manage CCM memory allocation
 - Custom circulary buffers FIFO for data logging and ehternet data transfer management (not yet implmented)

 -  
