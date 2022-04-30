# Quantification of extreme weather events and their future changes using Physics-Informed DeepONet modeling and functional priors
This is a DARPA - ACTM project. The scope is to develop coarse-scale and data-informed simulation methods that can accurately predict 
  statistical features of climate systems. The goal is to study long timescale features of climate dynamics 
  reliably without the use of expensive high resolution simulations, which are intractable over decadal timescales
  
  This work is funded by Defense Advanced research Projects Agency, as part of the AI-Assited Climate Tipping-point Modelling program. 

## TEAM
This project is a collaboration between Massachusetts Institute of Technology,
  Brown University, Pacific Northwest National Laboratory. The PIs at each organisation are 
  <ul>
    <li><a href="http://meche.mit.edu/people/faculty/sapsis@mit.edu"> Themistoklis Sapsis </a></li>
    <li><a href="https://www.brown.edu/research/projects/crunch/george-karniadakis"> George Karniadakis </a></li>
    <li><a href="https://www.pnnl.gov/people/lai-yung-ruby-leung"> Lai-yung (Ruby) Leung </a></li>
  </ul>

The team includes the following graduate students and postdocs
<p><ul>
    <li>Alexis Charalampopoulos (MIT)</li>
    <li>Alireza Mojahed (MIT)</li>
    <li>Ethan Pickering (MIT)</li>
    <li>Sualeh Khurshid (MIT)</li>
    <li>Aniruddha Bora (Brown)</li>
    <li>Khemraj Shukla (Brown)</li>
    <li>Bryce Harrop (PNNL)</li>
    <li>Shixuan Zhang (PNNL)</li>
</ul></p>

## Project Summary
The governing equations of climate and weather prediction are chaotic, non-linear and multiscale in nature. This is partly due to the underlying
  turbulent fluid motion which is strongly coupled with other multi-physics processes such as convection, particle-transport, sea-ice interaction
  etc. The governing equations of some of these interactions are well known while others are difficult to derive from first principles.
  The unknown parts are often parametrized empiriacally. This physics based approach allows for simulation of
  the climate system using high performance codes (HPC) on state-of-the-art supercomputers. Fully resolved simulations are prohibively expensive 
  due to the large degrees of freedom that are exicted. Therefore,  high fidelity accurate simulations are limited to short time windows. Although, 
  coarse grids can be used to simulate the climate on the fastest supercomputers available today, their accuracy is severely delpleted due
  to the absence of sub-grid scale processes (or inaccurate models) that interact with atmospheric circulation. Our project
  employs techniques from data assimilation and machine learning to learn the correction for the coarse-resolution simulation with respect to 
  high-resolution simulation. The application of this correction to coarse models improves their predictions
  and makes them comparable to the high-resolution counterpart. An additional goal is to develop methods
  that require minimal changes to the highly scalable HPC solvers.

We are developing our methods by studying the reduced problem of Quasigeostrophic (QG) turbulence. We are exploring
   the use of classical methods such as LSTM and recently developed operator learning methods, specifically
   DeepONet. The code and tutorials for employing DeepONet can be found 
   <a href="https://deepxde.readthedocs.io/en/latest/"> here </a>. An important feature of our approach is that
   the ML corrections are implemented in post-processing of data from coarse simulation rather than online. This requires
   no changes to the solver. The methods will then be employed on data from a full
   climate simulation using DOE Exascale Earth System Model (E3SM). The documentation for E3SM can be found 
   <a href="https://e3sm.org/">here</a>.
   
## Links to data and documentation
The problem description and outline of the proposal can be found in <a href="darpa_milestone_1.pdf"> Milestone Report 1</a>.
  
Details on hybrid methodology can be found in <a href="darpa_milestone_2.pdf"> Milestone Report 2</a>.

The specific dataset for QG Model will be available <a href="data/">here</a> soon. The code for generating this dataset will
soon be available here. The LSTM implementation of the coarse model correction will be made available here. 
The The datasets from E3SM will soon be made
  available here. 
  
  
# Relevant Publications  
  E. Pickering, G. Karniadakis, T. Sapsis, Discovering and forecasting extreme events via active learning in neural operators, Submitted, (2022) (19 pages). <a href="https://sandlab.mit.edu/Papers/22_Optimal_NN.pdf">pdf</a>.

L. Lu, P. Jin, G. Pang, Z. Zhang, and G. Karniadakis. Learning nonlinear operators via deeponet based on the universal approximation theorem of operators. Nature Machine Intelligence, 3(3):218–229, 2021. <a href="https://www.nature.com/articles/s42256-021-00302-5">link</a>.
