
add_library(biofvm SHARED
     BioFVM_agent_container.cpp 
     BioFVM_basic_agent.cpp 
     BioFVM_matlab.cpp BioFVM_mesh.cpp 
     BioFVM_mesh.cpp
     BioFVM_microenvironment.cpp 
     BioFVM_MultiCellDS.cpp 
     BioFVM_solvers.cpp 
     BioFVM_utilities.cpp 
     BioFVM_vector.cpp 
     pugixml.cpp)

target_link_libraries(biofvm ${OpenMP_CXX_LIBRARIES})

install(TARGETS biofvm DESTINATION lib)
