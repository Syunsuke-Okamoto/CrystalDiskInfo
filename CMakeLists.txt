cmake_minimum_required( VERSION 3.14 )

# Splution(*.sln) and Project(*.vcxproj)
project( DiskInfo )

add_definitions(-D_AFXDLL)
set(CMAKE_MFC_FLAG 1) # 1:static MFC DLL, 2: shard MFC DLL
set(CMAKE_ANSI_CXXFLAGS)
add_definitions(-D_MBCS_)

file(GLOB MY_SOURCE *.h *.cpp)
add_executable( DiskInfo ${MY_SOURCE} )

# Set StartUp Project (Option)
set_property( DIRECTORY PROPERTY VS_STARTUP_PROJECT "DiskInfo" )

# CMAKE_VS_WINDOWS_TARGET_PLATFORM_VERSION
# CMAKE_WINDOWS_KITS_10_DIR