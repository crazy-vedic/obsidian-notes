A signal that has discrete values, non continuous values.
Levels: Information in a digital signal can be represented in the form of voltage levels.
No. of bits required = Log2(Levels)
![[Pasted image 20230816111510.png]]

Any signals past lvl 4, or below lvl1, are considered 4 and 1 respectly
Q assume we need to download 100 pages/s, what is the required bit rate?
	page=24 lines, 80 charachters, 8 bits for one char
	thus bit rate = `100*24*80*8` = 1.636 mbps

Q what is the bit rate for HD TV:
	1920/1080 pixels, screen renewed 30/s, 24 bits per pixel
	bit rate = `1920*1080*30*24` = 1.5 gbps

Baud rate is the rate at which changes to the signal occur per second when it is tramissted through a medium, the higher the baud rate, the faster the data is transmitted
Baud rate = Number of signal elements/time

Problems with digital signal Impairments
[[Attenuation]]
[[Distortion]]
[[Noise]]