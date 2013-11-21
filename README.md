grapherator
===========

This generates a set of data points that simulate a semi-realistic usage pattern that can trend upwards or downwards or not trend at all

In order to generate a semi-realistic looking graph behavior we use a sine function to generate periodic behavior(ups and downs).  
In order to avoid a graph that is too regular, we introduce randomness at two levels:
The delta between steps across the x-axis is random, but within a range(deltavariance). 
The wavelength of the sine function is varied by randomly incrementing the index we pass to the sine function(sine_index)
