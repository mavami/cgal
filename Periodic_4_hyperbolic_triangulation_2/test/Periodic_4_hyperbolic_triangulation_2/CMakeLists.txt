# Created by the script cgal_create_cmake_script
# This is the CMake script for compiling a CGAL application.


project( Periodic_4_hyperbolic_triangulation_2_Tests )

cmake_minimum_required(VERSION 2.8.10)

find_package(CGAL QUIET COMPONENTS Core )

if ( CGAL_FOUND AND CGAL_Core_FOUND )

  	include( ${CGAL_USE_FILE} )

  	include( CGAL_CreateSingleSourceCGALProgram )

    create_single_source_cgal_program( "test_p4ht2_construct_point_2.cpp" ) 
    create_single_source_cgal_program( "test_p4ht2_exact_complex_numbers.cpp" )
    create_single_source_cgal_program( "test_p4ht2_intersections.cpp" )
    create_single_source_cgal_program( "test_p4ht2_locate.cpp" )
    create_single_source_cgal_program( "test_p4ht2_matrix.cpp" )
    create_single_source_cgal_program( "test_p4ht2_removal_iterator.cpp" )
    create_single_source_cgal_program( "test_p4ht2_removal.cpp" )
    create_single_source_cgal_program( "test_p4ht2_insert_degenerate.cpp" )
    
else()
  
    message(STATUS "This program requires the CGAL library and the GMP library, and will not be compiled.")
  
endif()

