# Copyright (C) 2007-2015 Istituto Italiano di Tecnologia ADVR & iCub Facility & RBCS Department
# Authors: Enrico Mingo, Alessio Rocchi, Mirko Ferrati, Silvio Traversaro, Alessandro Settimi and Francesco Romano
# CopyPolicy: Released under the terms of the LGPLv2.1 or later, see LGPL.TXT


PROJECT(Plugin_Clock)

include(AddGazeboYarpPluginTarget)



add_gazebo_yarp_plugin_target(LIBRARY_NAME clock
                              INCLUDE_DIRS include/gazebo include/GazeboYarpPlugins
                              SYSTEM_INCLUDE_DIRS ${GAZEBO_YARP_COMMON_HEADERS} ${Boost_INCLUDE_DIRS} ${GAZEBO_INCLUDE_DIRS}  ${SDFORMAT_INCLUDE_DIRS} ${PROTOBUF_INCLUDE_DIRS}
                              LINKED_LIBRARIES gazebo_yarp_rpc_clock gazebo_yarp_lib_common ${YARP_LIBRARIES} ${GAZEBO_LIBRARIES} ${Boost_LIBRARIES}
                              HEADERS include/gazebo/Clock.hh 
                                      include/GazeboYarpPlugins/ClockServerImpl.h
                              SOURCES src/Clock.cc 
                                      src/ClockServerImpl.cpp
                                 )
