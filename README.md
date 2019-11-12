# Healthspan and lifespan predictors based on machine learning analysis of mouse frailty

This repository contains machine learning-derived models to predict age and lifespan from frailty assesment. The FRIGHT (**F**railty **I**nferred **G**eriatric **H**ealth **T**imeline) age model is designed to predict chronological age and the AFRAID (**A**nalysis of **F**railty and **D**eath) score is designed to predict time to death using frailty the 31 parameter murine frailty index (Whitehead et al. 2014). 

The models are packaged as `fright_age.sav` and `afraid_score.sav`. The iPython notebook shows how to load these models and use them on the data from **our biorxiv preprint (xxx)**. 

# Python Environment Requirements
Implementation of the FRIGHT and AFRAID models via the iPython notebook in the repository require Python version 3.7.x and the following packages:

- jupyter (6.0.1)
- scikit-learn (0.21.3)
- pandas (0.25.1)
- numpy (1.17.2)
- scipy (1.3.1)
- seaborn (0.9.0)

Note that the [most recent version of Anaconda](https://www.anaconda.com/distribution/) (2019.07) comes with these packages pre-installed. Currently the iPython script will work with a current Anaconda installation. However, to avoid issues with dependencies and future releases, a conda environment can be used.

`conda create -n frailtyEnv -c conda-forge python=3.7 pandas=0.25.1 seaborn=0.9.0 numpy=1.17.2 jupyter=6.0.1 scipy=1.3.1 scikit-learn=0.21.3`

You can then activate the new environment on OS/linux using `source activate frailtyEnv` in the terminal, or on Windows using `conda activate frailtyEnv` in AnacondaPrompt.

Once you've gotten started with the current version of Python via Anaconda, or with the `frailtyEnv` Conda environment, download the Git repository to your computer by clicking the 'Clone or Download' button (unzip the folder after it's downloaded), or using a git command (`git clone https://github.com/xxx`).

Navigate to the downloaded Git repository on your computer in the terminal or AnacondaPrompt and then start a Jupyter notebook (`jupyter notebook`).

# Running the FRIGHT and AFRAID models
The FRIGHT and AFRAID models are packaged as `fright_age.sav` and `afraid_score.sav` in the repository. We've also included data from the methionine restriction intervention from the paper to provide an example of how to run the models. 

Running the iPython notebook will show how to load the data, load the models and calculate FRIGHT age and AFRAID score on the data.

Note that the column names for your data must match the formatting in the iPython script as listed in the `frightVariables` and `afraidVariables` objects. If you're running into trouble running your data through the model it may be because the column names from your data doesn't exactly match the column names that the models are expecting.
