
add_library(modules SHARED
PhysiCell_geometry.cpp
PhysiCell_MultiCellDS.cpp
PhysiCell_pathology.cpp
PhysiCell_POV.cpp
#PhysiCell_standard_modules.h
PhysiCell_SVG.cpp
PhysiCell_various_outputs.cpp
)


target_link_libraries(modules physicellcore biofvm)

install(TARGETS modules DESTINATION lib)
