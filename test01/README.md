cd /workspaces/asmjit

mkdir build && cd build

cmake .. -DASMJIT_STATIC=true

make

cd /workspaces/asmjit/test01

g++ -Os -I../src t01.cpp ../build/libasmjit.a -lrt -o t01.out && ./t01.out
