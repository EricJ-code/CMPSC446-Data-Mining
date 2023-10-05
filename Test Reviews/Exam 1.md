# Review
## Formulas To Know
-  Min-Max Normalization:
	- 𝑣<sub>𝑖</sub>\` = ((𝑣<sub>𝑖</sub> ― 𝑚𝑖𝑛<sub>𝐴</sub>)/𝑚𝑎𝑥<sub>𝐴</sub> ― 𝑚𝑖𝑛<sub>𝐴</sub>))(𝑛𝑒𝑤𝑚𝑎𝑥<sub>𝐴</sub> ― 𝑛𝑒𝑤𝑚𝑖𝑛<sub>𝐴</sub>) + 𝑛𝑒𝑤𝑚𝑖𝑛<sub>𝐴</sub>
- Z-Score Normalization:
	- 𝑣<sub>𝑖</sub>\`  = (𝑣<sub>𝑖</sub> ― Ā)/𝜎<sub>𝐴</sub>
- [Standard Deviation (POPULATION)](https://youtu.be/Uk98hiMQgN0?si=MPj1DD11Kq1QWHVV&t=279)
	 ![[Pasted image 20231004214025.png]]
	 Technically X bar should be mu
	
## Data Preprocessing

### Binning Process
- Equal-Frequency Partitioning
	- Definition:
		Evenly distributing the data across the bins.
	- Example:
		Given the dataset of {1, 1, 1, 1, 3, 4, 5, 6, 6, 7, 9, 9} and a **Bin Depth of 3**
		Your results should look like this:
		- Bin 1: {1, 1, 1} 
		- Bin 2: {1, 3, 4}  
		- Bin 3: {5, 6, 6}  
		- Bin 4: {7, 9, 9} 
### Smoothing Processes
#### Smoothing by Bin Means
- Explanation:
	Take the mean of the bin and replace all values with that mean
- Example:
	Given the dataset of {1, 1, 1, 1, 3, 4, 5, 6, 6, 7, 9, 9} and a **Bin Depth of 3**
	Your results should look like this:
	- Bin 1: {1, 1, 1} --> AVG = 1 -----> **New Bin 1: {1, 1, 1}**
	- Bin 2: {1, 3, 4} --> AVG = 2.67 --> **New Bin 2: {2.67, 2.67, 2.67}**
	- Bin 3: {5, 6, 6} --> AVG = 5 .67--> **New Bin 3: {5.67, 5.67, 5.67}**
	- Bin 4: {7, 9, 9} --> AVG = 8.33 --> **New Bin 4: {8.33, 8.33, 8.33}**
#### Smoothing by Bin Boundaries
- Explanation:
	Determine the difference between the current value and the bin's min & max. Make the current value the min or max, depending on which ever is closest.
- Example:
	Given the dataset of {1, 1, 1, 1, 3, 4, 5, 6, 6, 7, 9, 9} and a **Bin Depth of 3**
	Your results should look like this:
	- Bin 1: {1, 1, 1} --> **New Bin 1: {1, 1, 1}**
	- Bin 2: {1, 3, 4} --> **New Bin 2: {1, 4, 4}** 
	- Bin 3: {5, 6, 6} --> **New Bin 3: {5, 6, 6}**
	- Bin 4: {7, 9, 9} --> **New Bin 4: {7, 9, 9}**
	*Note: Bin 2 is the only bin that changed as 3 is closer to 4 than it is to 1 thus changes to 4. the rest stayed the same due to repeat numbers.
- Example 2:
- Given the dataset of {1, 2, 4, 5, 9, 15, 16, 18, 21, 21, 22, 30} and a **Bin Depth of 4**
	Your results should look like this:
	- Bin 1: {1, 2, 4, 5} -------> **New Bin 1: {1, 1, 5, 5}**
	- Bin 2: {9, 15, 16, 18} ---> **New Bin 2: {9, 18, 18, 18}** 
	- Bin 3: {21, 21, 22, 30} --> **New Bin 3: {21, 21, 21, 30}**


### Normalization
Given the the data set {100, 200, 250, 400, 600}
#### Min-Max Normalization
- Min-Max Normalization EQ:
	- 𝑣<sub>𝑖</sub>\` = ((𝑣<sub>𝑖</sub> ― 𝑚𝑖𝑛<sub>𝐴</sub>)/𝑚𝑎𝑥<sub>𝐴</sub> ― 𝑚𝑖𝑛<sub>𝐴</sub>))(𝑛𝑒𝑤𝑚𝑎𝑥<sub>𝐴</sub> ― 𝑛𝑒𝑤𝑚𝑖𝑛<sub>𝐴</sub>) + 𝑛𝑒𝑤𝑚𝑖𝑛<sub>𝐴</sub>
- Normalization Process
	- Set normalization min = 0 and max = 1
	- Find the dataset's Min and Max
		- Min = 100
		- Max = 600
	- Using the equation above you should get these results:
		- 𝑣<sub>𝑖</sub>= 100 --> **𝑣<sub>𝑖</sub>\`**= ((100-100) / (600 -100))(1-0)+0 = **0**
		- 𝑣<sub>𝑖</sub>= 200 --> **𝑣<sub>𝑖</sub>\`**= ((200-100) / (600 -100))(1-0)+0 = **0.2**
		- 𝑣<sub>𝑖</sub>= 250 --> **𝑣<sub>𝑖</sub>\`**= ((250-100) / (600 -100))(1-0)+0 = **0.3**
		- 𝑣<sub>𝑖</sub>= 400 --> **𝑣<sub>𝑖</sub>\`**= ((400-100) / (600 -100))(1-0)+0 = **0.6**
		- 𝑣<sub>𝑖</sub> = 600 --> **𝑣<sub>𝑖</sub>\`**= ((600-100) / (600 -100))(1-0)+0 = **1**
#### Z-Score Normalization
- Z-Score Normalization EQ:
	- 𝑣<sub>𝑖</sub>\`  = (𝑣<sub>𝑖</sub> ― Ā)/𝜎<sub>𝐴</sub>
- Normalization Process
	- Set normalization min = 0 and max = 1
	- Find the dataset's Min and Max
		- Min = 100
		- Max = 600
	- Calculate the mean
		- mean = 310
	- Find the standard deviation
		- std = 174.35596
	- Using the equation above you should get these results:
		- 𝑣<sub>𝑖</sub>= 100 --> **𝑣<sub>𝑖</sub>\`**= (100-310) / 174.35596 = **-1.2044**
		- 𝑣<sub>𝑖</sub>= 200 --> **𝑣<sub>𝑖</sub>\`**= (200-310) / 174.35596  = **-0.6309**
		- 𝑣<sub>𝑖</sub>= 250 --> **𝑣<sub>𝑖</sub>\`**= (250-310) / 174.35596  = **-0.3441**
		- 𝑣<sub>𝑖</sub>= 400 --> **𝑣<sub>𝑖</sub>\`**= (400-310) / 174.35596  = **0.5162**
		- 𝑣<sub>𝑖</sub> = 600 --> **𝑣<sub>𝑖</sub>\`**= (600-310) / 174.35596  = **1.6633**
	- It is not necessary but you can use a z-table to look up the z-values related to your findings
### Clustering
#### "Simple" Way
#### Centroid Method




