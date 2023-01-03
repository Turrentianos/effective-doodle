cmake_minimum_required(VERSION 3.8)
project(VulkanTutorial)

find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)
find_package(Vulkan REQUIRED)


add_executable(vulkan_test main.cpp)
set_target_properties(vulkan_test PROPERTIES CXX_STANDARD 17)
target_link_libraries(vulkan_test Vulkan::Vulkan glfw)
# target_include_directories(vulkan_test PRIVATE ${STB_INCLUDEDIR})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
