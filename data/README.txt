# Dataset Description

This dataset provides a summary of the worker-weighted access by different census geography levels and travel times for the state. The worker-weighted access here represents the number of jobs a person can reach at 8am from a specific census area within a given travel time threshold. The travel time threshold are in integer seconds, at intervals from 300 (5 min) to 3600 (1 hour).

Census levels included in this dataset are:

	1. Block
	2. Block Group
	3. Census Tract
	4. County
	5. State

Each of these census levels corresponds to three different types of modes: auto, bike, and transit. The data for each census level is presented in a separate tab in the Excel file, except for the 'Block' level data, which is contained in separate csv files for each mode due to its large size.

## Data Files

[state].xlsx: This file contains data for the Block Group, Census Tract, County, and State census levels. The data for each level is presented in a separate tab.  
[state]_[statecode]_[mode]_block_[year].csv: These files contain the Block level data by mode.  

### Important Note

Due to its large size, the 'Block' level data file should not be opened outside of a person's coding platform. Attempting to open this file in Excel or a similar spreadsheet program would cut off a significant amount of data points.

## Data Fields

	1. mode: the type of travel modes, one of auto; bike; or transit)
	2. year: NAE data year, the year for which this dataset is relevant
	3. parent_area: the ID of the containing geography within which the data averages are calculated
	4. summary_level: the level of geography at which averages are calculated; one of state, county, census tract, block group, or block
	5. geoid: the ID of the particular census geography for which the data averages are calculated 
	3. threshold: the travel time threshold in seconds, ranging from 300 to 3600 seconds
	4. weighted_average: the average number of jobs a person can reach from a given census area within the travel time threshold for a specific mode
