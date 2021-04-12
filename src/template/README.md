# libhttpserver
```
cd ./extra/libhttpserver-master
./configure
make -j8 install
make clean
cd ../libhttpserver-master
mkdir ./build
cd ./build
../configure
make -j8 install
make clean
```
This should leave you with 
```
/usr/local/lib/libhttpserver.a
/usr/local/lib/ibhttpserver.la
/usr/local/lib/ibhttpserver.so
/usr/local/lib/ibhttpserver.so.0
/usr/local/lib/ibhttpserver.so.0.19.0
/usr/local/lib/ibmicrohttpd.a
/usr/local/lib/ibmicrohttpd.la
/usr/local/lib/ibmicrohttpd.so
/usr/local/lib/ibmicrohttpd.so.12
/usr/local/lib/ibmicrohttpd.so.12.57.0
```
as well as
```
/usr/local/include/httpserver
/usr/local/include/httpserver.hpp
/usr/local/include/httpserverpp
/usr/local/include/microhttpd.h
```
which will allow you to build this template
```
cd ../../
make
```
You might need to modify your `LD_LIBRARY_PATH`, but the run target does set it to `/usr/lib:/usr/local/lib`

Load test statistics:
```
Statistics        Avg      Stdev        Max
  Reqs/sec     13409.68    1075.06   16147.56
  Latency        9.32ms     1.82ms    92.72ms
  HTTP codes:
    1xx - 0, 2xx - 133633, 3xx - 0, 4xx - 0, 5xx - 0
    others - 0
  Throughput:     2.63MB/s
```
