add_executable(i2c_bus_scan
        bus_scan.c
        )

# pull in common dependencies and additional i2c hardware support
target_link_libraries(i2c_bus_scan pico_stdlib hardware_i2c)

pico_enable_stdio_usb(i2c_bus_scan 1)
pico_enable_stdio_uart(i2c_bus_scan 0)

# create map/bin/hex file etc.
pico_add_extra_outputs(i2c_bus_scan)

# add url via pico_set_program_url
example_auto_set_url(i2c_bus_scan)
