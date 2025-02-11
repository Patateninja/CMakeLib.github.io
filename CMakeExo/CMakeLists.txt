# CMakeList.txt : CMake project for CMakeExo, include source and define
# project specific logic here.
#

# Add source to this project's executable.
add_executable (CMakeExo "CMakeExo.cpp" "CMakeExo.h")

find_package(SFML COMPONENTS system window audio CONFIG REQUIRED)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET CMakeExo PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
target_link_libraries(CMakeExo PRIVATE Library)

target_link_libraries(${PROJECT_NAME} PRIVATE
	sfml-audio
	sfml-system
	sfml-graphics
	sfml-window
	sfml-network
)