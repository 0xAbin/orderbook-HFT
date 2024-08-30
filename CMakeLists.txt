cmake_minimum_required(VERSION 3.10)

# Project name
project(orderbook-HFT-perp VERSION 1.0 LANGUAGES CXX)

# Specify C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Include directories
include_directories(${PROJECT_SOURCE_DIR}/include)

# Add source files
set(SOURCES
        src/main.cpp
#        src/OrderBook.cpp
#        src/SpotOrderBook.cpp
#        src/PerpetualOrderBook.cpp
#        src/TradeExecution.cpp
#        src/MatchingEngine.cpp
#        src/Utils.cpp
)

# Add executable
add_executable(orderbook-HFT-perp ${SOURCES})

# Link libraries (if any)
# target_link_libraries(orderbook-HFT-perp PRIVATE SomeExternalLibrary)

# Tests
add_subdirectory(tests)

# Install target
install(TARGETS orderbook-HFT-perp DESTINATION bin)
install(DIRECTORY include/orderbook DESTINATION include)