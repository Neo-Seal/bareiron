
file(GLOB_RECURSE app_sources
    "${CMAKE_CURRENT_LIST_DIR}/*.c"
)

idf_component_register(
    SRCS ${app_sources}

    PRIV_REQUIRES
        freertos
        esp_wifi
        esp_event
        esp_netif
        nvs_flash
        esp_timer
        lwip

    INCLUDE_DIRS
        "."
        "../include"
)
