# local de desistino dos arquivos, no exemplo os resultado é salvo na pasta raiz do disco local c.
setwd("C:/") 
#instalar pacote
#verificar versão mais atual e modificar o numero no link abaix, exemplo a atual é 05.
install.packages("https://github.com/user-attachments/files/17557189/vhregression05.tar.gz", repos = NULL, type = "source")
#pacotes necessarios
library(minpack.lm)
library(ggplot2)
library(gridExtra)
library(openxlsx)
library(readxl)
library(regressionvh)



#seleciona os modelos que serão analisados
modelos_selecionados <- c( "Logistic", "Gompertz", "MMF", "Weibull", "Exponential",
                           "Modified Exponential", "Logarithmic", "Reciprocal Logarithm", "Vapor Pressure",
                           "Power Fit", "Modified Power", "Shifted Power", "Geometric",
                           "Modified Geometric", "Hoerl Model", "Exponential Associative 2",
                           "Exponential Associative 3", "Sinusoidal", "Gaussian",
                           "Hyperbolic", "Heat Capacity", "Rational", "Richards","Asymptotic","Harris","Brody","Wilmink")
#executa a analise
analise_completa(dados, modelos_selecionados)
