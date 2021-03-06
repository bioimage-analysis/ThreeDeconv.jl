# ThreeDeconv.jl

**ThreeDeconv.jl** is a 3D deconvolution software for fluorescence microscopy written in [Julia](https://julialang.org).
The detail of the algorithm is available in [our paper](https://www.nature.com/articles/s41598-018-29768-x#Sec21) and [our website](http://www.computationalimaging.org/publications/2d-deconvolution-for-low-photon-count-fluorescence-imaging-scientific-reports-2019/).
While the deconvolution algorithm is the same as described in the paper, we made some improvements in our software along with the major update of Julia. Please refer to [NEWS.md](NEWS.md).

# Instlation

Hit the key `]` in the Julia REPL to ender the Pkg REPL-mode, and run

```julia-repl
pkg> add https://github.com/computational-imaging/ThreeDeconv.jl.git
```

# Usage

The sample Jupyter notebook is avaialbe in the `example` directory.

To run the notebook, you need to install Julia packages, [IJulia.jl](https://github.com/JuliaLang/IJulia.jl), [PyCall.jl](https://github.com/JuliaPy/PyCall.jl), [PyPlot.jl](https://github.com/JuliaPy/PyPlot.jl) and [Conda.jl](https://github.com/JuliaPy/Conda.jl), and a Python package, [scikit-image](https://scikit-image.org/), for image I/O. You can run the following in Julia's REPL to install them. If you already have a Python environment that you want to use from Julia, please consult with `PyCall.jl`in

```julia-repl
pkg> add Conda
julia> using Conda
julia> Conda.add_channel("conda-forge")
julia> Conda.add("scikit-image")
julia> ENV["PYTHON"]=""
pkg> add PyCall PyPlot
```

# Citation

["A convex 3D deconvolution algorithm for low photon count fluorescence imaging"](https://www.nature.com/articles/s41598-018-29768-x#Sec21)

_Scientific Reports_ **8**, Article number: 11489 (2018)

Hayato Ikoma, Michael Broxton, Takamasa Kudo, Gordon Wetzstein

If you use this library for your research, please cite our paper.

# To biologists

If you find this package useful but feel that it lacks some functionalities for your research, feel free to create an issue in this repository. I am happy to extend this package to accomodate your need.

# Dataset

The dataset used in our paper is available at [Google Drive (150MB)](https://drive.google.com/a/stanford.edu/file/d/1lWlvngb5iJkToFKLSA3N1FuScVPTe-42/view?usp=sharing).
The images are corrected with darkfield and flatfield correction as described in the paper.

Its raw dataset is also available at [Google Drive (1GB)](https://drive.google.com/a/stanford.edu/file/d/1pg_OG5GxjcKMSvwi4Si0HTyWT0XCW4Kt/view?usp=sharing).
This dataset comes with corresponding darkfield and flatfield images.

This dataset can be used for academic and other non-commercial purposes.
If you use this dataset in your research paper, please cite our paper.
