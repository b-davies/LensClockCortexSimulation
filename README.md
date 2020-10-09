# LensClockCortexSimulation
Bootstrap simulations to assess a method for estimating original lithic nodule size from cortical curvature in an experimental quartz bipolar stone assemblage and its application to geometric whole assemblage indicators. Built analyzed using [R (4.0.2)](https://cran.r-project.org/) and [R Studio (1.1.383)](https://rstudio.com/), this code and data are used in a forthcoming publication:

Douglass, M., B. Davies, D. Braun, J. T. Faith, M. Power, and J. Reeves. Deriving Original Nodule Size of Lithic Reduction Sets from Cortical Curvature:  An Application to Monitor Stone Artifact Transport from Bipolar Reduction. Submitted to *Journal of Archaeological Science: Reports*.

This study uses estimates of curvature from stone fragments to estimate the size of the original whole. Simulations were used to assess the effects of the number of fragments measured on nodule size estimates, and the effects of addition and subtraction of preferred fragments on calculation of cortex ratio from curvature-derived values (see Dibble et al. 2005; Douglass et al. 2008). To run the simulation, be sure that data files (.csv) are stored in the 

To reproduce the results of the analysis, download the program and data files, as well as the required software ([R](https://cran.r-project.org/), [R Studio](https://rstudio.com/)) and follow these steps:

-Open the *LENSCLOCK_CURVE_notebook.rmd* file in R Studio, select the **Run** drop down menu and select **Run All**.
-To output graphs to file, remove the octothorp symbols (#) from the following code sections:

In section 3A:

#png(filename="Num_Frag.png",width=6,height=3.5,units="in",res=300)
grid.arrange(f2,f3,ncol=1,nrow=2,right="Number of Fragments",bottom="Curvature:Axial Radius",left="Frequency",heights=c(1,1))
#dev.off()

In section 4A:

#png(filename="LRQ_CR.png",width=6,height=5,units="in",res=300)
grid.arrange(leg,ch1m,ch2m,ch3m,ch4m,layout_matrix=lay,heights=c(0.75,3,3),widths=c(4,4),bottom="Cortex Ratio",left="Curvature:Axial Radius      ")
#dev.off()

In section 4B:

#png(filename="HRQ_CR.png",width=6,height=5,units="in",res=300)
grid.arrange(leg,ch1m,ch2m,ch3m,ch4m,layout_matrix=lay,heights=c(0.75,3,3),widths=c(4,4),bottom="Cortex Ratio",left="Curvature:Axial Radius      ")
#dev.off()

---
Copyright (c) 2020 Ben Davies and Matt Douglass
