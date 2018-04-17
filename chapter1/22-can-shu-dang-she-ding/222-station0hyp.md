

STATION0.HYPlists parameters used in the location program HYP. There are many important parameters here to modify, including parameters for the

* coda magnitude calculation,

* station locations,

* velocity model and

* network code.  

Coda duration magnitude parameters TEST\(7\), TEST\(8\) and TEST\(9\):

These parameters are the duration magnitude coefficients used for calculating the coda magnitude, as

MAG = TEST\(7\) +TEST\(8\) \* LOG\(T\) + TEST\(9\) \* DELTA where

T is the coda length in seconds,  
 DELTA is the hypocentral distance in km.

The default SEISAN values for the coda magnitude parameters are those determined by Richter for Northern California.

Default values: 7: 0.087, 8: 2.0,  
 9: 0.0035 \(Lee, 1972\)

So default MAG = 0.087 +2.0 \* LOG\(T\) + 0.0035 \* DELTA

Values for these parameters are often different at volcanoes. Here, we use the coda magnitude parameters determined for Mt. St. Helens, or  
 RESET TEST\(07\)=-2.46  
 RESET TEST\(08\)=2.82

RESET TEST\(09\)=0.00

See the section below on Mc for more information.  
See the document “Processing Seismic Data” for more information on determining Mc parameters for your volcano.

Routine processing in Seisan for BPPTK; event location

Station locations:  
 Follow the format of the examples in STATION0.HYP for station location.  
 Velocity structure:  
 The velocity structure is given as shown in this example, from the example file below:

This velocity structure is used at Mt. St. Helens. Use this, or your own velocity structure, following this format. The letter ‘N’ indicates the moho.

S/P velocity ratio

S/P velocity radio in the example below is given by the value 1.74 in the line:

33.0 1000.3300. 1.74 15 1.0 00.5

4. 6 5. 10 6.0 6.2 6.6 6.8 7.1 7.8

0. 0 2. 2 3. 4 6. 0

10. 0  
 18. 0  
 34. 0 N 43. 0

16

Use this value or your own. Network code:

In the example below, CC is the network code used when a location is reported in the event’s s-file. Replace it with your own 2-digit network code.



```
RSET TEST(02)=500.0
RESET TEST(07)=-3.0
RESET TEST(08)=2.6
RESET TEST(09)=0.001
RESET TEST(11)=99.0
RESET TEST(13)=5.0
RESET TEST(34)=1.5
RESET TEST(35)=2.5
RESET TEST(36)=0.0
RESET TEST(41)=20000.0
RESET TEST(43)=5.0
RESET TEST(51)=3.6
RESET TEST(50)=1.0
RESET TEST(56)= 1.0
RESET TEST(58)= 99990.0
RESET TEST(40)=0.0
RESET TEST(60)=0.0
RESET TEST(71)=1.0
RESET TEST(75)=1.0
RESET TEST(76)=0.910
RESET TEST(77)=0.00087
RESET TEST(78)=-1.67
RESET TEST(79)=1.0
RESET TEST(80)=3.0
RESET TEST(81)=1.0
RESET TEST(82)=1.0
RESET TEST(83)=1.0
RESET TEST(88)=1.0
RESET TEST(85)=0.1
RESET TEST(91)=0.1
```

```
  YM012322.72N12245.19E   9
  YN032756.73N123 6.22E  20
  YM0624 7.77N12556.76E 131
```

```
  3.79       1.0
  4.41       2.0
  4.88       3.0
  5.34       5.0
  5.66       7.0
  5.99       9.0
  6.34      17.0
  6.90      36.0
  7.80      80.0      B

15.0 1100.2200. 1.78
```



