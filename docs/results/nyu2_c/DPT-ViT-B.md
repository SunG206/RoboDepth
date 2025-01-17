<img src="https://github.com/ldkong1205/RoboDepth/blob/main/docs/figs/logo2.png" align="right" width="34%">

# RoboDepth Benchmark
The following metrics are consistently used in our benchmark:
- Absolute Relative Difference: $\text{Abs Rel} = \frac{1}{|D|}\sum_{pred\in D}\frac{|gt - pred|}{gt}$
- Accuracy: $\delta_t = \frac{1}{|D|}|\{\ pred\in D | \max{(\frac{gt}{pred}, \frac{pred}{gt})< 1.25^t}\}| \times 100\\%$
- Depth Estimation Score (DES):
  - $\text{DES}_1 = \text{Abs Rel} - \delta_1 + 1$ 
  - $\text{DES}_2 = \frac{\text{Abs Rel} - \delta_1 + 1}{2}$
  - $\text{DES}_3 = \frac{\text{Abs Rel}}{\delta_1}$


### DPT (ViT-Base)
### Clean
| $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| 0.135 | 0.079 | 0.413 | 0.153 | 0.863 | 0.979 | 0.995 | 0.054 | 10.903 |

- **Summary:** $\text{DES}_1=$ 0.272, $\text{DES}_2=$ 0.136, $\text{DES}_3=$ 0.156


### Brightness
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.134 | 0.079 | 0.412 | 0.153 | 0.864 | 0.978 | 0.995 | 0.053 | 11.058 |
|   2   | 0.132 | 0.078 | 0.413 | 0.153 | 0.864 | 0.977 | 0.995 | 0.053 | 11.319 |
|   3   | 0.131 | 0.078 | 0.418 | 0.154 | 0.861 | 0.977 | 0.995 | 0.053 | 11.687 |
|   4   | 0.131 | 0.080 | 0.431 | 0.157 | 0.855 | 0.976 | 0.994 | 0.054 | 12.204 |
|  avg  | 0.132 | 0.079 | 0.418 | 0.154 | 0.861 | 0.977 | 0.995 | 0.053 | 11.567 |

- **Summary:** $\text{DES}_1=$ 0.271, $\text{DES}_2=$ 0.135, $\text{DES}_3=$ 0.153


### Dark
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.148 | 0.096 | 0.453 | 0.170 | 0.831 | 0.966 | 0.990 | 0.059 | 12.741 |
|   2   | 0.150 | 0.101 | 0.466 | 0.174 | 0.821 | 0.961 | 0.989 | 0.060 | 13.368 |
|   3   | 0.158 | 0.115 | 0.501 | 0.185 | 0.798 | 0.951 | 0.986 | 0.063 | 14.592 |
|   4   | 0.182 | 0.154 | 0.594 | 0.215 | 0.736 | 0.925 | 0.978 | 0.074 | 17.255 |
|  avg  | 0.160 | 0.117 | 0.503 | 0.186 | 0.796 | 0.951 | 0.986 | 0.064 | 14.489 |

- **Summary:** $\text{DES}_1=$ 0.363, $\text{DES}_2=$ 0.182, $\text{DES}_3=$ 0.200


### Contrast
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.135 | 0.081 | 0.424 | 0.156 | 0.859 | 0.977 | 0.994 | 0.054 | 11.576 |
|   2   | 0.134 | 0.083 | 0.435 | 0.158 | 0.854 | 0.975 | 0.994 | 0.055 | 12.058 |
|   3   | 0.137 | 0.092 | 0.476 | 0.169 | 0.827 | 0.967 | 0.992 | 0.058 | 13.254 |
|   4   | 0.199 | 0.196 | 0.750 | 0.262 | 0.623 | 0.875 | 0.965 | 0.095 | 18.357 |
|  avg  | 0.151 | 0.113 | 0.521 | 0.186 | 0.791 | 0.948 | 0.986 | 0.065 | 13.811 |

- **Summary:** $\text{DES}_1=$ 0.361, $\text{DES}_2=$ 0.180, $\text{DES}_3=$ 0.191


### Defocus Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.139 | 0.082 | 0.427 | 0.158 | 0.852 | 0.977 | 0.994 | 0.055 | 11.262 |
|   2   | 0.140 | 0.085 | 0.436 | 0.160 | 0.847 | 0.975 | 0.994 | 0.056 | 11.599 |
|   3   | 0.144 | 0.091 | 0.462 | 0.167 | 0.833 | 0.971 | 0.993 | 0.058 | 12.538 |
|   4   | 0.150 | 0.101 | 0.496 | 0.179 | 0.805 | 0.964 | 0.990 | 0.062 | 13.709 |
|  avg  | 0.143 | 0.090 | 0.455 | 0.166 | 0.834 | 0.972 | 0.993 | 0.058 | 12.277 |

- **Summary:** $\text{DES}_1=$ 0.309, $\text{DES}_2=$ 0.154, $\text{DES}_3=$ 0.172


### Glass Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.141 | 0.084 | 0.427 | 0.159 | 0.850 | 0.976 | 0.994 | 0.056 | 11.258 |
|   2   | 0.143 | 0.087 | 0.436 | 0.162 | 0.842 | 0.974 | 0.993 | 0.057 | 11.671 |
|   3   | 0.155 | 0.106 | 0.494 | 0.181 | 0.803 | 0.959 | 0.990 | 0.062 | 13.910 |
|   4   | 0.161 | 0.118 | 0.536 | 0.192 | 0.781 | 0.949 | 0.987 | 0.066 | 15.118 |
|  avg  | 0.150 | 0.099 | 0.473 | 0.173 | 0.819 | 0.964 | 0.991 | 0.060 | 12.989 |

- **Summary:** $\text{DES}_1=$ 0.331, $\text{DES}_2=$ 0.166, $\text{DES}_3=$ 0.183


### Motion Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.138 | 0.083 | 0.424 | 0.157 | 0.855 | 0.977 | 0.995 | 0.055 | 11.212 |
|   2   | 0.140 | 0.086 | 0.434 | 0.160 | 0.849 | 0.975 | 0.994 | 0.056 | 11.647 |
|   3   | 0.146 | 0.096 | 0.462 | 0.168 | 0.830 | 0.970 | 0.992 | 0.058 | 12.590 |
|   4   | 0.155 | 0.111 | 0.501 | 0.182 | 0.805 | 0.960 | 0.989 | 0.063 | 14.006 |
|  avg  | 0.145 | 0.094 | 0.455 | 0.167 | 0.835 | 0.970 | 0.992 | 0.058 | 12.364 |

- **Summary:** $\text{DES}_1=$ 0.310, $\text{DES}_2=$ 0.155, $\text{DES}_3=$ 0.173


### Zoom Blur
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.153 | 0.114 | 0.525 | 0.191 | 0.794 | 0.950 | 0.986 | 0.065 | 15.336 |
|   2   | 0.168 | 0.143 | 0.606 | 0.220 | 0.740 | 0.926 | 0.976 | 0.074 | 17.603 |
|   3   | 0.182 | 0.170 | 0.672 | 0.244 | 0.694 | 0.903 | 0.967 | 0.083 | 18.899 |
|   4   | 0.205 | 0.211 | 0.765 | 0.281 | 0.627 | 0.867 | 0.951 | 0.098 | 20.803 |
|  avg  | 0.177 | 0.160 | 0.642 | 0.234 | 0.714 | 0.912 | 0.970 | 0.080 | 18.160 |

- **Summary:** $\text{DES}_1=$ 0.463, $\text{DES}_2=$ 0.232, $\text{DES}_3=$ 0.248


### Elastic Transform
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.133 | 0.078 | 0.414 | 0.153 | 0.861 | 0.978 | 0.995 | 0.053 | 11.256 |
|   2   | 0.132 | 0.078 | 0.418 | 0.154 | 0.860 | 0.976 | 0.995 | 0.053 | 11.601 |
|   3   | 0.132 | 0.080 | 0.431 | 0.157 | 0.853 | 0.974 | 0.994 | 0.053 | 12.189 |
|   4   | 0.133 | 0.083 | 0.446 | 0.161 | 0.846 | 0.971 | 0.994 | 0.054 | 12.724 |
|  avg  | 0.133 | 0.080 | 0.427 | 0.156 | 0.855 | 0.975 | 0.994 | 0.053 | 11.942 |

- **Summary:** $\text{DES}_1=$ 0.278, $\text{DES}_2=$ 0.139, $\text{DES}_3=$ 0.155


### Color Quant
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.136 | 0.080 | 0.415 | 0.154 | 0.862 | 0.978 | 0.994 | 0.054 | 11.050 |
|   2   | 0.137 | 0.082 | 0.423 | 0.157 | 0.855 | 0.975 | 0.994 | 0.055 | 11.414 |
|   3   | 0.146 | 0.093 | 0.457 | 0.169 | 0.827 | 0.967 | 0.993 | 0.059 | 12.768 |
|   4   | 0.176 | 0.137 | 0.578 | 0.214 | 0.729 | 0.932 | 0.984 | 0.074 | 16.723 |
|  avg  | 0.149 | 0.098 | 0.468 | 0.174 | 0.818 | 0.963 | 0.991 | 0.061 | 12.989 |

- **Summary:** $\text{DES}_1=$ 0.330, $\text{DES}_2=$ 0.165, $\text{DES}_3=$ 0.182


### Gaussian Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.137 | 0.089 | 0.443 | 0.162 | 0.847 | 0.968 | 0.990 | 0.055 | 12.728 |
|   2   | 0.149 | 0.106 | 0.487 | 0.177 | 0.816 | 0.958 | 0.987 | 0.060 | 14.163 |
|   3   | 0.175 | 0.143 | 0.574 | 0.207 | 0.752 | 0.937 | 0.980 | 0.071 | 16.618 |
|   4   | 0.212 | 0.200 | 0.709 | 0.253 | 0.654 | 0.893 | 0.968 | 0.089 | 19.988 |
|  avg  | 0.168 | 0.135 | 0.553 | 0.200 | 0.767 | 0.939 | 0.981 | 0.069 | 15.874 |

- **Summary:** $\text{DES}_1=$ 0.401, $\text{DES}_2=$ 0.200, $\text{DES}_3=$ 0.219


### Impulse Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.141 | 0.094 | 0.464 | 0.169 | 0.831 | 0.964 | 0.991 | 0.058 | 13.487 |
|   2   | 0.157 | 0.116 | 0.524 | 0.189 | 0.790 | 0.950 | 0.987 | 0.064 | 15.175 |
|   3   | 0.174 | 0.142 | 0.582 | 0.209 | 0.747 | 0.934 | 0.981 | 0.072 | 16.836 |
|   4   | 0.220 | 0.215 | 0.751 | 0.266 | 0.618 | 0.880 | 0.963 | 0.095 | 20.785 |
|  avg  | 0.173 | 0.142 | 0.580 | 0.208 | 0.746 | 0.932 | 0.980 | 0.072 | 16.571 |

- **Summary:** $\text{DES}_1=$ 0.427, $\text{DES}_2=$ 0.213, $\text{DES}_3=$ 0.232


### Shot Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.133 | 0.085 | 0.437 | 0.158 | 0.855 | 0.971 | 0.991 | 0.054 | 12.426 |
|   2   | 0.143 | 0.100 | 0.484 | 0.173 | 0.825 | 0.962 | 0.989 | 0.059 | 13.829 |
|   3   | 0.164 | 0.128 | 0.556 | 0.197 | 0.775 | 0.944 | 0.984 | 0.067 | 15.834 |
|   4   | 0.207 | 0.196 | 0.710 | 0.249 | 0.661 | 0.896 | 0.968 | 0.087 | 19.602 |
|  avg  | 0.162 | 0.127 | 0.547 | 0.194 | 0.779 | 0.943 | 0.983 | 0.067 | 15.423 |

- **Summary:** $\text{DES}_1=$ 0.383, $\text{DES}_2=$ 0.191, $\text{DES}_3=$ 0.208


### ISO Noise
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.150 | 0.109 | 0.503 | 0.180 | 0.811 | 0.956 | 0.987 | 0.061 | 14.472 |
|   2   | 0.156 | 0.117 | 0.523 | 0.188 | 0.795 | 0.951 | 0.986 | 0.064 | 15.072 |
|   3   | 0.170 | 0.137 | 0.567 | 0.203 | 0.763 | 0.939 | 0.982 | 0.070 | 16.362 |
|   4   | 0.192 | 0.168 | 0.638 | 0.228 | 0.707 | 0.918 | 0.975 | 0.079 | 18.167 |
|  avg  | 0.167 | 0.133 | 0.558 | 0.200 | 0.769 | 0.941 | 0.982 | 0.069 | 16.018 |

- **Summary:** $\text{DES}_1=$ 0.398, $\text{DES}_2=$ 0.199, $\text{DES}_3=$ 0.217


### Pixelate
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.142 | 0.084 | 0.426 | 0.159 | 0.850 | 0.977 | 0.995 | 0.056 | 11.037 |
|   2   | 0.138 | 0.082 | 0.420 | 0.156 | 0.857 | 0.977 | 0.994 | 0.055 | 11.085 |
|   3   | 0.163 | 0.105 | 0.472 | 0.176 | 0.807 | 0.971 | 0.993 | 0.064 | 11.488 |
|   4   | 0.189 | 0.133 | 0.530 | 0.197 | 0.752 | 0.960 | 0.991 | 0.072 | 12.320 |
|  avg  | 0.158 | 0.101 | 0.462 | 0.172 | 0.816 | 0.971 | 0.993 | 0.062 | 11.482 |

- **Summary:** $\text{DES}_1=$ 0.341, $\text{DES}_2=$ 0.171, $\text{DES}_3=$ 0.194


### JPEG Compression
| Level | $\text{Abs Rel}$ | $\text{Sq Rel}$ | $\text{RMSE}$ | $\text{RMSE log}$ | $\delta_{1}$ | $\delta_{2}$ | $\delta_{3}$ | $\text{log10}$ | $\text{silog}$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|   1   | 0.150 | 0.091 | 0.444 | 0.166 | 0.837 | 0.975 | 0.994 | 0.059 | 11.355 |
|   2   | 0.157 | 0.099 | 0.460 | 0.172 | 0.821 | 0.973 | 0.993 | 0.061 | 11.695 |
|   3   | 0.160 | 0.103 | 0.471 | 0.176 | 0.811 | 0.971 | 0.993 | 0.063 | 12.019 |
|   4   | 0.172 | 0.118 | 0.509 | 0.189 | 0.777 | 0.961 | 0.992 | 0.068 | 13.254 |
|  avg  | 0.160 | 0.103 | 0.471 | 0.176 | 0.812 | 0.970 | 0.993 | 0.063 | 12.081 |

- **Summary:** $\text{DES}_1=$ 0.348, $\text{DES}_2=$ 0.174, $\text{DES}_3=$ 0.197

