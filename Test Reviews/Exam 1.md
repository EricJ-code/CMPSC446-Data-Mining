# Review
## Formulas To Know
-  Min-Max Normalization:
	- 𝑣𝑖` = ((𝑣𝑖 ― 𝑚𝑖𝑛𝐴)/𝑚𝑎𝑥𝐴 ― 𝑚𝑖𝑛𝐴))(𝑛𝑒𝑤𝑚𝑎𝑥𝐴 ― 𝑛𝑒𝑤𝑚𝑖𝑛𝐴) + 𝑛𝑒𝑤𝑚𝑖𝑛𝐴
- Z-Score Normalization:
	- 𝑣𝑖` = (𝑣𝑖 ― Ā)/𝜎𝐴
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
#### Min-Max Normalization
