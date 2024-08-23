# Description

Both Redis and Memcached are:
noSQL key-value in-memory data storage systems
open source
used to speed up applications
supported by the major cloud service providers

## How Redis stores data

Redis has five data types:

String: a text value
Hash: A hash table of string keys and values
List: A list of string values
Set: A non-repeating list of string values
Sorted Set: A non-repeating list of string values ordered by a score value

## How Memcached stores data
Unlike Redis, Memcached has no data types, as it stores strings indexed by a string key. 
When compared to Redis, it uses less overhead memory. 
Also, it is limited by the amount of memory of its machine and, if full, it will start to purge values on a least recently used order. 
It uses an allocation mechanism called Slab, which segments the allocated memory into chunks of different sizes, and stores key-value data records of the corresponding size. 
This solves the memory fragmentation problem. 
Memcached supports keys with a maximum size of 250B and values up to 1MB

### Run memcached

sudo docker run -p 11211:11211 --name my-memcache -d memcached
