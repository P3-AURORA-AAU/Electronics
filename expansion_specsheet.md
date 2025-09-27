# expansion slot
## power
18v rail
12v rail
5v rail

## com
### custom 6-pin SPI
1. MOSI (master out slave in) [pin 27]
2. MISO (Master in slave out) [pin 29]
3. sck (clock) [pin 31]
4. ss (salve select (chip select)) [pin 33]
5. additional ss for additional slaves (optional) [pin 35]
6. ready line (or reset line) [pin 37]


this arch will allow for 2 expansions operating at once, with an optional third one that manufactores could choose to include

# Module interfacing
module must contain MCU with the at least 5 free GPIO lines for com via SPI
modules MCU and sensors are allowed to use 5v rail
module electronics (such as motors) must use 12 or 18v rail. If module uses more than 18v, use internal voltage regulation, and the 18v rail

it is recommended to reserve GPIO pin 0 & 1 for internal UART com, and reserve pin 2-6 (optionally 7) for SPI com


