MCU=atmega328p
F_CPU=12000000UL
CC=avr-gcc
OBJCOPY=avr-objcopy
CFLAGS=-Wall -Os -DF_CPU=$(F_CPU) -mmcu=$(MCU)

all: task_1_6_7_leds.hex

task_1_6_7_leds.elf: *.c
	$(CC) $(CFLAGS) -o $@ $<

task_1_6_7_leds.hex: task_1_6_7_leds.elf
	$(OBJCOPY) -O ihex -R .eeprom $< $@

flash: task_1_6_7_leds.hex
	sudo avrdude -p m328p -c gpio -e -U flash:w:task_1_6_7_leds.hex

clean:
	rm -f *.elf *.hex
