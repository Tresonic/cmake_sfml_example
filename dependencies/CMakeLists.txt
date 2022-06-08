include(FetchContent)

set(SFML_VERSION 2.5.1)
set(BUILD_SHARED_LIBS OFF)

message(STATUS "Fetching third party libraries")

FetchContent_Declare(
  SFML
  URL "https://github.com/SFML/SFML/archive/${SFML_VERSION}.zip"
)

# SFML
option(SFML_BUILD_AUDIO "Build audio" OFF)
option(SFML_BUILD_NETWORK "Build network" OFF)
FetchContent_MakeAvailable(sfml)
