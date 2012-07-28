#
# Install test data
#

configure_file(
  reportingmoduledatapaths.py.in
  ${CMAKE_BINARY_DIR}/Testing/Python/reportingmoduledatapaths.py
  @ONLY
  )

slicer_add_python_unittest(
        SCRIPT ReportingRoundTripTest.py
        SLICER_ARGS --disable-cli-modules)
#       --additional-module-paths ${CMAKE_BINARY_DIR}/lib/Slicer-4.1/qt-loadable-modules
