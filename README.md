# db2_cpp
Guide for developing and deploying CPP code to Db2


g++ -m64 -fPIC -c <yourfile>.cpp -std=c++14 -I/opt/ibm/db2/V11.1/include/ -D_REENTRANT
g++ -m64 -shared -o <yourfile> <yourfile>.o -L$DB2PATH -ldb2 -Wl,-rpath,$DB2PATH/$LIB -lpthread
