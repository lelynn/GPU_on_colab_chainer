# GPU_on_colab_chainer

In order to use the GPU on google's colaboratory notebook, you must first correctly install cuda and cupy using the following lines:

``` 
!apt -y -q install cuda-libraries-dev-9-2
!pip install -q cupy-cuda92 chainer 
```

Then go to Runtime > change runtime type > and switch hardware accelerator to <b>GPU</b>

Finally, after initializing your model, remember to add:

```
model.to_gpu()
```
