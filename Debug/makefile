################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32L0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
BlinkLED.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
BlinkLED.list \

OBJCOPY_BIN += \
BlinkLED.bin \


# All Target
all: BlinkLED.elf secondary-outputs

# Tool invocations
BlinkLED.elf: $(OBJS) $(USER_OBJS) /home/rk42/STM32CubeIDE/workspace_1.2.0/BlinkLED/STM32L072CZYX_FLASH.ld
	arm-none-eabi-gcc -o "BlinkLED.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"/home/rk42/STM32CubeIDE/workspace_1.2.0/BlinkLED/STM32L072CZYX_FLASH.ld" --specs=nosys.specs -Wl,-Map="BlinkLED.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

BlinkLED.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "BlinkLED.list"
	@echo 'Finished building: $@'
	@echo ' '

BlinkLED.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "BlinkLED.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
