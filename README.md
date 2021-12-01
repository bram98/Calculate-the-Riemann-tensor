# Calculate-the-Riemann-tensor
A Mathematica notebook that allows you to provide a symbolic metric tensor and from that it will compute the Christoffel symbols, the Riemann tensor, the lowered Riemann tensor, the Ricci tensor and the Ricci scalar. Great for all your GR needs

## How to use
First input what coordinates you want to use by modyfing this line
```
(* change X to be a list of your variables *)
X = {t, r, \[Theta], \[Phi]};
```
Make sure these coordinates do not coincide with one of the dummy variables <img src="https://latex.codecogs.com/svg.image?\rho&space;,\sigma&space;,\mu&space;,\nu,&space;\lambda" title="\rho ,\sigma ,\mu ,\nu, \lambda" />. If you do want to use one of these make sure you replace those dummy variables in the code below with other variables.

Next you can decide if you want to show only independent components by changing this line to `True` or `False`
```
(* if you set this to true components that are the same because of 
symmetry will not be displayed *)
showOnlyIndependentComponents = True;
```
Then you can edit the metric tensor `g` to provide input. 

<img src="https://latex.codecogs.com/svg.image?g=\left(\begin{array}{cccc}&space;1&space;&&space;0&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;-\frac{a(t)^2}{1-k&space;r^2}&space;&&space;0&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;-a(t)^2&space;r^2&space;&&space;0&space;\\&space;0&space;&&space;0&space;&&space;0&space;&&space;-a(t)^2&space;r^2&space;&space;\sin&space;^2(\theta&space;)&space;\\\end{array}\right)" title="g=\left(\begin{array}{cccc} 1 & 0 & 0 & 0 \\ 0 & -\frac{a(t)^2}{1-k r^2} & 0 & 0 \\ 0 & 0 & -a(t)^2 r^2 & 0 \\ 0 & 0 & 0 & -a(t)^2 r^2 \sin ^2(\theta ) \\\end{array}\right)" />

The coordinates are in the same order as the variable `X` and the metric 
tensor is assumed to have lower indices. For example if `X[[1]]==t` and `X[[2]]==r` (by default) then `g[[1,2]]` corresponds to <img src="https://latex.codecogs.com/svg.image?g_{tr}" title="g_{tr}" />.
The variable `gup` is the inverse metric tensor and corresponds to <img src="https://latex.codecogs.com/svg.image?g^{\mu\nu}" title="g^{\mu\nu}" />

You can now run the rest of the notebook and it will show you to the non-zero components of the Christoffel symbols, the Riemann tensor, the lowered Riemann tensor, the Ricci tensor and the Ricci scalar.
