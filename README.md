# Harmonic series filter


`hfilter.pd` is a filter to remove frequencies from the harmonic series.

There are four inlets from left to right

1. Audio signal
2. Frequency.  
3. Which partial to filter
4. Q Value - width of filter.

The test patch:


Takes in a signal from `sigmund~` then `mtof`.  And the starting harmonic to filter.

Then there are four more filters each filtering a harmonic 2 in the series above the last.

Finally it subtracts the inverted output of the filters from the original signal and sends audio output

