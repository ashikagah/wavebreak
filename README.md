# Locating order-disorder phase transition in a cardiac system

The original paper is [here](https://arxiv.org/abs/1708.03990).


## How to cite

Please cite the following paper when you use the code in this repo:

Ashikaga H, Asgari-Targhi A. Locating order-disorder phase transition in a cardiac system. _arXiv preprint_ 1708.03990, 2017


## Dependencies

1. MATLAB - Tested in MATLAB version 2018a with OSX 10.13.2 High Sierra

2. Function `fk2d.m`, a MATLAB implementation of the Fenton-Karma model in two dimensions (2-D) from [Fenton-Karma repo](https://github.com/ashikagah/Fenton-Karma).

3. Java Information Dynamics Toolkit [JIDT](https://github.com/jlizier/jidt/wiki/Installation) > v1.3.1

## Installation

Clone the github repository.
```
$ git clone https://github.com/ashikagah/wavebreak
```


## Usage

1. Generate time series of spiral waves and information flow

In MATLAB command window, 

```
>> generate_data
```
It uses the function `rm_spirals.m` to create sequential stimulations according to the stimulation file `s4_stim.mat` to induce four spiral waves in a 2-D lattice. It saves the time series of the excitation variable (_ts_) in a file `orig60.mat` and its binarized time series in a file `bi60.mat`. It also creates and saves the time series of information flow [uo, vo] in a file `uvo60.mat`. The whole process takes several hours, depending on the system used.

2. Perform Eulerian analysis of information flow

In MATLAB command window, 

```
>> eulerian_analysis
```
It shows Shannon entropy, instantaneous information flow and total information flow over time, all in an Eulerian perspective.  

3. Perform Lagrangian analysis of information flow

In MATLAB command window, 

```
>> lagrangian_analysis
```
It shows the forward trajectory of information flow and the Lagrangian coherent structures in an Lagrangian perspective.

## Spatial domain
- Matrix size: 120 x 120
- Grid spacing: 0.99 mm
- Grid size: 11.9 x 11.9 cm

## Licence
MIT

## References
1. Lizier JT. JIDT: An information-theoretic toolkit for studying the dynamics of complex systems. _Frontiers in Robotics and AI_ 1:11, 2014 [html](https://journal.frontiersin.org/article/10.3389/frobt.2014.00011/full)
