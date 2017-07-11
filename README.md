# Algorithmic-Markov-Chain-Composition
> Algorithmic music composition using second-order Markov chains in Max/MSP.

This patch reads in a MIDI song file and produces an infinite stream of MIDI notes with random pitches, velocities, and durations at randomly changing tempos. After any given note, the next note is chosen at random from a list of possible \"transition\" notes, weighted by the probabilitiy of the previous pitch, velocity, and duration transitioning into the next pitch, velocity, and duration, respectively.

### Preview
![preview of patch](https://github.com/andrewdcampbell/Algorithmic-Markov-Chain-Composition/blob/master/preview.png)

### Notes 
* The transition probabilities are generated from the MIDI file given. As a result, you might hear traces of the original song in the output, especially if it's a simple song. 
* The generated music lacks structure because it's based on the simplifying Markov property that the probability distribution of the next note depends only on the current note. 
* Try different MIDI files (sample files are included) to hear the output! I find that the more complex songs tend to result in better sounding music. You can also try loading multiple MIDI files without reseting the STMs (state transition matrices) to hear a blend of multiple songs's influences.
