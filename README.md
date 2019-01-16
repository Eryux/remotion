# remotion

**Blender add-on for motion capture analysis and animation re-build using LSTM RNN. (POC)**


### Introduction

Remotion is a POC that allow to fix frames of motion capture animation based on previous and next frame of animation and a learning process from similar movement. All is encapsuled in a Blender add-on for a user-friendly usage.


### Our method

1. First, we train a model on correct on clean motion capture movement using a LSTM-3LR network. 

2. We take a broken animmation with movement of same type as movement trained with our network and for each x frames of broken animation we trying to predict thank to our network and learning date, the next x frames of our animation.

3. Then we compare predicted frames with broken animations frames and if the result go over a tolerance value, we replace broken animation frames by our predicted frames.

4. We re-do step 2 and 3 a second time but this time we trying to predict previous x frames for each x frame.


### Demo

[![Video: Motion capture analysis and animation rebuild using LSTM RNN](https://img.youtube.com/vi/ifLWbranI4I/0.jpg)](https://www.youtube.com/watch?v=ifLWbranI4I)

Video: Motion capture analysis and animation rebuild using LSTM RNN


### Requirements

* Anaconda python 3 environnement
* Keras and Tenserflow *(Anaconda environnement)*
* Cuda 9.0 and cudNN *(required for hardware acceleration only)*
* Blender 2.7+


### License

GNU GPLv3