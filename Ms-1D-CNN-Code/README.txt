Source: https://www.cse.wustl.edu/~z.cui/projects/mcnn/

#########################################################
#                    Python packages                   ##
#########################################################
0. numpy (version I use: 1.10.4)
1. Theano (version I use: 0.7.0)

Useful link for installing theano:
http://deeplearning.net/software/theano/install.html

#########################################################
#                    How To Run                       ##
#########################################################
mcnn.py trains on one of the ucr dataset, Trace, with 
multiscale convolutional neural network (MSCNN). 
It can run on both CPU and GPU.

1. run 'python mcnn.py' 
## This command trains a MSCNN with default parameters. 
## You should be able to get zero error on train set, 
## validation set as well as test set.

2. run "THEANO_FLAGS='blas.ldflags=-lblas -lgfortran,mode=FAST_RUN,
          cuda.root=/usr/local/cuda,device=gpu,floatX=float32,
          lib.cnmem=1' python mcnn.py" 
## This command trains exactly the same MSCNN as the first one. 
## However, You can enjoy 10x speedup if you have GPU with 
## CUDA installed using this command.

3. run 'python mcnn.py -h' for more information.

#########################################################
#                    Standard Output                   ##
#########################################################
increase factor is  1 , ori len 500
train size 2720 ,valid size 680  test size 1456
batch size  272
n_train_batches is  10
data dim is  1923
---------------------------
building the model...
training...
...epoch 1, valid err: 0.49412 | test err: 0.50000 | train err 0.49669, cost 1.0972
...epoch 2, valid err: 0.10000 | test err: 0.07555 | train err 0.33566, cost 0.5880
...epoch 3, valid err: 0.06324 | test err: 0.06319 | train err 0.06103, cost 0.2885
...epoch 4, valid err: 0.04706 | test err: 0.04533 | train err 0.04596, cost 0.1981
...epoch 5, valid err: 0.04118 | test err: 0.03297 | train err 0.03529, cost 0.1468
  
#########################################################
Please contact me if you have any question.
