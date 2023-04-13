# Redis

### Open redis-cli (default port is 6379)
```
redis-cli
```
### Open redis-cli for a specific port
```
redis-cli -p 6379
```
### List all the kyes for redis
```
keys *
```
### Delete/Flush all keys from redis
```
FLUSHALL
```
### To see all cache of a specific attribute
```
redis-cli -h host_ip KEYS '*app:cache*'
```
### Delete all cache of specific type and return the count
```
redis-cli -h host_ips KEYS '*app:cache*' | awk '{print $1}' | xargs redis-cli -h host_ip DEL
```
### Returns a subset of the sorted set
```
ZRANGE input_zset 0 -1
```
> ZRANGE key start stop
### Get value in key
```
GET "KEYNAME" 
```
### Search a specific pattern and return count
```
eval "return #redis.pcall('keys', '*AM')" 0
```
### See count of ZCARD that updates every_second
```
watch -n 5 "redis-cli -p 6379 -n 0 ZCARD input_zset"
```
