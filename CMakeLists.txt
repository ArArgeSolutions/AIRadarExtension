cmake_minimum_required(VERSION 3.16.3...3.19.7 FATAL_ERROR)

project(AIRadar)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "https://github.com/ArArgeSolutions/AIRadarExtension")
set(EXTENSION_CONTRIBUTORS "Emin Ibili (AR ARGE)")
set(EXTENSION_DESCRIPTION "AIRadar is a 3D Slicer extension that connects to a clinical backend and MONAI Label server to browse, download, visualize and upload patient volumes and segmentations, with optional streaming to HoloLens via Slicer Virtual Reality. Known related patents: none.")
set(EXTENSION_ICONURL "https://raw.githubusercontent.com/ArArgeSolutions/AIRadarExtension/main/Resources/Icons/AIRadar.png")
set(EXTENSION_SCREENSHOTURLS "https://raw.githubusercontent.com/ArArgeSolutions/AIRadarExtension/main/Resources/Screenshots/AIRadar_Screenshot1.png")
set(EXTENSION_DEPENDS "NA")  # no Slicer extension dependencies

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(AIRadar)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_GENERATE_CONFIG})
include(${Slicer_EXTENSION_CPACK})

