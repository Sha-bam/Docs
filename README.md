# Sha-bam!

**Problem statement**:
As civil unrest grows in the US there inevitably be more shootings and one issue that dispatchers will have to face is figure out the what kind of the weapon(s) the instigator is using.

**Solution**:
Build a CNN to classify what kind of arm(s) is being discharged given down-sampled audio clip of the bang!

## Convolutional Neural Network Primer

Check out this [link](https://www.kaggle.com/fizzbuzz/beginner-s-guide-to-audio-data) for a good introduction to audio processing with CNN

### **Potential CNN Architecture**

![alt text](images/architecture.jpg)

\***\*notes**:

- We can replace dense layers with sparse using **SET** pruning.
