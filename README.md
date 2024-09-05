# HospitalKG
In this repository, we present the SPARQL* queries developed for "_Spatiotemporal Data Modelling for Epidemiological Research in Hospitals_" [10.1109/JBHI.2024.3417224](https://ieeexplore.ieee.org/document/10568325) and the dataset in RDF* generated for testing them.

## 0. Related Repositories
Below, we present some other related repositories that may be of interest to you:
- [HospitalGeneratorRDF](https://github.com/LorenaPujante/HospitalGeneratorRDF): It is also linked to [10.1109/JBHI.2024.3417224](https://ieeexplore.ieee.org/document/10568325)

## 1. SPARQL* Queries
We have designed and implemented in SPARQL* a set of 6 queries based on patients' movements within a hospital that are meant to assist in several epidemiological research tasks. Each query is in a separate file, where the values of the parameters are the ones used in the experiments presented in [10.1109/JBHI.2024.3417224](https://ieeexplore.ieee.org/document/10568325). The objectives of each query are the following:
- **Q1:** Detection of an outbreak at a _Service_
- **Q2:** Detection of an outbreak at a _Location_
- **Q3:** Study of the spread of an outbreak from a patient via analysis of contacts
- **Q4:** Study of the spread of an outbreak from a set of patients via analysis of contacts
- **Q5:** Investigation of sources of contagion via analysis of contacts
- **Q6:** Discovery of the index patient

## 2. RDF* dataset
We provide the dataset used for the experiments presented in [10.1109/JBHI.2024.3417224](https://ieeexplore.ieee.org/document/10568325) This is an RDF* knowledge graph that follows the spatiotemporal data model presented in the paper. It is a synthetic dataset whose data have been generated using the [_H-Outbreak_](https://github.com/denissekim/Simulation-Model) simulation model. The values for the parameters of H-Outbreak used to create the dataset are the following:
- _n_patients_: 0.7
- _steps_: 462 (462×8 = 3696 Hours → 3696/24 = 154 Days → 154/7 = 22 Weeks)
- _population_: 170000
- _step_time_: 8 (hours)
- _init_exposed_: 1
- _init_infected_: 0
- _arrival_rate_: 17.55
- _prob_arrival_ER_: 0.7
- _arrival_state_colonized_: 0.076 
- _arrival_state_S_: 0.9973429
- _arrival_state_I_: 0.001563
- _arrival_state_NS_: 0.0010941
- _prob_p-env_min_: 0.14
- _prob_p-env_max_: 0.9
- _prob_p-env_mean_: 0.52
- _prob_env-p_min_: 0.3262
- _prob_env-p_max_: 0.5437
- _prob_env-p_mean_: 0.435
- _prob_pe_min_: 0.18
- _prob_pe_max_: 0.3
- _prob_pe_mean_: 0.24
- _incubation_time_min_: 48
- _incubation_time_max_: 72
- _prob_quick_recov_min_: 0.0
- _prob_quick_recov_max_: 0.23
- _prob_quick_recov_mean_: 0.115 
- _prob_long_recov_min_: 0.5985
- _prob_long_recov_max_: 0.9975
- _prob_long_recov_mean_: 0.7981
- _treatment_days_min_: 5
- _treatment_days_max_: 15
- _treatment_days_mean_: 10
- _prob_death_: 0.069
- _max_patients_rx_: 3
- _max_patients_qx_: 2
- _min_steps_rx_: 10
- _min_steps_qx_: 30
- _max_ward_movements_: 2
- _max_steps_er_icu_: 3
- _max_movements_room_: 5
- _occupancy_icu_: 0.46

To transform the output from H-Outbreak in an RDF* knowledge graph, we have used [_HospitalGeneratorRDF_](https://github.com/LorenaPujante/HospitalGeneratorRDF). The file `Dataset/LogicZones.ttl` has been created ad hoc and contains both the nodes and the edges related to the class _LogicZone_. <!--The values for the parameters used to create the hospital and the temporal data are the following:-->
<!--- _index_: 1600-->
<!--- _huPerService_: 3-->
<!--- _nFloors_: 5-->
<!--- _huPerFloor_: 6-->
<!--- _nRows_: 3-->
<!--- _nColumns_: 4-->
<!--- _startDateTime_: 01/01/2023 08:00:00-->
<!--- _optionFloorUH_: None-->
