################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
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
donatello.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
donatello.list \

OBJCOPY_BIN += \
donatello.bin \


# All Target
all: donatello.elf secondary-outputs

# Tool invocations
donatello.elf: $(OBJS) $(USER_OBJS) C:\Users\Isak\Documents\GitHub\robotsm20-folkrace-donatello\software\STM32F031G6UX_FLASH.ld
	arm-none-eabi-gcc -o "donatello.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Users\Isak\Documents\GitHub\robotsm20-folkrace-donatello\software\STM32F031G6UX_FLASH.ld" --specs=nosys.specs -Wl,-Map="donatello.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

donatello.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "donatello.list"
	@echo 'Finished building: $@'
	@echo ' '

donatello.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "donatello.bin"
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
