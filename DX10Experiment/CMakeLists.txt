set( PROJECT_NAME
DX10Experiment
)
cmake_minimum_required( VERSION 2.8 )
include( ScanSourceFiles )

#----- Enable Unicode -----
add_definitions(-DUNICODE -D_UNICODE)

#------ additional includes ------
include_directories(
${DIRECTX_SDK_DIR}/include
)

#------ link directories listed ------
link_directories(
${DIRECTX_SDK_DIR}/lib
${DIRECTX_SDK_DIR}/lib/x64
${DIRECTX_SDK_DIR}/lib/x86
)
link_libraries(
${DirectX_D3DX10_LIBRARY}
${DirectX_LIBRARY}
)

#------ target -----
add_executable (${PROJECT_NAME} WIN32 ${MY_SRC} ${MY_HEADERS})