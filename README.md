# tex-commands
Some useful commands for LaTex

# Mathematical Symbols:

**NOTE:** always use the `$`(dollar) sign before and afer the expression when you are writing a mathematical expression in LaTex

#### Without $:
\geq

$\geq$ - the above statement but with the dollar sign added on both sides of the expression

----

## Commands:

- `$a^b$` is $a^b$ (exponents)
- `$a_b$` is $a_b$ (subscript.. can be used to write chemical formulaes like $Ch_6$
- `\frac{first arg}{second arg}` is $\frac{first \space arg}{second \space arg}$ (fractions.. replace first arg and second arg by your expression)
- `\neq` is $\neq$ (not equals to.. can be used when a != b)
- `\int` is $\int$ (`$\int$`) or Integral Sign
- `\lambda` is $\lambda$ (`$lambda`) or Lambda
- `\infty` is $\infty$ or Infitnity

----

### Misc Signs:
- `\circ` is used to make a circle or degree symbol such as  $180^{\circ}$ (`$180^{\circ}$`)
- `\square` is used to make a square.. like: $\square$
- `\space` is used to add spacing inside a mathematical expression.. $\int(x) \space + 1$ (`$\int(x) \space + 1$`)

# Text Coloring:
**NOTE:** in order for colorization you must add package `xcolor`

### Adding It:
```latex
\usepackage{xcolor}
```

---

### Usage:
The available colors are `black, blue, brown, cyan, darkgray, gray, green, lightgray, lime, magenta, olive, orange, pink, purple, red, teal, violet, white, yellow`

```latex
\color{your_color}This is a colored text\color{white} % white is the FG here
```

> ### Demo:

> ##### Code: 
```latex
\usepackage {xcolor}
\color{red}This is a red text\color{white}
\color{orange}This is an orange text\color{white}
\color{yellow}This is a yellow text\color{white}
\color{green}This is a green text\color{white}
\color{blue}This is a blue text\color{white}
\color{purple}This is a purple text\color{white}
```
> ##### Preview:
$\color{red}This \space is \space a \space red \space text\color{white}$

$\color{orange}This \space is \space an \space orange \space text\color{white}$

$\color{yellow}This \space is \space a \space yellow \space text\color{white}$

$\color{green}This \space is \space a \space green \space text\color{white}$

$\color{blue}This \space is \space a \space blue \space text\color{white}$

$\color{purple}This \space is \space a \space purple \space text\color{white}$

# Preamble
Your preamble is where you setup your LaTeX envioment and packages, often its imported from a spereate file called `preamble.tex` using the `\input{}` command.

## Vectors
Creating vectors in LaTeX can be a hassle, use the folloing macros to make the process faster. This code introduces two new commands `\vec{}` and `\pvec{}`, `\vec{ab}` creates an arrow above your variable name like $\overrightarrow{ab}$ and `\pvec{}` creates a vector column such as `\pvec{3 \\ 4 \\ 1}` 

![image](https://github.com/logicguy1/tex-commands/assets/56993729/ac1e5582-1560-4a0c-b7f4-17b5044c5ec8)

Add the following code to your preamble after importing the `amsmath` (the amarecan mathmatical assosiation math package)
```latex
% Vectors
\renewcommand{\vec}[1]{\overrightarrow{#1}}

% Custom command for display vectors using pmatrix, use \pvec{1 \\ 2 \\ 3}
\newcommand{\pvec}[1]{%
  \begin{pmatrix}
  #1
  \end{pmatrix}%
}
```

# Contributing:
On this README.md you may add an section or fix some mistakes
