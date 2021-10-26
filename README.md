# Neural Symplectic Form

## Environments

- Python 3.6.9
- Pytorch 1.8.1
- Numpy 1.19.5
- Scipy 1.4.1

## Structure

Mass spring data, double pendulum data and Lotka-Volterra data should be prepared into the follow structure.:

```
code
│  
│  
├─double pendulum
│  │  HNN.ipynb
│  │  LNN.ipynb
│  │  Neural Symplectic Form.ipynb
│  │  NODE.ipynb
│  │  Skew Matrix Learning.ipynb
│  │  
│  └─data
│          A.csv
│          B.csv
│          double pendulum data.ipynb
│          input.csv
│          target.csv
│          
├─lotka-volterra
│  │  HNN.ipynb
│  │  Neural Symplectic Form.ipynb
│  │  NODE.ipynb
│  │  Skew Matrix Learning.ipynb
│  │  
│  └─data
│          A.csv
│          B.csv
│          input.csv
│          lotka-volterra data.ipynb
│          target.csv
│          
└─mass spring
    │  HNN.ipynb
    │  LNN.ipynb
    │  Neural Symplectic Form.ipynb
    │  NODE.ipynb
    │  Skew Matrix Learning.ipynb
    │  
    └─data
            A.csv
            B.csv
            input.csv
            mass spring data.ipynb
            target.csv
```

## Datasets

The dataset is illustrated below using double pendulum as an example.

For double pendulum data,  generate random data by ``double pendulum data.ipynb`` and write it to ``target.csv`` and ``input.csv`` as following:

```
1.15E-01	1.29E-02	-5.67E-02	-4.89E-02
1.22E-01	4.79E-03	-8.68E-02	-4.02E-02
1.19E-01	-1.52E-02	-1.07E-01	-1.96E-02
...
```

The four columns of target data represent the position and motion of double pendulum.

The matrix used for data pre-processing is saved in the ``A.csv``  and  ``B.csv``  which can be used to restore the data for the simulation.

## Target dynamics and Models

 The ``.ipynb`` files  under each experiment file contain the code for training models and simulation models. Although the experiments were performed in double precision in the paper, these codes are for single precision computation.

#### mass spring:

```
 HNN.ipynb  
 LNN.ipynb 
 Neural Symplectic Form.ipynb
 NODE.ipynb
 Skew Matrix Learning.ipynb
```

#### double pendulum:

```
 HNN.ipynb  
 LNN.ipynb 
 Neural Symplectic Form.ipynb
 NODE.ipynb
 Skew Matrix Learning.ipynb
```

#### Lotka-Volterra:

```
 HNN.ipynb
 Neural Symplectic Form.ipynb
 NODE.ipynb
 Skew Matrix Learning.ipynb
```

## Acknowledgements

The following resource is very helpful for our work:

- We used the implementation of the LNN model in torchdyn https://torchdyn.readthedocs.io/en/latest/tutorials/09_lagrangian_nets.html 
