# Tuning the antenna

## Preparation
1. Have a Google spreadsheet or pen and paper ready. 
2. Assembled yagi antenna on a mast or low height tripod (as far away from ground but low enough to make length adjustments). 
3. Equipment below

## Procedure

### Equipment
1. RigExpert or NanoVNA
2. Multimeter
3. Tape measure
4. Spreadsheet or pen and paper (notepad)
5. Sharpie pen
   
### Measurements 

Adjusted tuning sequence (with length asymmetry in mind)
1.	Check mechanical assembly  
    1.1 Confirm rear-fed element is installed as indeed the longer one. (I label them with Brother P-Touch label printer. You can label them with Sharpie pen also.)  
	1.2 Confirm forward-fed element is the shorter one.  
2.	Resonance check individually  
    2.1 Start from Prototype element length measurements (See Table 1). The Prototype yagi has the similar materials used for elements and phasing harness and optimal performance measurements.  
	2.2 Rear-fed element (also acts as reflector) → should resonate slightly below the design frequency (~28.2 MHz if targeting 28.4).  
    2.3 For attaching the RigExpert to the feedpoint, use the shortest coax stub possible. Connect the RigExpert to the antenna feedpoint. Record the SWR measurements from RigExpert. Go back to 2 until lowest SWR obtained for desired frequency.  
	2.4 Forward-fed element → should resonate slightly above design frequency (~28.6 MHz if targeting 28.4).  
	2.5 Don’t force elements to be equal — the offsets are intentional in yagi antennas. (See Table 1 below)  
3.  Ensure electrical continuity in all elements, phasing harness (multimeter ohm meter). 
4.	Phasing harness connection  
	4.1 Verify coax lengths/phasing line are correct.  
	4.2 Choke at forward feedpoint, equal lead lengths.
5.	Antenna array measurement  
	5.1 Combined SWR dip should land close to design center (~28.4).  
	5.2 If dip is too low in frequency → trim the forward-fed element slightly.  
	5.2 If dip is too high → lengthen the rear-fed element slightly.  
6.	Pattern verification  
    6.1 Test the antenna with your radio. (Antenna is tuned for FT8 communications so fire up WSJT-X.) See also [Testing.md](Testing.md)  
	6.2 Rotate between forward azimuth and 180° opposite.  
	6.3 Front/Back >15 dB confirms the length asymmetry is correct.  
7. Mark point where the tip inserts into the next element to record last known placement with good SWR.

#### Practical tip

When trimming, always do it in small increments (0.25 inch at a time). Since only the tip sections are adjustable, you can sneak up on the proper offset. Notice that only the director length had to be increased, the other two elements were reduced in length. 


**Table 1.** Element lengths from Cebik and Prototype antennas. AF-C3-V1 (Bennett) is this modified Cebik antenna. All dimensions are in inches. The final dimensions for Yagi AF-C3-V1 are derived from incremental tuning in Table 2 below.

| Source	| Element	  | Dipole	| Half-dipole	| Proportions (* rear-fed reference) |
|-----------|-------------|---------|---------------|------------------------------------|
| Cebik	    | Rear-fed	  | 206	    | 103	        | 1.00 *                             |
| Cebik	    | Forward-fed | 194	    | 97	        | 0.94                               |
| Cebik	    | Director	  | 191	    | 95.5	        | 0.93                               |
| Prototype	| Rear-fed	  | 217	    | 108.5	        | 1.00 *                             |
| Prototype	| Forward-fed |	200.5	| 100.25	    | 0.92                               |
| Prototype	| Director	  | 190	    | 95	        | 0.88                               |
| AF-C3-V1	| Rear-fed	  | 214.5	| 107.25	    | 1.00 *                             |
| AF-C3-V1	| Forward-fed | 197.74	| 99.22	        | 0.92                               |
| AF-C3-V1	| Director	  | 191.07	| 95.54	        | 0.89                               |   


**Table 2.** Incremental tuning data for AF-C3-V1 - observing SWR with incremental changes in element lengths. All units are in inches, except for proportions and SWR. Legend: L = left, R = right, T = total, FF = forward-fed, RF = rear-fed, D = director, SWR = Standing Wave Ratio. Bracketed figures are the right element lengths.

| Rear-fed-T | Cebik RF delta | Forward-fed-T   | Cebik FF delta | Director-T | Cebik D delta | SWR-28097@2500 |
|------------|----------------|-----------------|----------------|------------|---------------|----------------|
| 214.88     | 8.88           | 198.24          | 4.24           | 191.07     | 0.07          | 1.47           |
| 213.06     | 7.06           | 198.24          | 4.24           | 191.07     | 0.07          | 1.42           |
| 214.5      | 8.5            | 198.24          | 4.24           | 191.07     | 0.07          | 1.43           |
| [214.5]    | 8.5            | [197.74]        | 3.74           | [191.07]   | 0.07          | [1.17]         |
| 214.5      | 8.5            | 198.43          | 4.43           | 191.07     | 0.07          | 1.43           |






