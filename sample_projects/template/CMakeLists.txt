add_subdirectory(custom_modules)

add_executable(template main.cpp)

target_include_directories(template PUBLIC
                          ${PROJECT_BINARY_DIR}
                          )
                          
target_link_libraries(template PUBLIC templatecustmodules ${OpenMP_CXX_LIBRARIES})

install(DIRECTORY DESTINATION "template/output")
install(DIRECTORY ${CMAKE_SOURCE_DIR}/sample_projects/template/config DESTINATION "template")
install(TARGETS template DESTINATION "template")

IF(WIN32)
	install(TARGETS biofvm DESTINATION "template")
	install(TARGETS physicellcore  DESTINATION "template")
	install(TARGETS modules  DESTINATION "template")
	install(TARGETS templatecustmodules DESTINATION "template")
ENDIF()