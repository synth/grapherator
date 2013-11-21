grapherator
===========

This generates a set of data points that simulate a semi-realistic usage pattern that can trend upwards or downwards or not trend at all

In order to generate a semi-realistic looking graph behavior we use a sine function to generate periodic behavior(ups and downs).  
In order to avoid a graph that is too regular, we introduce randomness at two levels:

1. The delta between steps across the x-axis is random, but within a range(deltavariance). 
2. The wavelength of the sine function is varied by randomly incrementing the index we pass to the sine function(sine_index)


Usage
=====

num_data_points = 100
grapherator = Grapherator.new(num_data_points, {})
grapherator.generate! # => returns [] of 0..num_data_points of psuedo-random numbers that follow a sinusoidal function

# output string that can be entered into the Google charts playground
# here: https://code.google.com/apis/ajax/playground/?type=visualization#line_chart
grapherator.google_charts_code 

