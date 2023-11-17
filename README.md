# VulMAE#
=========
Code for paper "VulMAE: Graph Masked Autoencoders for Vulnerability Detection from Source and Binary Codes", FPS 2023

The major Dependencies:
======================
* Python >= 3.7
* [Pytorch](https://pytorch.org/) >= 1.9.0 
* [dgl](https://www.dgl.ai/) >= 0.7.2
* pyyaml == 5.4.1

Sample Run:
==========

(1) Without SMOTE:
python main_graph.py --dataset A02BR8J6RMQ25ADCC02PU3IR9RAZ633H --encoder gat --decoder mlp --seed 50 --max_epoch 2 --loss_fn='mse' 

(2) With SMOTE:
python main_graph_smote.py --dataset A02BR8J6RMQ25ADCC02PU3IR9RAZ633H --encoder gat --decoder mlp --seed 50 --max_epoch 2 --loss_fn='mse'


The dataset folder supports 5 different graph types (AST (SDR7H7BHKJ97SSNOQUBGQE7FNRICVTPU), CFG (I1JMTK6PSIUEO6N1ZBKLL3NFFIGBSN0F), CPG (A02BR8J6RMQ25ADCC02PU3IR9RAZ633H), BIN (C2XK83BR49EP8TI19DRJ29EX5MSGY0WL), CDCPG (SDR7H7BHKJ97SSNOQUBGQE7FNRICVTPUCDCPG)). So you can replace with different graph types for your evaluation.

The encoder/decoder used in our experiments: GAT, GIN, MLP, GCN

The loss function used in our experiments: MSE, InfoNCE, SCE, SIG, FocalLoss, FocalLossBCE, DCL and DCLW


Contact info:
============

mahmoud.zamani@utdallas.edu (zamanioracle@gmail.com)

saquib.irtiza@utdallas.edu
