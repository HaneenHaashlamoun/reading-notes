# Matplotlib

![v](https://pythonawesome.com/content/images/2021/08/cheatsheets-1.png)

Matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like Tkinter, wxPython, Qt, or GTK.

## pyplot
pyplot provides a convenient interface to the matplotlib object-oriented plotting library. It is modeled closely after Matlab(TM). Therefore, the majority of plotting commands in pyplot have Matlab(TM) analogs with similar arguments. Important commands are explained with interactive examples.

## Using defaults
![ma](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_1.png)

Matplotlib comes with a set of default settings that allow customizing all kinds of properties. You can control the defaults of almost every property in matplotlib: figure size and dpi, line width, color and style, axes, axis and grid properties, text and font properties and so on. While matplotlib defaults are rather good in most cases, you may want to modify some properties for specific cases.

## Instantiating defaults

In the script below, we've instantiated (and commented) all the figure settings that influence the appearance of the plot. The settings have been explicitly set to their default values, but now you can interactively play with the values to explore their affect (see Line properties and Line styles below).

## Changing colors and line widths

![Changing](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_3.png)

As a first step, we want to have the cosine in blue and the sine in red and a slightly thicker line for both of them. We'll also slightly alter the figure size to make it more horizontal.

>`plt.figure(figsize=(10,6), dpi=80)`

>`plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")`

>`plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")`

## Setting limits

- xlim() command
- ylim() command

Current limits of the figure are a bit too tight and we want to make some space in order to clearly see all data points.

## Setting ticks

![ticks](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_5.png)

Current ticks are not ideal because they do not show the interesting values (+/-π,+/-π/2) for sine and cosine. We'll change them such that they show only these values.

## Setting tick labels
![tick](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_6.png)

Ticks are now properly placed but their label is not very explicit. We could guess that 3.142 is π but it would be better to make it explicit. When we set tick values, we can also provide a corresponding label in the second argument list. Note that we'll use latex to allow for nice rendering of the label.

## Moving spines

![spines](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_7.png)

Spines are the lines connecting the axis tick marks and noting the boundaries of the data area. They can be placed at arbitrary positions and until now, they were on the border of the axis. We'll change that since we want to have them in the middle. Since there are four of them (top/bottom/left/right), we'll discard the top and right by setting their color to none and we'll move the bottom and left ones to coordinate 0 in data space coordinates.

## Adding a legend
Let's add a legend in the upper left corner. This only requires adding the keyword argument label (that will be used in the legend box) to the plot commands.

## Devil is in the details

![](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/exercice_10.png)

The tick labels are now hardly visible because of the blue and red lines. We can make them bigger and we can also adjust their properties such that they'll be rendered on a semi-transparent white background. This will allow us to see both the data and the labels.

## Contour Plots

![Contour](https://github.com/rougier/matplotlib-tutorial/raw/master/figures/contour_ex.png)

Starting from the code below, try to reproduce the graphic on the right taking care of the colormap (see Colormaps below).

```
import numpy as np
import matplotlib.pyplot as plt

def f(x,y): return (1-x/2+x**5+y**3)*np.exp(-x**2-y**2)

n = 256
x = np.linspace(-3,3,n)
y = np.linspace(-3,3,n)
X,Y = np.meshgrid(x,y)

plt.contourf(X, Y, f(X,Y), 8, alpha=.75, cmap='jet')
C = plt.contour(X, Y, f(X,Y), 8, colors='black', linewidth=.5)
plt.show()
```

    
© Haneen Hashlamoun

