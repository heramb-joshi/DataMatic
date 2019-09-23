# DataMatic
Importing IGRA2 US Weather Balloon Data into readable format
One of my friend approached me with a problem that he is not able to get the data in the easily redable format.
He wanted to study US weather balloon data. 
This data is available at the following loacation..

https://www.ncdc.noaa.gov/data-access/weather-balloon-data

The dataset is constructed such that each station will have a dataset file with records dated as old as 1948 till around latest available years.
The readings invlove pressure, temperature and other weather attributes captured by the balloon at different heights and different point of time in a dat.
The station parameters are more or less constant with multiple readings at a point of time at different heights of the balloon.

So the dataset starts with a header record indicating station name, date and time of the observation, followed by readings at various height like the following.

#Station_name 1948 01 01 03 XXXXXX
1000  2000  X X X
2000  1000  X X X
3000  500   X X X

where first column of the data record is height, second column as pressure and so on.

We can't as it is import this data to any software as the column count of a flat file is varying based on whether it is a header record or a data record.

I found several libraries which help download the weather balloon data in readable format but I took this challenge to hone my data wrangling skills.

Thanks to stack overflow and Google, I could translate my algorithm into a working function.

The code is not memory optimized and takes a while to create the dataset but it seems a good start!
Hope anyone will benefit this!

Regards,

Heramb
