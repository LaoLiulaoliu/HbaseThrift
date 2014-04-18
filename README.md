Hbase Thrift
============

Using python to manipulate Hbase's data through Hbase thrift


* Put, Puts, Get, Gets, Scan example in boilerplate.py

***


How to generate all the library file
------------------------------------

- Here are the setup code on ubuntu 14.04.4

```
sudo apt-get install libboost-dev libboost-test-dev libboost-program-options-dev libevent-dev automake libtool flex bison pkg-config g++ libssl-dev
sudo apt-get install python2.7-dev git
git clone https://git-wip-us.apache.org/repos/asf/thrift.git thrift
cd thrift
./bootstrap.sh
./configure; make; sudo make install
cd ..
mkdir HbaseThrift; cd HbaseThrift
thrift -gen py /home/ubuntu/hbase-0.98.1/hbase-thrift/src/main/resources/org/apache/hadoop/hbase/thrift/Hbase.thrift
mv gen-py/* .
rm -r gen-py/
mkdir thrift
cp -rp /home/ubuntu/thrift/lib/py/src/* ./thrift/
cp /home/ubuntu/hbase-0.98.1/hbase-thrift/src/main/resources/org/apache/hadoop/hbase/thrift/Hbase.thrift .
```
