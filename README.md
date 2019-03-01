# Improve efficiency
## Themes ([ZHIHU][1])
To protect your eyes, it's time to change a dark theme. In order to do this, we need
### Install
```{bash}  
#Install the themes packages 
pip install jupyterthemes
```
### Look the themes list
```
jt -l
```
### Change your themes
```
# jt -t (the theme you like)
# For example
jt -t onedork  -N -T
# -N -T allows us to show the toolbar after changing the theme
```
![Onedork](./images/onedork.png)
### Change it back
```
jt -r
# then restart your jupyter notebook
```

## Use jupyter as excel ([ZHIHU][2])
We need a package named Qgrid.
### Install
By pip:
```
pip install qgrid
jupyter nbextension enable --py --sys-prefix qgrid
# only required if you have not enabled the ipywidgets nbextension yet
jupyter nbextension enable --py --sys-prefix widgetsnbextension
```
By conda:
```
# only required if you have not added conda-forge to your channels yet
conda config --add channels conda-forge
conda install qgrid
```
### Example of using qgrid
```{python}
import qgrid
qgrid.show_grid(your_data_name)
# data type: data.frame
```
![Qgrid](./images/qgrid.png)

## Other useful tools
...continue to update 

[1]: https://zhuanlan.zhihu.com/p/46242116
[2]: https://www.zhihu.com/question/59392251/answer/560977151
