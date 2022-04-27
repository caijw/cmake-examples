cmake_minimum_required(VERSION 3.5)

project(test)

add_executable(${PROJECT_NAME} main.c)

message(${CMAKE_COMMAND} )

add_custom_command(OUTPUT printout 
                   COMMAND ${CMAKE_COMMAND} -E echo compile finish
                   VERBATIM
                  )



add_custom_target(finish
                  DEPENDS printout
                  )