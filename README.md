# Julia_info
Some information and knowledge about Julia.


# jupyter notebook

    import Pkg

    Pkg.add("Gadfly")  # using Gadfly for example , we can add other packages.

    Pkg.status()  # to make sure we have add the right package.

The followings are some packages often be used:

    using RDatasets
    using DataFrames

    iris = dataset("datasets","iris")
    first(iris,5)

    using StatsBase
    using JSON
    using CSV
    using LightXML
    using HypothesisTests


## by 被移除,嘗試使用combine...groupby
##### 細緻處理 
    combine(groupby(iris,:Species),
            :PetalLength .=> mean .=> :PL_mean ,
            :PetalLength .=> sum .=> :PL_sum )
        
     

## Pluto notebook

    import Pluto
    Pluto.run()
