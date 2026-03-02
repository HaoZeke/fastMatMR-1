## Patch release

Fixes a clang compiler warning ("ignoring return value of function
declared with 'nodiscard' attribute") in the vendored fast_matrix_market
C++ header `read_body_threads.hpp`, which produced a WARNING on the
CRAN r-devel Fedora clang check.

The fix casts the discarded `std::future::get()` return value to void.

## R CMD check results

0 errors | 0 warnings | 1 note

The installed package size note is expected due to the vendored
fast_matrix_market C++ header-only library.
