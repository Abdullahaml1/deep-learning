# deep-learning


# Rsources for RNNs
* week8 -> lec16
* [arabic rnns](https://www.youtube.com/watch?v=2ftru4s6gvU&list=PLQkyODvJ8ywsLydDYORIlJxV9KarhXp9O&index=124)
* [oxford lecture](https://www.youtube.com/watch?v=56TYLaQN4N8&list=PLE6Wd9FR--EfW8dtjAuPoTuPcqmOV53Fu&index=15)
* [LSTM mathematical drivations](https://arunmallya.github.io/writeups/nn/lstm/index.html#/1)
* [RNNs applications](https://karpathy.github.io/2015/05/21/rnn-effectiveness/)
* [how vanishing gradient is solved in LSTM](https://medium.datadriveninvestor.com/how-do-lstm-networks-solve-the-problem-of-vanishing-gradients-a6784971a577)

# CUDA
for cuda check `cuda` directory

# pytorch
I used anaconda to deploy pytorch

### Activating anaconda3
```bash
source ~/anaconda3/bin activate
```

### install pytorch nightly version [resource](https://discuss.pytorch.org/t/pytorch-cuda-11-6/149647/2)
We installed nightly version becasue we used CUDA 11.6 that is not supported by the official verion

```bash
pip install torch torchvision torchaudio --pre --extra-index-url https://download.pytorch.org/whl/nightly/cu116
```

### test installation
```python
import torch
import torchvision
import torchaudio

print(torch.cuda.is_available())
print(torchvision.torch.cuda.is_available())

# device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
device = torch.device("cuda")

x = torch.rand(5, 3)
print(x)
```



# Accelerate scikit-learn

 Installed package of scikit-learn can be accelerated using scikit-learn-intelex. More details are available here: https://intel.github.io/scikit-learn-intelex

 ```
    For example:

        $ conda install scikit-learn-intelex
        $ python -m sklearnex my_application.py
```


