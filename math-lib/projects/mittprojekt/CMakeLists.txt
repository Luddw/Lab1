#--------------------------------------------------------------------------
# mittprojekt project
#--------------------------------------------------------------------------

PROJECT(mittprojekt)
FILE(GLOB mittprojekt_headers code/*.h)
FILE(GLOB mittprojekt_sources code/*.cc)

SET(files_mittprojekt ${mittprojekt_headers} ${mittprojekt_sources})
SOURCE_GROUP("mittprojekt" FILES ${files_mittprojekt})

ADD_EXECUTABLE(mittprojekt ${files_mittprojekt})
TARGET_LINK_LIBRARIES(mittprojekt core render Matlibrary)
ADD_DEPENDENCIES(mittprojekt core render Matlibrary)