
add_executable(stdthread_rand_per_thread rand_per_thread.cpp)
target_link_libraries(stdthread_rand_per_thread doctest)
add_test(NAME "stdthread::random-number-per-thread" COMMAND stdthread_rand_per_thread)

add_executable(stdthread_joinable joinable_thread.cpp)
target_link_libraries(stdthread_joinable PRIVATE doctest Threads::Threads)
add_test(NAME "stdthread::joinable" COMMAND stdthread_joinable)

add_executable(stdthread_pass_arguments pass_arguments.cpp)
target_link_libraries(stdthread_pass_arguments PRIVATE doctest Threads::Threads)
add_test(NAME "stdthread::pass-arguments" COMMAND stdthread_pass_arguments)

add_executable(stdthread_thread_pool thread_pool.cpp)
target_link_libraries(stdthread_thread_pool PRIVATE doctest Threads::Threads)
add_test(NAME "stdthread::thread-pool" COMMAND stdthread_thread_pool)

add_executable(stdthread_scoped_thread scoped_thread.cpp)
target_link_libraries(stdthread_scoped_thread PRIVATE doctest Threads::Threads)
add_test(NAME "stdthread::scoped-thread" COMMAND stdthread_scoped_thread)
