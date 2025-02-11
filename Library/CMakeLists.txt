add_library(Library STATIC
	"Lib.cpp"
	Lib.hpp
)
target_include_directories(Library INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})