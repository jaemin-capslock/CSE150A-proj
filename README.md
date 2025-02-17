# CSE150A-proj

I am using 2023 National Survey on Drug Use and Health (NSDUH) survey data, which was conducted by Substance Abuse and Mental Health Services and Administration of the U.S.

The data is available online, see [link](https://www.samhsa.gov/data/data-we-collect/nsduh/datafiles).

My `.ipynb` file contains picking out desired columns for analysis [^1] , null/exception handling, as well as preprocessing for better handling. I then use `pgmpy` library to construct a bayesian graph based on the datatable using the Hill Climbing optimization method, and then apply Maximum Likelihood as the desired cost function to fit my bayesian network's parameters. I then conduct a few example studies, and confirm that the results largely follow expectations.

I would like to build a dynamically interactive program to create a personalized "risk estimator", where the user can input their demographic information, then some substance use data, to obtain personal risk for psychopathology. The dataset also contains information on age of first drug use, so it would be interesting to see more specific patterns for certain demographics, as well as some sort of casuality analysis. Data from past years are available, but I'm not sure if I could use Markov chains as it's unlikely that the samples were obtained by the same person.


[^1]: See [link](https://www.samhsa.gov/data/system/files/media-puf-file/NSDUH-2023-DS0001-info-codebook_v1.pdf)