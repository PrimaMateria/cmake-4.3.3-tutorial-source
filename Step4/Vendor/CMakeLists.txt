add_library(VendorLib INTERFACE)
target_compile_definitions(VendorLib INTERFACE TUTORIAL_USE_VENDORLIB)

# TODO11: Add the include directory to VendorLib
target_include_directories(VendorLib INTERFACE include)

# TODO12: Add the lib directory to VendorLib
target_link_directories(VendorLib INTERFACE lib)

# TODO13: Add the Vendor archive to VendorLib
# "Vendor" is not a CMake target — it's a raw linker name. The Unix linker
# convention automatically maps it to libVendor.a in the directories added
# by target_link_directories above.
target_link_libraries(VendorLib INTERFACE Vendor)
