set(COMPONENT_SRCS "AudioPipeline.c" "VolcRTCDemo.c")
set(COMPONENT_ADD_INCLUDEDIRS .)

# idf_component_register(SRCS ${COMPONENT_SRCS}
#                     INCLUDE_DIRS "."
#                     REQUIRES audio_board audio_pipeline audio_hal esp_wifi nvs_flash lwip spiffs VolcEngineRTCLite)

register_component()

#release_remove_tag add_prebuilt_library(VolcEngineRTCLite "libVolcEngineRTCLite.a" REQUIRES mbedtls json zlib)
#release_remove_tag target_link_libraries(${COMPONENT_LIB} PRIVATE VolcEngineRTCLite)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC -Wno-unused-variable -Wfatal-errors -Wno-incompatible-pointer-types -Wno-int-conversion -Wno-format -Wno-implicit-function-declaration -Wno-pointer-sign -Wno-double-promotion  -Wno-unused-value -Wno-switch -Wno-return-type -g -O3")  
