# Project Needs a name, of course
project(RunnerExample)

# We add our source code here
set(example_SRCS homefilesrunner.cpp)

# Now make sure all files get to the right place
add_library(plasma_runner_example_homefiles MODULE ${example_SRCS})
target_link_libraries(plasma_runner_example_homefiles KF5::Runner KF5::KIOCore KF5::KIOWidgets)

# Install the library and .desktop file
install(TARGETS plasma_runner_example_homefiles DESTINATION ${PLUGIN_INSTALL_DIR})
install(FILES plasma-runner-example-homefiles.desktop DESTINATION ${SERVICES_INSTALL_DIR})
