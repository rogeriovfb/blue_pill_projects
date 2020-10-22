################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
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
flash_read_write.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
flash_read_write.list \

OBJCOPY_BIN += \
flash_read_write.bin \


# All Target
all: flash_read_write.elf secondary-outputs

# Tool invocations
flash_read_write.elf: $(OBJS) $(USER_OBJS) C:\Users\Rogerio\ Ballestrin\STM32CubeIDE\workspace_1.3.0\flash_read_write\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "flash_read_write.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\Rogerio Ballestrin\STM32CubeIDE\workspace_1.3.0\flash_read_write\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="flash_read_write.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

flash_read_write.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "flash_read_write.list"
	@echo 'Finished building: $@'
	@echo ' '

flash_read_write.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "flash_read_write.bin"
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
