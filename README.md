## Usage of Daisi

It is recommended to use this application on the daisi platform itself using the link https://app.daisi.io/daisies/vijay/Noise_Cancellation/app. However, you can still use your own editor using the below method:

### First, load the Packages:

```
import pydaisi as pyd
noise_cancellation = pyd.Daisi("vijay/Noise_Cancellation")
```

## Now, connect to Daisi and access the functions using:

### Sigmoid

```
noise_cancellation.sigmoid(x, shift, mult).value
```

Using this sigmoid to discourage one network overpowering the other

### Smoothing filter

```
noise_cancellation._smoothing_filter(n_grad_freq, n_grad_time).value
```

Arguments: n_grad_freq {[type]} -- [how many frequency channels to smooth over with the mask.] n_grad_time {[type]} -- [how many time channels to smooth over with the mask.]

### Reduce noise

```
noise_cancellation.reduce_noise(y, sr).value
```

Reduce noise via spectral gating.
