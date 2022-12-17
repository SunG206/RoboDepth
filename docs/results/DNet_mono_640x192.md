<img src="../../figs/logo2.png" align="right" width="34%">

# RoboDepth Benchmark
The following metrics are consistently used in our benchmark:
- Absolute Relative Difference: $\text{Abs Rel} = \frac{1}{|D|}\sum_{pred\in D}\frac{|gt - pred|}{gt}$
- Accuracy: $\delta_t = \frac{1}{|D|}|\{\ pred\in D | \max{(\frac{gt}{pred}, \frac{pred}{gt})< 1.25^t}\}| \times 100\\%$
- Depth Estimation Score (DES):
  - $\text{DES}_1 = \text{Abs Rel} - \delta_1 + 1$ 
  - $\text{DES}_2 = \frac{\text{Abs Rel} - \delta_1 + 1}{2}$
  - $\text{DES}_3 = \frac{\text{Abs Rel}}{\delta_1}$



### DNet, Mono, 640x192
| Corruption | Clean | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG | 
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |          
| $\text{DES}_{1}$ | 0.237 | 0.256     | 0.528     | 0.313     | 0.634     | 1.007     | 0.419     | 0.696     | 0.640     | 0.485     | 0.429     | 0.262     | 0.377     | 0.724     | 0.732     | 0.651     | 0.715     | 0.290     | 0.381     |
| $\text{CE}_{1}$  |      -       | 0.988  | 0.941  | 1.006  | 1.146  | 0.984  | 1.123  | 1.429  | 1.322  | 1.120  | 1.067  | 1.016  | 0.977  | 0.943  | 0.940  | 0.956  | 0.921  | 1.003  | 0.974  |
| $\text{RCE}_{1}$ |      -       | 0.905 | 0.901 | 1.041 | 1.260 | 0.981 | 1.348 | 1.843 | 1.638 | 1.272 | 1.171 | 1.250 | 0.946 | 0.919 | 0.915 | 0.935 | 0.888 | 1.039 | 0.941 |
| $\text{DES}_{2}$ | 0.118 | 0.128     | 0.264     | 0.156     | 0.317     | 0.504     | 0.209     | 0.348     | 0.320     | 0.242     | 0.215     | 0.131     | 0.189     | 0.362     | 0.366     | 0.326     | 0.357     | 0.145     | 0.190     |
| $\text{CE}_{2}$  |      -       | 0.985  | 0.943  | 1.006  | 1.144  | 0.986  | 1.118  | 1.426  | 1.322  | 1.120  | 1.070  | 1.016  | 0.979  | 0.943  | 0.941  | 0.959  | 0.920  | 1.000  | 0.969  |
| $\text{RCE}_{2}$ |      -       | 0.909 | 0.907 | 1.056 | 1.259 | 0.985 | 1.338 | 1.840 | 1.642 | 1.278 | 1.183 | 1.300 | 0.959 | 0.921 | 0.919 | 0.941 | 0.888 | 1.038 | 0.935 |
| $\text{DES}_{3}$ | 0.130 | 0.138     | 0.300     | 0.167     | 0.402     | 1.019     | 0.226     | 0.468     | 0.402     | 0.272     | 0.236     | 0.141     | 0.202     | 0.495     | 0.503     | 0.413     | 0.480     | 0.158     | 0.209     |
| $\text{CE}_{3}$  |      -       | 0.986  | 0.909  | 1.006  | 1.229  | 0.963  | 1.136  | 1.727  | 1.489  | 1.153  | 1.068  | 1.000  | 0.967  | 0.898  | 0.893  | 0.934  | 0.862  | 1.000  | 0.972  |
| $\text{RCE}_{3}$ |      -       | 0.889 | 0.854 | 1.057 | 1.388 | 0.959 | 1.412 | 2.414 | 1.957 | 1.352 | 1.178 | 1.100 | 0.923 | 0.869 | 0.863 | 0.910 | 0.822 | 1.037 | 0.940 |

- **Summary:** $\text{mCE}_1 =$ 1.048, $\text{RmCE}_1 =$ 1.122, $\text{mCE}_2 =$ 1.047, $\text{RmCE}_2 =$ 1.128, $\text{mCE}_3 =$ 1.066, $\text{RmCE}_3 =$ 1.162


INFO:root:



### Clean
| $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0.114 | 0.867 | 4.819 | 0.191 | 0.877 | 0.960 | 0.981 |

- **Summary:** $\text{DES}_1=$ 0.237, $\text{DES}_2=$ 0.118, $\text{DES}_3=$ 0.130




### Brightness
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.114 | 0.878 | 4.828 | 0.192 | 0.876 | 0.960 | 0.981 |
|   2   | 0.116 | 0.902 | 4.883 | 0.194 | 0.872 | 0.959 | 0.981 |
|   3   | 0.118 | 0.926 | 4.961 | 0.197 | 0.866 | 0.957 | 0.981 |
|   4   | 0.122 | 0.949 | 5.060 | 0.201 | 0.857 | 0.954 | 0.980 |
|   5   | 0.126 | 0.966 | 5.173 | 0.206 | 0.847 | 0.951 | 0.979 |
|  avg  | 0.119 | 0.924 | 4.981 | 0.198 | 0.864 | 0.956 | 0.980 |

- **Summary:** $\text{DES}_1=$ 0.256, $\text{DES}_2=$ 0.128, $\text{DES}_3=$ 0.138




### Dark
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.146 | 1.108 | 5.622 | 0.227 | 0.808 | 0.937 | 0.975 |
|   2   | 0.160 | 1.215 | 5.978 | 0.244 | 0.774 | 0.925 | 0.971 |
|   3   | 0.186 | 1.441 | 6.619 | 0.275 | 0.712 | 0.902 | 0.961 |
|   4   | 0.231 | 1.888 | 7.699 | 0.331 | 0.596 | 0.853 | 0.938 |
|   5   | 0.289 | 2.566 | 9.039 | 0.396 | 0.481 | 0.783 | 0.906 |
|  avg  | 0.202 | 1.644 | 6.991 | 0.295 | 0.674 | 0.880 | 0.950 |

- **Summary:** $\text{DES}_1=$ 0.528, $\text{DES}_2=$ 0.264, $\text{DES}_3=$ 0.300




### Fog
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.127 | 0.987 | 5.170 | 0.209 | 0.846 | 0.949 | 0.977 |
|   2   | 0.132 | 1.026 | 5.289 | 0.214 | 0.837 | 0.946 | 0.976 |
|   3   | 0.138 | 1.071 | 5.460 | 0.222 | 0.825 | 0.940 | 0.974 |
|   4   | 0.138 | 1.053 | 5.486 | 0.224 | 0.823 | 0.940 | 0.974 |
|   5   | 0.152 | 1.173 | 5.799 | 0.241 | 0.793 | 0.928 | 0.969 |
|  avg  | 0.137 | 1.062 | 5.441 | 0.222 | 0.825 | 0.941 | 0.974 |

- **Summary:** $\text{DES}_1=$ 0.313, $\text{DES}_2=$ 0.156, $\text{DES}_3=$ 0.167




### Frost
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.151 | 1.226 | 5.499 | 0.230 | 0.801 | 0.934 | 0.972 |
|   2   | 0.211 | 1.845 | 6.572 | 0.299 | 0.680 | 0.876 | 0.945 |
|   3   | 0.266 | 2.523 | 7.634 | 0.358 | 0.563 | 0.824 | 0.919 |
|   4   | 0.279 | 2.671 | 7.860 | 0.373 | 0.544 | 0.803 | 0.912 |
|   5   | 0.322 | 3.263 | 8.632 | 0.413 | 0.471 | 0.760 | 0.888 |
|  avg  | 0.246 | 2.306 | 7.239 | 0.335 | 0.612 | 0.839 | 0.927 |

- **Summary:** $\text{DES}_1=$ 0.634, $\text{DES}_2=$ 0.317, $\text{DES}_3=$ 0.402




### Snow
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.263 | 2.555 | 7.286 | 0.351 | 0.580 | 0.824 | 0.921 |
|   2   | 0.400 | 4.911 | 10.135 | 0.470 | 0.380 | 0.676 | 0.849 |
|   3   | 0.428 | 5.885 | 10.800 | 0.486 | 0.365 | 0.655 | 0.833 |
|   4   | 0.481 | 7.158 | 12.087 | 0.529 | 0.314 | 0.599 | 0.798 |
|   5   | 0.442 | 5.765 | 10.972 | 0.512 | 0.338 | 0.629 | 0.818 |
|  avg  | 0.403 | 5.255 | 10.256 | 0.470 | 0.395 | 0.677 | 0.844 |

- **Summary:** $\text{DES}_1=$ 1.007, $\text{DES}_2=$ 0.504, $\text{DES}_3=$ 1.019




### Contrast
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.122 | 0.954 | 5.042 | 0.202 | 0.860 | 0.954 | 0.979 |
|   2   | 0.127 | 0.982 | 5.188 | 0.209 | 0.848 | 0.950 | 0.978 |
|   3   | 0.140 | 1.063 | 5.528 | 0.226 | 0.819 | 0.939 | 0.973 |
|   4   | 0.182 | 1.409 | 6.716 | 0.287 | 0.722 | 0.900 | 0.954 |
|   5   | 0.276 | 2.541 | 9.331 | 0.408 | 0.505 | 0.791 | 0.900 |
|  avg  | 0.169 | 1.390 | 6.361 | 0.266 | 0.751 | 0.907 | 0.957 |

- **Summary:** $\text{DES}_1=$ 0.419, $\text{DES}_2=$ 0.209, $\text{DES}_3=$ 0.226




### Defocus Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.166 | 1.383 | 6.483 | 0.262 | 0.766 | 0.914 | 0.960 |
|   2   | 0.230 | 2.094 | 7.735 | 0.335 | 0.635 | 0.849 | 0.929 |
|   3   | 0.302 | 3.001 | 9.052 | 0.415 | 0.512 | 0.759 | 0.883 |
|   4   | 0.323 | 3.273 | 9.673 | 0.449 | 0.470 | 0.732 | 0.863 |
|   5   | 0.316 | 3.196 | 9.962 | 0.453 | 0.472 | 0.736 | 0.865 |
|  avg  | 0.267 | 2.589 | 8.581 | 0.383 | 0.571 | 0.798 | 0.900 |

- **Summary:** $\text{DES}_1=$ 0.696, $\text{DES}_2=$ 0.348, $\text{DES}_3=$ 0.468




### Glass Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.142 | 1.183 | 5.981 | 0.229 | 0.816 | 0.935 | 0.972 |
|   2   | 0.169 | 1.471 | 6.859 | 0.268 | 0.756 | 0.908 | 0.958 |
|   3   | 0.253 | 2.300 | 8.446 | 0.362 | 0.567 | 0.830 | 0.920 |
|   4   | 0.289 | 2.662 | 9.122 | 0.405 | 0.490 | 0.784 | 0.899 |
|   5   | 0.360 | 3.553 | 10.355 | 0.487 | 0.385 | 0.686 | 0.846 |
|  avg  | 0.243 | 2.234 | 8.153 | 0.350 | 0.603 | 0.829 | 0.919 |

- **Summary:** $\text{DES}_1=$ 0.640, $\text{DES}_2=$ 0.320, $\text{DES}_3=$ 0.402




### Motion Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.130 | 1.021 | 5.375 | 0.213 | 0.842 | 0.948 | 0.977 |
|   2   | 0.150 | 1.203 | 6.084 | 0.243 | 0.793 | 0.927 | 0.968 |
|   3   | 0.191 | 1.664 | 7.250 | 0.299 | 0.705 | 0.880 | 0.944 |
|   4   | 0.235 | 2.169 | 8.138 | 0.348 | 0.616 | 0.834 | 0.922 |
|   5   | 0.255 | 2.421 | 8.589 | 0.376 | 0.580 | 0.808 | 0.907 |
|  avg  | 0.192 | 1.696 | 7.087 | 0.296 | 0.707 | 0.879 | 0.944 |

- **Summary:** $\text{DES}_1=$ 0.485, $\text{DES}_2=$ 0.242, $\text{DES}_3=$ 0.272




### Zoom Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.163 | 1.353 | 6.085 | 0.252 | 0.775 | 0.921 | 0.965 |
|   2   | 0.180 | 1.501 | 6.426 | 0.272 | 0.738 | 0.904 | 0.957 |
|   3   | 0.171 | 1.368 | 6.271 | 0.261 | 0.755 | 0.911 | 0.961 |
|   4   | 0.183 | 1.491 | 6.507 | 0.273 | 0.731 | 0.900 | 0.956 |
|   5   | 0.183 | 1.530 | 6.508 | 0.272 | 0.735 | 0.902 | 0.956 |
|  avg  | 0.176 | 1.449 | 6.359 | 0.266 | 0.747 | 0.908 | 0.959 |

- **Summary:** $\text{DES}_1=$ 0.429, $\text{DES}_2=$ 0.215, $\text{DES}_3=$ 0.236




### Elastic Transform
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.118 | 0.933 | 4.952 | 0.196 | 0.870 | 0.957 | 0.980 |
|   2   | 0.119 | 0.931 | 4.987 | 0.198 | 0.867 | 0.956 | 0.980 |
|   3   | 0.121 | 0.957 | 5.086 | 0.201 | 0.861 | 0.954 | 0.979 |
|   4   | 0.123 | 0.977 | 5.179 | 0.204 | 0.856 | 0.952 | 0.979 |
|   5   | 0.127 | 1.011 | 5.299 | 0.209 | 0.846 | 0.948 | 0.978 |
|  avg  | 0.122 | 0.962 | 5.101 | 0.202 | 0.860 | 0.953 | 0.979 |

- **Summary:** $\text{DES}_1=$ 0.262, $\text{DES}_2=$ 0.131, $\text{DES}_3=$ 0.141




### Color Quant
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.114 | 0.868 | 4.825 | 0.192 | 0.877 | 0.959 | 0.981 |
|   2   | 0.115 | 0.880 | 4.853 | 0.193 | 0.874 | 0.959 | 0.981 |
|   3   | 0.127 | 0.980 | 5.092 | 0.206 | 0.850 | 0.952 | 0.979 |
|   4   | 0.169 | 1.317 | 5.987 | 0.252 | 0.758 | 0.921 | 0.969 |
|   5   | 0.264 | 2.274 | 7.953 | 0.356 | 0.544 | 0.832 | 0.932 |
|  avg  | 0.158 | 1.264 | 5.742 | 0.240 | 0.781 | 0.925 | 0.968 |

- **Summary:** $\text{DES}_1=$ 0.377, $\text{DES}_2=$ 0.189, $\text{DES}_3=$ 0.202




### Gaussian Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.160 | 1.195 | 5.865 | 0.241 | 0.772 | 0.926 | 0.972 |
|   2   | 0.199 | 1.545 | 6.741 | 0.288 | 0.680 | 0.891 | 0.956 |
|   3   | 0.273 | 2.299 | 8.106 | 0.367 | 0.513 | 0.812 | 0.923 |
|   4   | 0.342 | 3.074 | 9.276 | 0.435 | 0.407 | 0.717 | 0.883 |
|   5   | 0.382 | 3.568 | 10.191 | 0.480 | 0.366 | 0.659 | 0.848 |
|  avg  | 0.271 | 2.336 | 8.036 | 0.362 | 0.548 | 0.801 | 0.916 |

- **Summary:** $\text{DES}_1=$ 0.724, $\text{DES}_2=$ 0.362, $\text{DES}_3=$ 0.495




### Impulse Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.177 | 1.338 | 6.359 | 0.266 | 0.730 | 0.907 | 0.964 |
|   2   | 0.219 | 1.756 | 7.394 | 0.319 | 0.629 | 0.862 | 0.942 |
|   3   | 0.258 | 2.174 | 8.177 | 0.362 | 0.540 | 0.822 | 0.922 |
|   4   | 0.330 | 3.017 | 9.521 | 0.436 | 0.418 | 0.730 | 0.882 |
|   5   | 0.369 | 3.467 | 10.224 | 0.476 | 0.374 | 0.671 | 0.853 |
|  avg  | 0.271 | 2.350 | 8.335 | 0.372 | 0.538 | 0.798 | 0.913 |

- **Summary:** $\text{DES}_1=$ 0.732, $\text{DES}_2=$ 0.366, $\text{DES}_3=$ 0.503




### Shot Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.135 | 0.973 | 5.380 | 0.214 | 0.828 | 0.945 | 0.979 |
|   2   | 0.165 | 1.208 | 6.193 | 0.249 | 0.752 | 0.918 | 0.971 |
|   3   | 0.233 | 1.843 | 7.568 | 0.328 | 0.589 | 0.847 | 0.940 |
|   4   | 0.334 | 2.997 | 9.356 | 0.430 | 0.419 | 0.721 | 0.883 |
|   5   | 0.363 | 3.308 | 9.882 | 0.459 | 0.387 | 0.683 | 0.864 |
|  avg  | 0.246 | 2.066 | 7.676 | 0.336 | 0.595 | 0.823 | 0.927 |

- **Summary:** $\text{DES}_1=$ 0.651, $\text{DES}_2=$ 0.326, $\text{DES}_3=$ 0.413




### ISO Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.185 | 1.390 | 6.621 | 0.273 | 0.705 | 0.899 | 0.962 |
|   2   | 0.208 | 1.606 | 7.064 | 0.299 | 0.651 | 0.879 | 0.952 |
|   3   | 0.254 | 2.063 | 7.846 | 0.349 | 0.547 | 0.830 | 0.932 |
|   4   | 0.310 | 2.680 | 8.778 | 0.405 | 0.447 | 0.758 | 0.902 |
|   5   | 0.357 | 3.265 | 9.713 | 0.453 | 0.390 | 0.691 | 0.868 |
|  avg  | 0.263 | 2.201 | 8.004 | 0.356 | 0.548 | 0.811 | 0.923 |

- **Summary:** $\text{DES}_1=$ 0.715, $\text{DES}_2=$ 0.357, $\text{DES}_3=$ 0.480




### Pixelate
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.118 | 0.932 | 4.911 | 0.195 | 0.870 | 0.958 | 0.980 |
|   2   | 0.120 | 0.947 | 4.977 | 0.197 | 0.867 | 0.956 | 0.980 |
|   3   | 0.128 | 1.025 | 5.140 | 0.204 | 0.853 | 0.952 | 0.978 |
|   4   | 0.145 | 1.197 | 5.509 | 0.221 | 0.822 | 0.940 | 0.974 |
|   5   | 0.154 | 1.256 | 5.716 | 0.231 | 0.805 | 0.934 | 0.972 |
|  avg  | 0.133 | 1.071 | 5.251 | 0.210 | 0.843 | 0.948 | 0.977 |

- **Summary:** $\text{DES}_1=$ 0.290, $\text{DES}_2=$ 0.145, $\text{DES}_3=$ 0.158




### JPEG Compression
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta < 1.25$ | $\delta < 1.25^2$ | $\delta < 1.25^3$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.130 | 1.046 | 5.172 | 0.208 | 0.848 | 0.950 | 0.978 |
|   2   | 0.140 | 1.157 | 5.361 | 0.218 | 0.829 | 0.944 | 0.976 |
|   3   | 0.150 | 1.258 | 5.536 | 0.227 | 0.809 | 0.938 | 0.973 |
|   4   | 0.179 | 1.548 | 6.021 | 0.255 | 0.752 | 0.918 | 0.966 |
|   5   | 0.219 | 2.035 | 6.706 | 0.291 | 0.677 | 0.888 | 0.955 |
|  avg  | 0.164 | 1.409 | 5.759 | 0.240 | 0.783 | 0.928 | 0.970 |

- **Summary:** $\text{DES}_1=$ 0.381, $\text{DES}_2=$ 0.190, $\text{DES}_3=$ 0.209


