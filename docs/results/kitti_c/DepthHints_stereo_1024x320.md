<img src="https://github.com/ldkong1205/RoboDepth/blob/main/docs/figs/logo2.png" align="right" width="34%">

# RoboDepth Benchmark
The following metrics are consistently used in our benchmark:
- Absolute Relative Difference: $\text{Abs Rel} = \frac{1}{|D|}\sum_{pred\in D}\frac{|gt - pred|}{gt}$
- Accuracy: $\delta_t = \frac{1}{|D|}|\{\ pred\in D | \max{(\frac{gt}{pred}, \frac{pred}{gt})< 1.25^t}\}| \times 100\\%$
- Depth Estimation Score (DES):
  - $\text{DES}_1 = \text{Abs Rel} - \delta_1 + 1$ 
  - $\text{DES}_2 = \frac{\text{Abs Rel} - \delta_1 + 1}{2}$
  - $\text{DES}_3 = \frac{\text{Abs Rel}}{\delta_1}$


### DepthHints, Stereo, 1024x320
| Corruption | Clean | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG | 
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |          
| $\text{DES}_{1}$ | 0.208 | 0.243     | 0.564     | 0.281     | 0.633     | 0.960     | 0.359     | 0.918     | 0.725     | 0.640     | 0.523     | 0.236     | 0.365     | 0.793     | 0.842     | 0.760     | 0.849     | 0.282     | 0.366     |
| $\text{CE}_{1}$  |      -       | 0.914  | 0.810  | 0.873  | 1.038  | 0.931  | 0.767  | 1.178  | 1.094  | 1.210  | 1.248  | 0.874  | 0.915  | 0.805  | 0.827  | 0.820  | 0.862  | 0.979  | 0.946  |
| $\text{RCE}_{1}$ |      -       | 1.750 | 0.791 | 0.961 | 1.168 | 0.958 | 0.680 | 1.332 | 1.240 | 1.527 | 1.821 | 1.167 | 1.026 | 0.792 | 0.821 | 0.811 | 0.867 | 1.762 | 1.121 |
| $\text{DES}_{2}$ | 0.104 | 0.122     | 0.282     | 0.141     | 0.317     | 0.480     | 0.180     | 0.459     | 0.363     | 0.320     | 0.262     | 0.118     | 0.183     | 0.397     | 0.421     | 0.380     | 0.424     | 0.141     | 0.183     |
| $\text{CE}_{2}$  |      -       | 0.917  | 0.810  | 0.876  | 1.039  | 0.932  | 0.769  | 1.177  | 1.093  | 1.212  | 1.254  | 0.874  | 0.915  | 0.807  | 0.827  | 0.821  | 0.860  | 0.979  | 0.943  |
| $\text{RCE}_{2}$ |      -       | 1.800 | 0.791 | 0.974 | 1.170 | 0.959 | 0.685 | 1.330 | 1.239 | 1.532 | 1.837 | 1.167 | 1.026 | 0.794 | 0.821 | 0.812 | 0.865 | 1.762 | 1.113 |
| $\text{DES}_{3}$ | 0.109 | 0.125     | 0.320     | 0.141     | 0.387     | 0.898     | 0.182     | 0.803     | 0.494     | 0.399     | 0.290     | 0.120     | 0.186     | 0.574     | 0.651     | 0.528     | 0.659     | 0.146     | 0.187     |
| $\text{CE}_{3}$  |      -       | 0.912  | 0.703  | 0.865  | 1.038  | 0.828  | 0.711  | 1.416  | 1.182  | 1.339  | 1.306  | 0.870  | 0.907  | 0.598  | 0.619  | 0.641  | 0.686  | 0.967  | 0.926  |
| $\text{RCE}_{3}$ |      -       | 1.600 | 0.643 | 0.889 | 1.130 | 0.824 | 0.566 | 1.577 | 1.323 | 1.696 | 1.905 | 1.000 | 0.987 | 0.558 | 0.586 | 0.601 | 0.660 | 1.542 | 1.040 |

- **Summary:** $\text{mCE}_1 =$ 0.949, $\text{RmCE}_1 =$ 1.144, $\text{mCE}_2 =$ 0.950, $\text{RmCE}_2 =$ 1.149, $\text{mCE}_3 =$ 0.917, $\text{RmCE}_3 =$ 1.063


### Clean
| $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0.097 | 0.734 | 4.454 | 0.187 | 0.889 | 0.961 | 0.981 |

- **Summary:** $\text{DES}_1=$ 0.208, $\text{DES}_2=$ 0.104, $\text{DES}_3=$ 0.109


### Brightness
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.097 | 0.737 | 4.473 | 0.187 | 0.889 | 0.961 | 0.981 |
|   2   | 0.100 | 0.747 | 4.538 | 0.191 | 0.882 | 0.959 | 0.980 |
|   3   | 0.105 | 0.770 | 4.660 | 0.198 | 0.870 | 0.954 | 0.979 |
|   4   | 0.113 | 0.815 | 4.878 | 0.209 | 0.851 | 0.947 | 0.976 |
|   5   | 0.123 | 0.894 | 5.199 | 0.223 | 0.829 | 0.936 | 0.972 |
|  avg  | 0.108 | 0.793 | 4.750 | 0.202 | 0.864 | 0.951 | 0.978 |

- **Summary:** $\text{DES}_1=$ 0.243, $\text{DES}_2=$ 0.122, $\text{DES}_3=$ 0.125


### Dark
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.122 | 0.939 | 5.242 | 0.226 | 0.832 | 0.936 | 0.971 |
|   2   | 0.142 | 1.128 | 5.909 | 0.254 | 0.788 | 0.916 | 0.962 |
|   3   | 0.186 | 1.658 | 7.395 | 0.320 | 0.682 | 0.864 | 0.936 |
|   4   | 0.257 | 2.754 | 9.791 | 0.435 | 0.514 | 0.756 | 0.871 |
|   5   | 0.319 | 3.924 | 11.762 | 0.556 | 0.389 | 0.644 | 0.791 |
|  avg  | 0.205 | 2.081 | 8.020 | 0.358 | 0.641 | 0.823 | 0.906 |

- **Summary:** $\text{DES}_1=$ 0.564, $\text{DES}_2=$ 0.282, $\text{DES}_3=$ 0.320


### Fog
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.107 | 0.802 | 4.716 | 0.202 | 0.865 | 0.951 | 0.977 |
|   2   | 0.110 | 0.816 | 4.797 | 0.206 | 0.858 | 0.948 | 0.976 |
|   3   | 0.115 | 0.862 | 4.940 | 0.215 | 0.846 | 0.941 | 0.973 |
|   4   | 0.119 | 0.905 | 5.064 | 0.224 | 0.835 | 0.935 | 0.970 |
|   5   | 0.140 | 1.119 | 5.626 | 0.268 | 0.782 | 0.903 | 0.952 |
|  avg  | 0.118 | 0.901 | 5.029 | 0.223 | 0.837 | 0.936 | 0.970 |

- **Summary:** $\text{DES}_1=$ 0.281, $\text{DES}_2=$ 0.141, $\text{DES}_3=$ 0.141


### Frost
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.132 | 1.014 | 5.246 | 0.249 | 0.804 | 0.914 | 0.957 |
|   2   | 0.189 | 1.653 | 6.670 | 0.361 | 0.674 | 0.823 | 0.900 |
|   3   | 0.251 | 2.503 | 8.202 | 0.483 | 0.554 | 0.721 | 0.821 |
|   4   | 0.266 | 2.769 | 8.648 | 0.515 | 0.528 | 0.696 | 0.801 |
|   5   | 0.319 | 3.614 | 9.949 | 0.621 | 0.430 | 0.604 | 0.727 |
|  avg  | 0.231 | 2.311 | 7.743 | 0.446 | 0.598 | 0.752 | 0.841 |

- **Summary:** $\text{DES}_1=$ 0.633, $\text{DES}_2=$ 0.317, $\text{DES}_3=$ 0.387


### Snow
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.224 | 1.973 | 6.934 | 0.425 | 0.610 | 0.767 | 0.860 |
|   2   | 0.325 | 3.550 | 9.738 | 0.628 | 0.429 | 0.591 | 0.714 |
|   3   | 0.374 | 4.244 | 10.437 | 0.723 | 0.350 | 0.498 | 0.636 |
|   4   | 0.447 | 5.628 | 12.289 | 0.883 | 0.248 | 0.379 | 0.522 |
|   5   | 0.389 | 4.812 | 11.643 | 0.758 | 0.322 | 0.484 | 0.624 |
|  avg  | 0.352 | 4.041 | 10.208 | 0.683 | 0.392 | 0.544 | 0.671 |

- **Summary:** $\text{DES}_1=$ 0.960, $\text{DES}_2=$ 0.480, $\text{DES}_3=$ 0.898


### Contrast
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.103 | 0.787 | 4.654 | 0.197 | 0.874 | 0.955 | 0.979 |
|   2   | 0.107 | 0.801 | 4.740 | 0.202 | 0.865 | 0.951 | 0.977 |
|   3   | 0.115 | 0.851 | 4.951 | 0.214 | 0.846 | 0.943 | 0.974 |
|   4   | 0.147 | 1.212 | 6.122 | 0.271 | 0.771 | 0.903 | 0.954 |
|   5   | 0.243 | 2.794 | 9.829 | 0.454 | 0.563 | 0.763 | 0.862 |
|  avg  | 0.143 | 1.289 | 6.059 | 0.268 | 0.784 | 0.903 | 0.949 |

- **Summary:** $\text{DES}_1=$ 0.359, $\text{DES}_2=$ 0.180, $\text{DES}_3=$ 0.182


### Defocus Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.139 | 1.180 | 5.806 | 0.264 | 0.793 | 0.909 | 0.952 |
|   2   | 0.204 | 2.089 | 7.777 | 0.404 | 0.654 | 0.813 | 0.885 |
|   3   | 0.396 | 5.482 | 13.308 | 0.816 | 0.295 | 0.509 | 0.639 |
|   4   | 0.468 | 6.858 | 14.835 | 0.964 | 0.180 | 0.385 | 0.529 |
|   5   | 0.473 | 6.944 | 14.928 | 0.966 | 0.169 | 0.374 | 0.522 |
|  avg  | 0.336 | 4.511 | 11.331 | 0.683 | 0.418 | 0.598 | 0.705 |

- **Summary:** $\text{DES}_1=$ 0.918, $\text{DES}_2=$ 0.459, $\text{DES}_3=$ 0.803


### Glass Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.121 | 0.995 | 5.349 | 0.221 | 0.831 | 0.937 | 0.971 |
|   2   | 0.153 | 1.423 | 6.597 | 0.290 | 0.758 | 0.891 | 0.942 |
|   3   | 0.264 | 3.268 | 10.515 | 0.533 | 0.526 | 0.713 | 0.817 |
|   4   | 0.332 | 4.455 | 12.252 | 0.678 | 0.407 | 0.600 | 0.723 |
|   5   | 0.470 | 6.905 | 14.899 | 0.968 | 0.192 | 0.377 | 0.519 |
|  avg  | 0.268 | 3.409 | 9.922 | 0.538 | 0.543 | 0.704 | 0.794 |

- **Summary:** $\text{DES}_1=$ 0.725, $\text{DES}_2=$ 0.363, $\text{DES}_3=$ 0.494


### Motion Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.115 | 0.900 | 5.038 | 0.212 | 0.850 | 0.946 | 0.975 |
|   2   | 0.137 | 1.141 | 5.739 | 0.253 | 0.800 | 0.919 | 0.960 |
|   3   | 0.213 | 2.246 | 8.241 | 0.410 | 0.632 | 0.807 | 0.884 |
|   4   | 0.333 | 4.440 | 11.997 | 0.677 | 0.404 | 0.617 | 0.731 |
|   5   | 0.395 | 5.594 | 13.474 | 0.813 | 0.305 | 0.517 | 0.640 |
|  avg  | 0.239 | 2.864 | 8.898 | 0.473 | 0.598 | 0.761 | 0.838 |

- **Summary:** $\text{DES}_1=$ 0.640, $\text{DES}_2=$ 0.320, $\text{DES}_3=$ 0.399


### Zoom Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.169 | 1.499 | 6.579 | 0.320 | 0.729 | 0.870 | 0.929 |
|   2   | 0.214 | 2.158 | 7.934 | 0.420 | 0.633 | 0.802 | 0.880 |
|   3   | 0.184 | 1.698 | 7.179 | 0.337 | 0.695 | 0.852 | 0.921 |
|   4   | 0.212 | 2.126 | 8.062 | 0.397 | 0.636 | 0.810 | 0.891 |
|   5   | 0.196 | 1.854 | 7.603 | 0.354 | 0.666 | 0.837 | 0.912 |
|  avg  | 0.195 | 1.867 | 7.471 | 0.366 | 0.672 | 0.834 | 0.907 |

- **Summary:** $\text{DES}_1=$ 0.523, $\text{DES}_2=$ 0.262, $\text{DES}_3=$ 0.290


### Elastic Transform
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.099 | 0.745 | 4.538 | 0.192 | 0.881 | 0.958 | 0.980 |
|   2   | 0.100 | 0.754 | 4.567 | 0.193 | 0.878 | 0.957 | 0.979 |
|   3   | 0.103 | 0.774 | 4.650 | 0.198 | 0.871 | 0.954 | 0.978 |
|   4   | 0.105 | 0.775 | 4.701 | 0.202 | 0.864 | 0.951 | 0.977 |
|   5   | 0.112 | 0.831 | 4.920 | 0.214 | 0.847 | 0.942 | 0.974 |
|  avg  | 0.104 | 0.776 | 4.675 | 0.200 | 0.868 | 0.952 | 0.978 |

- **Summary:** $\text{DES}_1=$ 0.236, $\text{DES}_2=$ 0.118, $\text{DES}_3=$ 0.120


### Color Quant
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.097 | 0.737 | 4.452 | 0.186 | 0.889 | 0.962 | 0.981 |
|   2   | 0.099 | 0.740 | 4.462 | 0.187 | 0.888 | 0.961 | 0.981 |
|   3   | 0.107 | 0.801 | 4.658 | 0.200 | 0.869 | 0.954 | 0.978 |
|   4   | 0.146 | 1.141 | 5.687 | 0.268 | 0.774 | 0.903 | 0.954 |
|   5   | 0.277 | 3.040 | 9.693 | 0.517 | 0.480 | 0.694 | 0.819 |
|  avg  | 0.145 | 1.292 | 5.790 | 0.272 | 0.780 | 0.895 | 0.943 |

- **Summary:** $\text{DES}_1=$ 0.365, $\text{DES}_2=$ 0.183, $\text{DES}_3=$ 0.186


### Gaussian Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.154 | 1.121 | 5.918 | 0.250 | 0.766 | 0.915 | 0.968 |
|   2   | 0.208 | 1.886 | 7.923 | 0.344 | 0.625 | 0.833 | 0.922 |
|   3   | 0.291 | 3.367 | 10.788 | 0.504 | 0.438 | 0.683 | 0.820 |
|   4   | 0.355 | 4.608 | 12.597 | 0.636 | 0.322 | 0.558 | 0.721 |
|   5   | 0.386 | 5.236 | 13.375 | 0.704 | 0.278 | 0.499 | 0.670 |
|  avg  | 0.279 | 3.244 | 10.120 | 0.488 | 0.486 | 0.698 | 0.820 |

- **Summary:** $\text{DES}_1=$ 0.793, $\text{DES}_2=$ 0.397, $\text{DES}_3=$ 0.574


### Impulse Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.179 | 1.460 | 6.896 | 0.290 | 0.711 | 0.882 | 0.949 |
|   2   | 0.249 | 2.607 | 9.503 | 0.419 | 0.533 | 0.763 | 0.876 |
|   3   | 0.299 | 3.538 | 11.129 | 0.519 | 0.423 | 0.669 | 0.809 |
|   4   | 0.362 | 4.751 | 12.805 | 0.650 | 0.311 | 0.546 | 0.712 |
|   5   | 0.384 | 5.199 | 13.340 | 0.699 | 0.285 | 0.504 | 0.675 |
|  avg  | 0.295 | 3.511 | 10.735 | 0.515 | 0.453 | 0.673 | 0.804 |

- **Summary:** $\text{DES}_1=$ 0.842, $\text{DES}_2=$ 0.421, $\text{DES}_3=$ 0.651


### Shot Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.135 | 0.912 | 5.304 | 0.220 | 0.817 | 0.941 | 0.977 |
|   2   | 0.193 | 1.640 | 7.426 | 0.310 | 0.664 | 0.864 | 0.943 |
|   3   | 0.275 | 3.100 | 10.419 | 0.469 | 0.469 | 0.715 | 0.842 |
|   4   | 0.361 | 4.738 | 12.758 | 0.649 | 0.314 | 0.544 | 0.709 |
|   5   | 0.382 | 5.148 | 13.253 | 0.696 | 0.283 | 0.502 | 0.673 |
|  avg  | 0.269 | 3.108 | 9.832 | 0.469 | 0.509 | 0.713 | 0.829 |

- **Summary:** $\text{DES}_1=$ 0.760, $\text{DES}_2=$ 0.380, $\text{DES}_3=$ 0.528


### ISO Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.219 | 2.061 | 8.394 | 0.358 | 0.598 | 0.819 | 0.915 |
|   2   | 0.246 | 2.543 | 9.372 | 0.411 | 0.534 | 0.770 | 0.882 |
|   3   | 0.289 | 3.346 | 10.797 | 0.498 | 0.442 | 0.688 | 0.823 |
|   4   | 0.336 | 4.255 | 12.140 | 0.597 | 0.353 | 0.595 | 0.751 |
|   5   | 0.374 | 4.970 | 13.050 | 0.675 | 0.293 | 0.521 | 0.690 |
|  avg  | 0.293 | 3.435 | 10.751 | 0.508 | 0.444 | 0.679 | 0.812 |

- **Summary:** $\text{DES}_1=$ 0.849, $\text{DES}_2=$ 0.424, $\text{DES}_3=$ 0.659


### Pixelate
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.105 | 0.839 | 4.604 | 0.189 | 0.881 | 0.959 | 0.981 |
|   2   | 0.106 | 0.836 | 4.619 | 0.191 | 0.877 | 0.958 | 0.981 |
|   3   | 0.116 | 0.926 | 4.866 | 0.202 | 0.858 | 0.951 | 0.978 |
|   4   | 0.135 | 1.156 | 5.469 | 0.233 | 0.811 | 0.926 | 0.967 |
|   5   | 0.151 | 1.402 | 5.927 | 0.257 | 0.778 | 0.905 | 0.955 |
|  avg  | 0.123 | 1.032 | 5.097 | 0.214 | 0.841 | 0.940 | 0.972 |

- **Summary:** $\text{DES}_1=$ 0.282, $\text{DES}_2=$ 0.141, $\text{DES}_3=$ 0.146


### JPEG Compression
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.112 | 0.866 | 4.778 | 0.208 | 0.855 | 0.947 | 0.975 |
|   2   | 0.123 | 0.954 | 4.997 | 0.224 | 0.831 | 0.935 | 0.971 |
|   3   | 0.132 | 1.034 | 5.163 | 0.237 | 0.810 | 0.925 | 0.967 |
|   4   | 0.161 | 1.321 | 5.793 | 0.281 | 0.741 | 0.889 | 0.950 |
|   5   | 0.199 | 1.786 | 6.652 | 0.338 | 0.660 | 0.839 | 0.921 |
|  avg  | 0.145 | 1.192 | 5.477 | 0.258 | 0.779 | 0.907 | 0.957 |

- **Summary:** $\text{DES}_1=$ 0.366, $\text{DES}_2=$ 0.183, $\text{DES}_3=$ 0.187

