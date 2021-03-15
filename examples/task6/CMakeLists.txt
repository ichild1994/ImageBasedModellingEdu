project(class6)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS "-fPIC -g")

include_directories("../..")


set(SURFACE_RECONSTRUCTION_SOURCES
        task6-1_surface_reconstruction.cc)
add_executable(task6_surface_reconstruction ${SURFACE_RECONSTRUCTION_SOURCES})
target_link_libraries(task6_surface_reconstruction mvs util core surface)

set(MESH_CLEAN_SOURCES
        meshclean.cc)
add_executable(meshclean ${MESH_CLEAN_SOURCES})
target_link_libraries(meshclean util core surface)
