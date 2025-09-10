cmake_minimum_required(VERSION 3.10)
project(Lab2Cpp)

set(CMAKE_CXX_STANDARD 11)

# Поиск SDL2
find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

# Добавляем исполняемый файл со всеми исходными файлами
add_executable(app
    main.cpp
)

# Подключаем SDL2
target_link_libraries(app ${SDL2_LIBRARIES})
