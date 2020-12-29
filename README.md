# BaggedRandomCausalNetworks
The file 'script R.txt' contains the code for all simulations, experiments, and graphical elements of the associated paper.

########## MAIN SIMULATION SCRIPT ########### 
This piece of code runs sparse/dense network simulations and compares crude estimation with boosted logistic regression, bagged random causal networks (few/many bags, with/without prior knowledge), and full DAG learning.
All parameters (including number of iterations, desired number of successful runs, etc) are customizable at the top of the script. The code writes the interim results on file every x iterations.

########## MAKING GRAPHS ########## 
This is ancillary code to be used to draw boxplots of average tretament effect errors for the main simulation script.

########## MANUAL DAG ##########
This part draws example DAGs with pre-specified confounder/collider structures.

########## DRAWING COMPLEX CAUSAL NETWORK AS EXAMPLE ##########
This part shows how to use the Rgraphviz graphical library to draw DAGs with flexible layout and color them as needed.

########## TIME LEARNING DAGs/ BAGGED DAGS ##########
This portion of the script tests the time benchmarks of the full DAG learning algorithms vs. the bagged estimators. The code compares hill-climbing with grow-shrink but the functions can be replaced by other learners.

########## NUMBER OF NODES ##########
This code checks what is the best curve fit for the time benchmark results, i.e. empirical complexity (testing linear, quadratic, cubic, fourth power, and other types).

########## FIGURE GAC #########
Here, an example of the GAC application with multiple adjustement sets on a random DAG is given. The drawing is made using the ggdag library.

########## REAL-WORLD DATA TEST ##########
This portion of the code applies the DAG/GAC framework and the bagged random causal network to the Class III Malocclusion dataset (the data are downloaded on the fly using the public url).
