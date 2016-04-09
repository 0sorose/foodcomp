The following is in-depth information about how to connect the control board circuitry.

Before attempting this you should read through  the build log at foodcomputer.tumblr.com



	LIST OF CONNECTIONS
	
	Title			Type		Pin		Program Label (used in the code for the Mega)

Light Intensity 		I2C		I2C		SLIN and SLPA
water Ph			0-5V		A1		SWPH
water Temp			0-5V		A2		SWTM
water connectivity 		0-5V				SWEC
Chamber Air Temp		0-5V  		A0		SATM
Chamber Humidity		0-5V				SAHU
Chamber CO2  			5V UART		11(TX)/12(RX)	SACO and SATM, SAHU but I believe SACO is the only sensor active in the device
Shell Open			5V		4		SGSO
Window Open			5V		3		SGWO
Chamber Heater			AC (R)		6		AAHE
Chamber Humidifier		AC (R)		9		AAHU
Chamber Air Vent		12V (R)		14		AAVE
Chamber Air Circulation		12V (R)		15		AACR
Chamber LED Illumination	12V (R)		53		ALPN 
Motherboard LED Illumination	12V (R)		52		ALMI




	PIN LABLE DIAGRAM
	each column of 4 lines represents a seeed socket	

	      (FACE UP)
  <-TO USB  (ORIENTATION) END OF BOARD->

	1	2	3

1 1	GND	GND	AC L
  2	5V	5V	AC N
  3	12	17	AC L
  4	11	16	AC N

2 1	12V	12V	AC L
  2	GND	GND	AC N
  3	12V	12V	12V
  4	GND	GND	GND
		
3 1	GND	GND	GND
  2	5V	SCK	5V
  3	14	MOSI 51	53
  4	15	MISO 50	52
		
