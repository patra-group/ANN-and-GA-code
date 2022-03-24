# ANN and GA Codes
ANN based code to predict TiO2 structural energy using AENET package 
Customized Python Code to evaluate Rg of copolymer sequences

##COMMANDS TO EXECUTE:
##Prerequisite packages :


  sudo apt-get install gfortran
	
	
  sudo apt-get install build-essential
  
	
	sudo apt install libopenblas-dev
  
	
	sudo apt install libopenmpi-dev
  
##AENET INSTALLATION##																																



tar xvf <aenet-package>

	
cd ~/aenet/lib

	
make

	
cd ~/aenet/src

	
make -f ./makefiles/Makefile.gfortran_openblas_mpi


	
##RUN AENET PACKAGE##
	
	
	

	
	nohup mpirun -np 1 generate.x generate.in > generate.out &
 
	
cp *.train ../02-train/

	

	
nohup mpirun -np 10 train.x train.in > train.out & 

	
nohup mpirun -np 1 predict.x predict.in > predict.out &
  
---------------------------------------------------------
  

#GA Code


	
nohup python3 parameter_try.py &  
	
-----------------------------------------------------------
Check out this article and cite this arxiv: **https://arxiv.org/abs/2107.06439v1 **
-----------------------------------------------------------
