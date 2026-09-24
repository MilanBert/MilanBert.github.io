# Milan Bertolutti - GitHub Website

## What is this repository?

This repository is for my personal github pages website that has some information about me and blog posts that have some data analysis.

## Installation instructions

### What you need

Install these first. The versions listed are the ones used to build the site:

- quarto | Version used 1.10.18
- uv | Version used: 0.12.5 
- R | Version used: 4.6.1

### Command workflow

1. Clone the repository and move into it:

```bash
git clone https://github.com/MilanBert/MilanBert.github.io.git
cd MilanBert.github.io
```

2. Install the Python packages from uv.lock into .venv (in the terminal, from the project folder):

```bash
uv sync
```

3. Install the R packages from renv.lock. Start R from the project folder (type R in the terminal, or open the folder in RStudio):

```bash
R
```

```r
renv::restore()
```
If you would like to install the packages accept with `Y`s

optionally type `q()` to quit R when it finishes. no need to save the workspace image.

4. Build the site (in the terminal, from the project folder):

```bash
uv run quarto render
```

5. Preview the site

The built site is written to the docs/ folder, which GitHub Pages publishes from. To view it locally, run this in the terminal from the project folder:

```bash
uv run quarto preview
```

This opens the site in your browser and reloads it whenever a file changes. You can also open docs/index.html directly in a browser, but the search box doesn't work that way.



## The data

The data used in analysis blog posts are: 

Data: [babynames](https://cran.r-project.org/package=babynames), from [US Social Security Administration](https://www.ssa.gov/oact/babynames/limits.html) records. Licence: CC0.
Data: [Palmer Penguins](https://allisonhorst.github.io/palmerpenguins/), Palmer Station Antarctica LTER.

All of the data comes from the built in data sets in native R or Python 

