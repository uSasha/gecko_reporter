################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include emusb/subdir.mk
-include emlib/subdir.mk
-include Drivers/subdir.mk
-include CMSIS/efm32hg/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: gecko_reporter.axf

# Tool invocations
gecko_reporter.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m0plus -mthumb -T "gecko_reporter.ld" -Xlinker --gc-sections -Xlinker -Map="gecko_reporter.map" --specs=nano.specs -o gecko_reporter.axf "./src/descriptors.o" "./src/main.o" "./src/scrolllcd.o" "./emusb/em_usbd.o" "./emusb/em_usbdch9.o" "./emusb/em_usbdep.o" "./emusb/em_usbdint.o" "./emusb/em_usbhal.o" "./emusb/em_usbtimer.o" "./emlib/em_assert.o" "./emlib/em_cmu.o" "./emlib/em_emu.o" "./emlib/em_gpio.o" "./emlib/em_int.o" "./emlib/em_prs.o" "./emlib/em_rtc.o" "./emlib/em_timer.o" "./emlib/em_usart.o" "./Drivers/display.o" "./Drivers/displayls013b7dh03.o" "./Drivers/displaypalemlib.o" "./Drivers/hidkbd.o" "./Drivers/udelay.o" "./CMSIS/efm32hg/startup_gcc_efm32hg.o" "./CMSIS/efm32hg/system_efm32hg.o" -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: gecko_reporter.hex'
	arm-none-eabi-objcopy -O ihex "gecko_reporter.axf" "gecko_reporter.hex"
	@echo ' '

	@echo 'Building bin file: gecko_reporter.bin'
	arm-none-eabi-objcopy -O binary "gecko_reporter.axf" "gecko_reporter.bin"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "gecko_reporter.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(C_DEPS)$(EXECUTABLES) gecko_reporter.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
