set(fortran_src
    mkgfsnemsioctl.f90)

set(exe_name mkgfsnemsioctl)
add_executable(${exe_name} ${fortran_src})
target_link_libraries(
  ${exe_name}
  nemsio
  bacio_4
  w3nco_d)

install(TARGETS ${exe_name} RUNTIME DESTINATION ${exec_dir})
