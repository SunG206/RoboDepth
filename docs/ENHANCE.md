<img src="https://github.com/ldkong1205/RoboDepth/blob/main/docs/figs/logo2.png" align="right" width="34%">

# Robustness Enhancement

### Outline
- [Train & Test on Clean Data](#train--test-on-clean-data)
  - [Train on Clean, Test on Clean](#train-on-clean-test-on-clean)
  - [Train on Corruptions, Test on Clean](#train-on-corruptions-test-on-clean)
- [Train & Test on Corrupted Data](#train--test-on-corrupted-data)
  - [Train on Clean, Test on Corruptions](#train-on-clean-test-on-corruptions)
  - [Train on Corruptions, Test on Corruptions](#train-on-corruptions-test-on-corruptions)


## Train & Test on Clean Data

### Train on Clean, Test on Clean
> **Model:** MonoDepth2, **Backbone:** ResNet-18

| Train | Abs Rel | Sq Rel | RMSE | RMSE log | a1 | a2 | a3 | DEE | mCE (%) | mRR (%) |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Clean | 0.115	| 0.905	| 4.864 |	0.193	| 0.877 |	0.959	| 0.981 | 0.119 | 100.00 | 84.46 |


### Train on Corruptions, Test on Clean
> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 1.0

| Train | Abs Rel | Sq Rel | RMSE | RMSE log | a1 | a2 | a3 | DEE | mCE (%) | mRR (%) |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   | 0.120 | 0.951 | 4.953 | 0.197 | 0.866 | 0.956 | 0.980 | 0.127 | 101.98 | 85.06 |
| Dark     | 0.130 | 1.082 | 5.251 | 0.206 | 0.848 | 0.952 | 0.979 | 0.141 | 111.11 | 84.90 |
| Fog      | 0.119 | 0.883 | 4.972 | 0.197 | 0.865 | 0.957 | 0.981 | 0.127 | 106.54 | 82.91 |
| Snow     | 0.123 | 0.920 | 4.987 | 0.200 | 0.859 | 0.955 | 0.980 | 0.132 | 102.07 | 86.35 |
| Contrast | 0.119 | 0.899 | 4.994 | 0.199 | 0.865 | 0.955 | 0.980 | 0.127 | 111.38 | 81.49 |
| Defocus  | 0.148 | 1.138 | 6.238 | 0.245 | 0.796 | 0.925 | 0.966 | 0.176 | 114.57 | 85.80 |
| Motion   | 0.124 | 0.909 | 5.067 | 0.202 | 0.855 | 0.952 | 0.979 | 0.135 | 100.78 | 85.87 |
| Zoom     | 0.160 | 1.191 | 6.023 | 0.244 | 0.768 | 0.923 | 0.969 | 0.196 | 132.44 | 82.84 |
| Elastic  | 0.122 | 0.950 | 5.015 | 0.200 | 0.865 | 0.955 | 0.979 | 0.129 | 110.40 | 81.94 |
| Gaussian | 0.126 | 1.023 | 5.091 | 0.203 | 0.856 | 0.953 | 0.979 | 0.135 | 94.26  | 90.05 |
| Impulse  | 0.126 | 1.025 | 5.118 | 0.203 | 0.857 | 0.953 | 0.979 | 0.135 | 94.16  | 90.06 |
| Shot     | 0.124 | 0.988 | 5.028 | 0.200 | 0.860 | 0.955 | 0.980 | 0.132 | 90.12  | 90.64 |
| ISO      | 0.127 | 0.984 | 5.055 | 0.203 | 0.853 | 0.953 | 0.980 | 0.137 | 102.64 | 87.93 |
| Pixelate | 0.122 | 0.938 | 4.978 | 0.199 | 0.862 | 0.955 | 0.980 | 0.130 | 106.78 | 83.35 |
| JPEG     | 0.125 | 0.973 | 5.034 | 0.202 | 0.859 | 0.954 | 0.979 | 0.133 | 106.33 | 85.06 |
||
| Combo (W&L) | 0.120 | 0.924 | 4.914 | 0.196 | 0.866 | 0.957 | 0.980 | 0.127 | 83.75 | 91.93 |
| Combo (S&M) | 0.128 | 1.009 | 5.132 | 0.205 | 0.850 | 0.952 | 0.979 | 0.139 | 93.94 | 89.15 |
| Combo (D&P) | 0.124 | 0.979 | 5.064 | 0.201 | 0.858 | 0.954 | 0.980 | 0.133 | 90.44 | 91.02 |
||
| Combo (All) | 0.124 | 0.963 | 5.040 | 0.199 | 0.860 | 0.955 | 0.980 | 0.132 | 71.25 | 96.75 |

> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 0.5

| Train | Abs Rel | Sq Rel | RMSE | RMSE log | a1 | a2 | a3 | DEE | mCE (%) | mRR (%) |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   | 0.119 | 0.935 | 4.916 | 0.195 | 0.871 | 0.957 | 0.980 | 0.124 | 99.59 | 85.60 |
| Dark     | 0.121 | 0.951 | 4.947 | 0.196 | 0.866 | 0.957 | 0.981 | 0.128 | 98.17 | 86.18 |
| Fog      | 0.116 | 0.879 | 4.865 | 0.193 | 0.872 | 0.959 | 0.981 | 0.122 | 99.20 | 85.17 |
| Snow     | 0.120 | 0.916 | 4.923 | 0.197 | 0.868 | 0.957 | 0.980 | 0.126 | 98.40 | 86.71 |
| Contrast | 0.118 | 0.928 | 4.929 | 0.194 | 0.870 | 0.958 | 0.981 | 0.124 | 98.90 | 85.76 |
| Defocus  | 0.123 | 0.964 | 5.002 | 0.199 | 0.862 | 0.955 | 0.980 | 0.131 | 90.45 | 89.02 |
| Motion   | 0.120 | 0.908 | 4.897 | 0.196 | 0.865 | 0.957 | 0.980 | 0.128 | 92.24 | 88.08 |
| Zoom     | 0.126 | 0.965 | 4.986 | 0.203 | 0.854 | 0.954 | 0.980 | 0.136 | 96.18 | 88.28 |
| Elastic  | 0.119 | 0.904 | 4.909 | 0.197 | 0.869 | 0.958 | 0.980 | 0.125 | 97.44 | 85.92 |
| Gaussian | 0.123 | 0.980 | 5.031 | 0.200 | 0.863 | 0.955 | 0.980 | 0.130 | 86.81 | 91.60 |
| Impulse  | 0.124 | 0.985 | 5.026 | 0.200 | 0.860 | 0.955 | 0.980 | 0.132 | 92.80 | 90.05 |
| Shot     | 0.123 | 0.989 | 5.015 | 0.201 | 0.864 | 0.955 | 0.979 | 0.130 | 90.09 | 90.57 |
| ISO      | 0.123 | 0.996 | 5.002 | 0.198 | 0.865 | 0.956 | 0.980 | 0.129 | 91.02 | 90.25 |
| Pixelate | 0.119 | 0.912 | 4.895 | 0.197 | 0.868 | 0.958 | 0.981 | 0.126 | 100.89 | 85.02 |
| JPEG     | 0.121 | 0.945 | 4.983 | 0.199 | 0.865 | 0.956 | 0.980 | 0.128 | 104.61 | 84.63 |
||
| Combo (W&L) | 0.120 | 0.945 | 4.925 | 0.195 | 0.868 | 0.957 | 0.980 | 0.126 | 83.15 | 92.08 |
| Combo (S&M) | 0.122 | 0.961 | 5.026 | 0.199 | 0.864 | 0.956 | 0.980 | 0.129 | 88.61 | 89.51 |
| Combo (D&P) | 0.120 | 0.912 | 4.951 | 0.198 | 0.865 | 0.956 | 0.980 | 0.128 | 85.05 | 91.78 |
||
| Combo (All) | 0.118 | 0.912 | 4.935 | 0.195 | 0.867 | 0.957 | 0.981 | 0.126 | 72.36 | 95.64 |

> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 0.25

| Train | Abs Rel | Sq Rel | RMSE | RMSE log | a1 | a2 | a3 | DEE | mCE (%) | mRR (%) |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   | 0.118 | 0.933 | 4.906 | 0.195 | 0.871 | 0.958 | 0.980 | 0.123 | 98.43 | 85.78 |
| Dark     | 0.119 | 0.968 | 4.920 | 0.195 | 0.869 | 0.958 | 0.980 | 0.125 | 98.03 | 86.26 |
| Fog      | 0.118 | 0.936 | 4.897 | 0.194 | 0.871 | 0.958 | 0.981 | 0.123 | 98.86 | 85.32 |
| Snow     | 0.119 | 0.922 | 4.897 | 0.196 | 0.868 | 0.957 | 0.980 | 0.126 | 97.72 | 86.87 |
| Contrast | 0.118 | 0.947 | 4.970 | 0.194 | 0.871 | 0.958 | 0.981 | 0.123 | 97.56 | 85.84 |
| Defocus  | 0.119 | 0.927 | 4.915 | 0.196 | 0.868 | 0.958 | 0.980 | 0.126 | 92.12 | 87.89 |
| Motion   | 0.120 | 0.946 | 4.957 | 0.197 | 0.867 | 0.957 | 0.980 | 0.127 | 92.80 | 87.76 |
| Zoom     | 0.123 | 0.973 | 4.980 | 0.199 | 0.863 | 0.957 | 0.980 | 0.130 | 97.21 | 86.88 |
| Elastic  | 0.120 | 0.951 | 4.958 | 0.198 | 0.868 | 0.956 | 0.980 | 0.126 | 99.81 | 85.53 |
| Gaussian | 0.122 | 0.962 | 4.930 | 0.199 | 0.865 | 0.956 | 0.980 | 0.129 | 86.94 | 91.44 |
| Impulse  | 0.121 | 0.977 | 4.956 | 0.197 | 0.867 | 0.957 | 0.980 | 0.127 | 88.18 | 90.48 |
| Shot     | 0.120 | 0.918 | 4.938 | 0.198 | 0.866 | 0.956 | 0.980 | 0.127 | 88.90 | 90.31 |
| ISO      | 0.121 | 0.931 | 4.974 | 0.199 | 0.866 | 0.955 | 0.980 | 0.128 | 86.96 | 91.23 |
| Pixelate | 0.119 | 0.917 | 4.920 | 0.197 | 0.868 | 0.957 | 0.980 | 0.126 | 99.74 | 85.39 |
| JPEG     | 0.121 | 0.931 | 4.955 | 0.199 | 0.866 | 0.956 | 0.980 | 0.128 | 102.96 | 84.77 |
||
| Combo (W&L) | 0.118 | 0.925 | 4.882 | 0.194 | 0.870 | 0.958 | 0.981 | 0.124 | 83.21 | 91.65 |
| Combo (S&M) | 0.120 | 0.936 | 4.925 | 0.196 | 0.866 | 0.956 | 0.980 | 0.127 | 92.57 | 87.77 |
| Combo (D&P) | 0.118 | 0.904 | 4.920 | 0.197 | 0.868 | 0.956 | 0.980 | 0.125 | 84.51 | 91.52 |
||
| Combo (All) | 0.117 | 0.907 | 4.861 | 0.195 | 0.872 | 0.958 | 0.980 | 0.122 | 77.50 | 94.02 |


## Train & Test on Corrupted Data

### Train on Clean, Test on Corruptions
> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Metric:** Abs Rel

| Train | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Clean |.120|.216|.137|.217|.414|.156|.191|.191|.175|.170|.121|.162|.285|.285|.253|.282|.133|.167|



### Train on Corruptions, Test on Corruptions
> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 1.0, **Metric:** Abs Rel

| Train | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   |.118|.223|.139|.218|.377|.164|.222|.218|.190|.172|.127|.167|.269|.285|.261|.271|.136|.160|
| Dark     |.144|.159|.193|.226|.356|.235|.243|.224|.210|.191|.135|.156|.274|.288|.249|.258|.144|.155|
| Fog      |.127|.230|.122|.211|.389|.133|.234|.206|.178|.167|.124|.170|.327|.350|.309|.348|.137|.192|
| Snow     |.130|.249|.145|.166|.134|.213|.198|.175|.166|.168|.127|.169|.318|.331|.288|.320|.129|.180|
| Contrast |.123|.278|.126|.228|.417|.123|.259|.224|.225|.174|.127|.181|.330|.335|.308|.343|.137|.181|
| Defocus  |.155|.282|.153|.233|.387|.173|.132|.158|.165|.158|.141|.207|.349|.369|.337|.363|.136|.180|
| Motion   |.135|.262|.147|.221|.313|.167|.151|.158|.129|.149|.126|.168|.321|.318|.294|.324|.131|.171|
| Zoom     |.178|.348|.179|.347|.366|.201|.181|.205|.153|.140|.160|.220|.407|.397|.390|.411|.163|.202|
| Elastic  |.126|.238|.145|.216|.394|.195|.218|.195|.203|.176|.124|.166|.347|.361|.326|.372|.131|.162|
| Gaussian |.131|.184|.177|.215|.395|.246|.207|.190|.183|.171|.129|.159|.166|.172|.145|.141|.132|.140|
| Impulse  |.133|.197|.190|.221|.397|.254|.182|.170|.169|.168|.130|.160|.189|.147|.156|.165|.130|.141|
| Shot     |.129|.181|.164|.204|.381|.217|.192|.173|.170|.175|.128|.159|.175|.182|.145|.148|.131|.142|
| ISO      |.138|.181|.195|.227|.407|.269|.271|.180|.227|.198|.130|.157|.188|.199|.161|.151|.133|.138|
| Pixelate |.129|.232|.144|.230|.453|.173|.207|.193|.193|.173|.124|.177|.308|.316|.283|.308|.127|.159|
| JPEG     |.131|.201|.160|.205|.397|.227|.277|.217|.208|.187|.130|.165|.251|.255|.224|.238|.133|.134|
||
| Combo (W&L) |.121|.155|.126|.152|.141|.130|.231|.192|.175|.175|.124|.154|.207|.228|.193|.184|.129|.159|
| Combo (S&M) |.137|.227|.150|.216|.301|.170|.142|.154|.137|.142|.130|.168|.267|.267|.239|.250|.134|.175|
| Combo (D&P) |.129|.187|.169|.210|.399|.248|.198|.175|.181|.175|.128|.153|.148|.140|.133|.138|.128|.134|
||
| Combo (All) |.125|.155|.133|.167|.153|.136|.148|.158|.144|.151|.127|.150|.147|.144|.135|.140|.129|.138|

> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 0.5, **Metric:** Abs Rel

| Train | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   |.119|.202|.138|.202|.397|.160|.245|.225|.205|.167|.124|.156|.245|.255|.235|.246|.134|.159|
| Dark     |.125|.162|.138|.181|.385|.167|.225|.212|.179|.175|.126|.155|.282|.299|.256|.272|.132|.149|
| Fog      |.120|.204|.120|.204|.379|.130|.226|.229|.211|.172|.121|.156|.266|.274|.241|.264|.134|.175|
| Snow     |.128|.229|.145|.166|.135|.201|.184|.172|.162|.172|.124|.165|.317|.318|.282|.321|.128|.170|
| Contrast |.122|.207|.128|.219|.385|.126|.245|.225|.180|.173|.124|.160|.250|.248|.229|.246|.136|.184|
| Defocus  |.129|.213|.141|.184|.383|.161|.136|.148|.153|.160|.125|.164|.258|.255|.217|.240|.128|.158|
| Motion   |.127|.224|.145|.219|.364|.160|.150|.159|.131|.153|.125|.161|.266|.260|.235|.250|.129|.171|
| Zoom     |.133|.224|.150|.220|.328|.172|.168|.184|.144|.139|.131|.164|.252|.251|.226|.238|.140|.181|
| Elastic  |.123|.216|.139|.203|.383|.159|.177|.176|.169|.165|.122|.169|.289|.287|.250|.281|.127|.159|
| Gaussian |.127|.184|.159|.193|.348|.189|.194|.179|.180|.179|.127|.162|.152|.156|.136|.137|.131|.139|
| Impulse  |.131|.203|.166|.203|.374|.228|.206|.182|.175|.170|.128|.167|.183|.144|.153|.163|.130|.143|
| Shot     |.129|.184|.164|.200|.377|.215|.206|.179|.170|.169|.127|.159|.167|.168|.141|.146|.132|.148|
| ISO      |.130|.177|.173|.210|.405|.252|.203|.178|.170|.165|.126|.156|.161|.170|.139|.139|.129|.140|
| Pixelate |.125|.227|.142|.215|.406|.168|.190|.172|.197|.171|.122|.164|.288|.285|.257|.284|.124|.158|
| JPEG     |.126|.199|.156|.234|.411|.219|.246|.216|.193|.185|.126|.155|.268|.269|.236|.257|.129|.132|
||
| Combo (W&L) |.120|.157|.125|.158|.144|.129|.221|.191|.174|.169|.125|.155|.208|.221|.184|.180|.131|.164|
| Combo (S&M) |.127|.209|.140|.203|.327|.157|.142|.154|.135|.142|.125|.163|.248|.244|.220|.233|.130|.163|
| Combo (D&P) |.127|.175|.156|.200|.387|.199|.178|.174|.168|.167|.124|.154|.148|.142|.133|.137|.125|.132|
||
| Combo (All) |.121|.156|.128|.172|.169|.130|.143|.155|.192|.152|.122|.147|.147|.143|.132|.136|.125|.135|

> **Model:** MonoDepth2, **Backbone:** ResNet-18, **Corrupt Probability:** 0.25, **Metric:** Abs Rel

| Train | Bright | Dark | Fog | Frost | Snow | Contrast | Defocus | Glass | Motion | Zoom | Elastic| Quant| Gaussian | Impulse | Shot | ISO | Pixelate | JPEG |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| Bright   |.119|.199|.135|.211|.413|.162|.236|.222|.187|.171|.123|.154|.252|.258|.229|.235|.133|.162|
| Dark     |.122|.156|.134|.185|.361|.160|.258|.214|.209|.177|.125|.157|.262|.274|.240|.247|.132|.155|
| Fog      |.122|.216|.124|.194|.345|.134|.232|.208|.186|.171|.124|.157|.285|.290|.256|.279|.136|.173|
| Snow     |.126|.228|.140|.165|.136|.188|.204|.182|.167|.170|.124|.165|.307|.317|.281|.311|.129|.163|
| Contrast |.122|.212|.128|.216|.387|.126|.216|.194|.191|.173|.123|.167|.259|.258|.233|.257|.135|.180|
| Defocus  |.124|.207|.139|.212|.360|.175|.137|.154|.156|.161|.124|.158|.270|.263|.235|.252|.126|.163|
| Motion   |.126|.214|.139|.206|.346|.169|.137|.155|.156|.162|.124|.160|.278|.270|.243|.263|.127|.163|
| Zoom     |.129|.225|.148|.228|.351|.169|.170|.178|.146|.142|.129|.161|.272|.274|.249|.263|.140|.181|
| Elastic  |.127|.228|.144|.222|.385|.178|.181|.172|.172|.166|.124|.168|.288|.283|.259|.280|.133|.164|
| Gaussian |.128|.184|.152|.200|.380|.205|.194|.180|.173|.169|.126|.157|.147|.147|.134|.137|.131|.145|
| Impulse  |.126|.194|.154|.203|.410|.200|.188|.174|.170|.164|.125|.160|.179|.144|.151|.162|.129|.144|
| Shot     |.124|.182|.150|.206|.408|.181|.206|.187|.177|.177|.126|.158|.170|.169|.141|.148|.131|.149|
| ISO      |.127|.173|.151|.193|.357|.183|.211|.182|.182|.166|.126|.156|.159|.161|.136|.140|.129|.144|
| Pixelate |.124|.215|.142|.214|.397|.169|.188|.183|.176|.165|.124|.163|.283|.285|.254|.277|.125|.160|
| JPEG     |.126|.215|.146|.231|.426|.182|.259|.201|.184|.175|.126|.155|.276|.272|.245|.267|.130|.134|
||
| Combo (W&L) |.120|.156|.125|.156|.144|.130|.201|.187|.168|.168|.124|.155|.217|.228|.198|.192|.130|.159|
| Combo (S&M) |.127|.223|.143|.220|.399|.170|.142|.157|.137|.148|.123|.163|.265|.253|.236|.251|.130|.167|
| Combo (D&P) |.123|.177|.148|.192|.376|.177|.188|.178|.176|.169|.123|.157|.150|.142|.134|.139|.124|.133|
||
| Combo (All) |.120|.155|.127|.166|.153|.135|.148|.154|.383|.171|.123|.144|.147|.144|.133|.138|.126|.137|

