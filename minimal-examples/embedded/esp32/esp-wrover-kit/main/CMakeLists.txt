idf_component_register(SRCS
		lws-minimal-esp32.c
		devices.c
		INCLUDE_DIRS "../libwebsockets/include;${IDF_PATH}/components/spi_flash/include;${IDF_PATH}/components/nvs_flash/include;${IDF_PATH}/components/lwip/port/include")

	target_link_libraries(${COMPONENT_LIB} PRIVATE websockets)
include_directories(../build/libwebsockets)
