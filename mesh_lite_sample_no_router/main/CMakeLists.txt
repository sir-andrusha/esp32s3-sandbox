idf_component_register(SRCS "no_router.c"
                       INCLUDE_DIRS ".")

if(CONFIG_MESH_ROOT)
    set(WEB_SRC_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../front/web-demo")
    if(EXISTS ${WEB_SRC_DIR}/site)
        spiffs_create_partition_image(www ${WEB_SRC_DIR}/site FLASH_IN_PROJECT)
    else()
        message(FATAL_ERROR "${WEB_SRC_DIR}/site doesn't exit. Please add index.html there.")
    endif()
endif()