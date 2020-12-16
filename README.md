# Sha-bam!

**Problem statement**:
As civil unrest grows in the US there inevitably be more shootings and one issue that dispatchers will have to face is figure out the what kind of the weapon(s) the instigator is using.

**Solution**:
Build a CNN to classify what kind of arm(s) is being discharged given down-sampled audio clip of the bang!

## Convolutional Neural Network Primer

Check out this [link](https://www.kaggle.com/fizzbuzz/beginner-s-guide-to-audio-data) for a good introduction to audio processing with CNN

### **Potential CNN Architecture**

![alt text](images/architecture.jpg)

\*\*\*misc notes\*\*:

- We can replace dense layers with sparse using **SET** pruning.
- Since our data is going to be varied among different sources we're gonna need to do something about the input layer
- Also probably going to need to increase dropout rate
- Need to discuss how we're going to be classifying based on rounds (.556, .762. 9mm ,etc ) or by type of gun (Longrfile, handgun, Sniper, Bazooka <- this is a joke), or finally even down to the specific gun (Ak-varient, AR-15, etc.)
- Sure we want automatic feature extraction, however, we should transform our data from traditional spectrogram to something like a [MEL-spectrogram](https://towardsdatascience.com/getting-to-know-the-mel-spectrogram-31bca3e2d9d0?gi=67c12ee836b7)?

# How we're gonna do this

**Data Sourcing:**

[Gunshot Audio Forensice Dataset](https://www.google.com/search?q=gun+sound+data+set&oq=gun&aqs=chrome.1.69i57j69i59l3j0i67j69i61l2j69i60.5474j0j7&sourceid=chrome&ie=UTF-8)

[Research Google](https://research.google.com/audioset/dataset/gunshot_gunfire.html)

-> We will also be sampling audio data from youtube for validation. We will also need to apply some preprocessing to normalize the data.

In addition, to combat variability in sound quality, we're going to down sample everything to some threshold we need to figure out.

We're probably going to need to write up a few python scripts :

```
pre-process.py

a-script-for-labelling.py
```

Also for validation we're going to have to do a lot of manual labelling. This is going to be the shittiest phase, but really key for making sure that our model doesn't end up completely useless.
