# change-python-version-colab

## This repo demonstrates how to change the python version on your colab notebook


* First you have to run this snippet from this [stackoverflow post](https://stackoverflow.com/questions/63168301/how-to-change-the-python-version-from-default-3-5-to-3-8-of-google-colab)
  > change the version as you like in both `!sudo apt-get install python3.7` and `!sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 1`
```python
#**Add python version you wish** to list
!sudo apt-get update -y
!sudo apt-get install python3.7
from IPython.display import clear_output 
clear_output()
!sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.7 1

# Choose one of the given alternatives:
!sudo update-alternatives --config python3

# This one used to work but now NOT(for me)!
# !sudo update-alternatives --config python

# Check the result
!python3 --version

# Attention: Install pip (... needed!)
!sudo apt install python3-pip

```
>> After you run this you have to choose the environment you wnat to run , choose whichever you like by simply typing

* You might need to run the following code too
  `!sudo apt-get install python3.7-distutils` 
