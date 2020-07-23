# Music Recommendation Calculator

The Calculator takes in one song and compares its features to a dataset of 300 other songs and outputs the 10 most similar songs. 

In my approach, I calculate certain features from the given audio signals and store them with in a Google Drive using the Python Pickle module.
In order to get better results, I use low and mid level features to give the songs a similarity score based on how far thier features are from the given song. The songs with the lowest similarity scores are the closest to the given song since their features have the least difference.

Features Used:

    Centroid
    Amplitude Variance
    Zero Crossing
    Spectral Flatness
    Tempo
I have written my own algorithims to calculate these features from the audio waveform using a fast fourier transform. 

By adjusting the weights for the given features, I was able to find certain weights that gave me appropriate results, although these results are subjective and might differ in opinion from person to person.

Using information from Audio Content Analysis by Alexander Lerch, I decided to use Temporal Characteristics (tempo) and Dynamic characteristics since the book states that classification with common characteristcs such as intensity have proved to give good results. I gave the most weight to Tempo and Zero Crossing rate and lesser weight to the centroid and amplitude variance.
