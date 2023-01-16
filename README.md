# gcc  
rpm -Uvh --force --nodeps *.rmp  
gcc -fsanitize=address -g test.cpp  
source ./devtoolset-9/enable && gcc -v && gcc -fsanitize=leak -g test.cpp  
ASAN_OPTIONS="log_path=./log alloc_dealloc_mismatch=0 allow_addr2line=true" ./a.out  
