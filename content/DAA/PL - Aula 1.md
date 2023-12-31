21 Setembro 2023 - #DAA

- ## Types of Data
  
  -Numerical
	- Discrete Data ({1,2,3,...})
	- Continuous Data (\[1, +$\infty$])
- *Categorical* (binary, languages, ...)
- **Ordinal** (ratings of 1 to 5)
  
  *not-scaled
  **scaled
  
  #+BEGIN_EXAMPLE - Qual o tipo de dado que representa a quantidade de gasóleo?
  Numérico: continuous data
  #+END_EXAMPLE 
  
  >[!example]- Qual o tipo de dado que representa a quantidade de gasóleo?
  >Numérico: continuous data
  
  >[!example]- Qual o tipo de dado que representa a nacionalidade?
  >Categórico
  
  >[!example]- Qual o tipo de dado que representa a idade?
  >Numérico: discreto
- ## Mean, Median & Mode
- #+BEGIN_TIP
  A mean in math is the average of a data set, found by adding all numbers together and then dividing the sum of the numbers by the number of numbers
  #+END_TIP
- >[!hint]+
  >A **mean** in math is the average of a data set, found by adding all numbers together and then dividing the sum of the numbers by the number of numbers.
- ## Standard Deviation & Variance
- ## Probability Density functions
- ## Percentiles
  
  There are 3 important percentiles:
- 50% - median
- 25% - 1st percentile
- 75% - 3rd percentile
  
  >[!note]+
  >These 3 percentiles allow the creation of box plot graphs. These specific graphs allow the discovery and presentation of outliers.
- ## Covariance & Correlation
  
  >[!hint]+
  >**Covariance** measures the direction of a relationship between two variables, while **correlation** measures the strength of that relationship.
  
  Covariance is hard to interpret, thus correlation is used instead.
  In a dataset, correlations >0.5 are considerable.
  
  >[!caution] Correlation does not mean causation!
- ## Practical session of the class: miniconda
  IDEs: PyCharm, VS Code, (Jupyter - not recommended)
  
  Depois de instalar o miniconda, correr os seguintes comandos:
- conda create --name daaEnv python=3.10
- conda activate daaEnv
- python --version
- conda install pandas
- conda install xlrd
- conda install xlwt
- conda install matplotlib
- conda install seaborn
- conda install scikit-learn
- conda install jupyterlab
- conda list
- ## Resource links
- https://en.wikipedia.org/wiki/Average
- https://en.wikipedia.org/wiki/Median
- https://en.wikipedia.org/wiki/Mode_(statistics)
- https://en.wikipedia.org/wiki/Standard_deviation
- https://en.wikipedia.org/wiki/Variance
- https://en.wikipedia.org/wiki/Probability_density_function
- https://en.wikipedia.org/wiki/Percentile
- https://en.wikipedia.org/wiki/Covariance
- https://en.wikipedia.org/wiki/Correlation