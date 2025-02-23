
## When you need Union

> You can use Union when you need to read your object separatly  and see it individually but flush it by oneshot.

```
union Example {
    
    struct ReadByDemand{
    uint8_t   Read_lowest_8;
    uint8_t   Read_mid_8;
    uint16_t  Read_highest_16;
    } Read;
    uint32_t OneShotWrite;
} ;
```

here total memory will be allocated for **Example object** is 4 Bytes.
| 16           | 8 |8 |
|--------------|--|--|
| higher 16  &nbsp; &nbsp; &nbsp; &nbsp;| mid 8 |lower 8 | 

To update it by one shot :
you can use **OneShotWrite**

To read it by demand :
you can use **Read**

