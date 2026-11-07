add_executable(vkSample vkSample.cpp)

# https://cmake.org/cmake/help/latest/module/FindVulkan.html
find_package(Vulkan REQUIRED)
target_link_libraries(vkSample PRIVATE Vulkan::Vulkan)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(vkSample PRIVATE glfw)

find_package(glm CONFIG REQUIRED)
target_link_libraries(vkSample PRIVATE glm::glm)
