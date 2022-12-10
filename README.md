# M3239.006800: Geometric Methods for High-Dimensional Data Analysis
The official repository for the homework assignments of the lecture &lt;Geometric Methods for High-Dimensional Data Analysis> instructed by Frank C. Park in Seoul National University. 

- *[Syllabus](https://drive.google.com/file/d/12fFBcK3D4JQkCZwxvvfdTPaEjxiALBwb/view?usp=sharing)*

#### Table of Contents  
[Schedule](#Schedule)  
[Instructions for Settings](#Instructions-for-Settings)  
[Homework 1](#Homework-1)  
[Homework 2](#Homework-2)  
[Homework 3](#Homework-3)  
[Homework 4](#Homework-4)  
[Homework 5](#Homework-5)  

#### TA Contacts
- Younghun Kim (yhun@robotics.snu.ac.kr, *Head TA*)
- Yonghyeon Lee (yhlee@robotics.snu.ac.kr)
- Seungyeon Kim (ksy@robotics.snu.ac.kr)

## Schedule
Task                 | Due date              | PDF file          | Solution
:---                 |  :---:                |   :---:           | :---:
**Assignment I**     | October 5, 2022       | [pdf](https://drive.google.com/file/d/1CG5lfSkTxjxo6ZGSeH8xmc01cMBh-7H3/view?usp=sharing)        | TBA
**Assignment II**    | October 26, 2022      | [pdf](https://drive.google.com/file/d/137vAvWIOZLRwMTKf6bqIqQk7HwvnBrG_/view?usp=sharing)        | TBA
**Project Proposal** | November 9, 2022      | [pdf](https://drive.google.com/file/d/1G8mGgSrgKwB0umlJg4jBg--oui7H6Ctz/view?usp=share_link)   | -
**Assignment III**   | November 14, 2022     | [pdf](https://drive.google.com/file/d/1sbkAN_rn_Zh7ei3-cVR2uEVgBxW99n23/view?usp=share_link)   | TBA
**Assignment IV**    | November 29, 2022      | [pdf](https://drive.google.com/file/d/1ZnqgPGdb0W2K0O_m5bC3vSH3SCK7kaQY/view?usp=share_link)   | TBA
**Assignment V**     | December 12, 2022      | [pdf](https://drive.google.com/file/d/1NYY7uMvlG6PBtDo6V45K7WXabv0BvOAH/view?usp=sharing)   | TBA
**Final Project**    | December 14, 2022      |:---:   | -

## Instructions for Settings
### Install Anaconda3 and Jupyter Notebook
For those unfamiliar with environment setup, Anaconda3 installation is recommended. 
- For Windows user, download and install Anaconda3 from the following link: [https://www.anaconda.com/products/distribution](https://www.anaconda.com/products/distribution).
- For Linux user, download shell file from the following link: [Anaconda3-2022.05-Linux-x86_64.sh](https://drive.google.com/file/d/1x0mTd3stcNkEC_tY9vvgDUCwwHdPRqVe/view?usp=sharing). After that, execute the shell using the following command:
    ```shell
    chmod +x Anaconda3-2022.05-Linux-x86_64.sh      # change permission
    ./Anaconda3-2022.05-Linux-x86_64.sh             # execute shell file
    ```

After Anaconda3 installation, jupyter is automatically installed and you can run jupyter notebook with the following command:
```shell
jupyter notebook
```

### Guidelines for Anaconda3 and Jupyter Notebook
Here's some commands for conda environment:
```shell
conda create -n {name} python=3.9   # create conda environment
conda activate {name}               # activate conda environment
conda deactivate {name}             # deactivate conda environment
```
If you want to use the created conda environment in jupyter notebook, you need to register the kernel. The command to register is following:
```
pip install ipykernel
python -m ipykernel install --user --name {name} --display-name "{name-in-jupyter}"
```
- {name} and {name-in-jupyter} can be replaced by your choices.

### Environment
The project codes are tested in the following environment.
- python 3.9
- numpy
- matplotlib
- scikit-learn
- *pytorch*
- *torchvision*

To setup the environment except *pytorch* and *torchvision*, run the following script in the command line:
```
pip install -r requirements.txt
```
*Pytorch* and *torchvision* need to be installed separately using the method below.

### Torch installation
Install PyTorch and torchvision from the following link: [https://pytorch.org](https://pytorch.org). 

## Homework 1
Follow the instructions in the ``HW1.ipynb`` file. After you complete and run the HW ipython file, send the result file to ``yhun@robotics.snu.ac.kr``.   
For problem 1~5, submit your answer sheet in the class.

## Homework 2
Follow the instructions in the ``HW2.ipynb`` file. After you complete and run the HW ipython file, send the result file to ``yhun@robotics.snu.ac.kr``.   
For problem 1~4, submit your answer sheet to 302-413, or ``yhun@robotics.snu.ac.kr``

- In problem 5 of the pdf file, change $\mathcal{D} =$ \{ $(x_i,x_j)|x_i, x_j \in \mathcal{X}$ \} to $\mathcal{D} =$ \{ $(x_i,x_j)$ \}

## Homework 3
Follow the instructions in the ``HW3.ipynb`` file. After you complete and run the HW ipython file, send the result file to ``yhun@robotics.snu.ac.kr``.   
For problem 1~4, submit your answer sheet to 302-413, or ``yhun@robotics.snu.ac.kr``

Correct some errors in the problems as below: 
- In problem 1, $\ddot{Q}+\dot{\mu} \dot{\mu}^T - \dot{Q}Q^{-1} \dot{Q}=0$
- In problem 3(a), $A^TJA=J$
- In problem 4(a), $(y_1, \ldots, y_N) \in \mathbb{R}^{n}$
- In problem 4(b), The gradient of the objective function $f(X)=\mathrm{Tr}(X^T QXA - 2BX^T Q)$ can then be ... 
- In problem 4(b), $df_X(\Omega) =\lim_{\epsilon \to 0}\frac{1}{\epsilon} (f(X\exp(\Omega \epsilon)) - f(X))$
- In problem 4(b), $\dot{X} = -XAX^T QX + XB^T Q X$
- In problem 4(b) and 4(c): (Hint) In Lie group $G$, for the gradient flow $\dot{X} = g(X)$ associated with the minimization problem $\min_X f(X)$, the following equality holds: $\mathrm{Tr}(X^{-1}g(X)\Omega) = -df_{X}(\Omega)$ (to see why, $g(X)\in T_X G$ is translated to $X^{-1} g(X) \in T_I G$).  
- In problem 4(d), $\nabla_x f = G^{-1}(x) \frac{\partial f}{\partial x}^T$. 

## Homework 4
Follow the instructions in the ``HW4.ipynb`` file. After you complete and run the HW ipython file, send the result file to ``yhun@robotics.snu.ac.kr``.   
For problem 1~2, submit your answer sheet in the class or 302-413.

There was an error in the ``HW4.ipynb`` file. More specifically, in C4Group class, left_action_on_H, output size is (b,b), not (b).\
We uploaded a fixed version of ``HW4.ipynb``, which contains a solution of left_action_on_H. You can pull it from github, or simply download the file.\
The due date of the homework has been extended to December 5th. We offer sincere apologies. 

Correct some errors in the problems as below:
- In problem 1, $\mathcal{S} = ((A, b, \alpha)|A \in SL(n), b \in \mathbb{R}^n, \alpha \in \mathbb{R} )$
- In problem 1, $(A_1, b_1, \alpha_1) * (A_2, b_2, \alpha_2) = (A_1 A_2, e^{\alpha_1}A_1b_2+b_1, \alpha_1 + \alpha_2)$
- In problem 2, second equation, $\int_{S^2}f(S^{-1}p)h(R^{-1}p)dA_p = (f*h)(S^{-1}R)$

## Homework 5
There's no programming exercise. For problem 1~5, submit your answer sheet to 302-413, or ``yhun@robotics.snu.ac.kr``.

- In problem 2, you may assume that $z(0) \in$ \{-1, 1\}.
