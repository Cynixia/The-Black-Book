# DESN2000 - Lab 6
## The Liquid Crystal Display
>[!Example] How much SRAM memory is built into the LPC2478?

96 kilobytes

>[!Example] How much memory is required to store the pixel data for a single LCD frame?

$(240\times320)\times16=1,228,800$ bits $=153.6$ kilobytes

>[!Example] Could this fit inside the LPC2478?

No.

>[!Example] Can you suggest a reason why we choose to give one extra bit of resolution to the green channel, rather than the red and blue channels?

The human eye is more sensitive to green than either red or blue.

## Drawing a pixel on the LCD display
>[!Example] What is *LCD_FRAME_BUFFER* in this function? Explain the logic behind the pointer arithmetic used on *LCD_FRAME_BUFFER*.

*LCD_FRAME_BUFFER* is the address pointing to the data of the first pixel in the LCD frame buffer.

ARM processors are byte-addressable and so adjacent bytes differ by 1 in their addresses. As each pixel is controlled by 16 bits or 2 bytes, adjacent pixels in memory differ by 2 in their addresses.

The address for any one pixel at $x,y$ will thus be the base address of the frame buffer, *LCD_FRAME_BUFFER*, plus $2\times x$, since pixels are updated along each row, then plus $240\times2\times y$, since each row is preceded by $y$ rows of 240 pixels.

## Setting up SPI on the LPC2478
>[!Example] When communicating over SPI, why is it good practice to disable the CS_TP immediately after a transmission has been completed?

By disabling any devices not in use over SPI any problems caused by unwanted data or clock signal transmission, such as slave-to-slave transmission, is avoided.

>[!Example] Treating the reserved bits as zeroes, write down what value should be written to the *S0SPCR* register for the following SPI interface configuration in hexadecimal.
>- Act as the master
>- Send 9 bits per transfer
>- Transfer data with the most significant bit first
>- Do not generate interrupts
>- Sample on the first edge of the SPI clock, which is taken as active low

0x093C

>[!Example] Calculate the required value of *S0SPCCR* to run the SPI bus at 2 MHz.

0x24

## Communicating with the TSC2046
>[!Example] For the following MISO data requirements, what bits must be written to the control byte?
>- 8-bit resolution
>- Differential reference mode
>- Power down between conversions

To read the x-coordinate:

| Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 | Control Byte |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:------------:|
|   1   |   1   |   0   |   1   |   1   |   0   |   0   |   0   | 0xD8             |

To read the y-coordinate:

| Bit 7 | Bit 6 | Bit 5 | Bit 4 | Bit 3 | Bit 2 | Bit 1 | Bit 0 | Control Byte |
|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|:------------:|
|  1 |   0   |   0   |   1   |   1   |   0   |   0   |   0   | 0x98             |


