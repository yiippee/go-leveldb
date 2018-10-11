# go-leveldb

manifest文件分析

56 F9 B8 F8 （校验和）
1C 00 （总长度为28）
01 （类型） 
01 （tag标志 kComparator） 
1A （长度26，下面为26个字节：leveldb.BytewiseComparator） 
6C 65 76 65 6C 64 62
2E 42 79 74 65 77 69 73 65 43 6F 6D 70 61 72 61
74 6F 72 

A4 9C 8B BE 校验和
08 00 长度为8
01 类型
02 tag标志  kLogNumber
03 kLogNumber日志文件号码 为3
09 tag标志 kPrevLogNumber
00 kPrevLogNumber 为0
03 tag kNextFileNumber
04 kNextFileNumber下一个文件号为4
04 tag kLastSequence 
00 kLastSequence 上一个seq为0



日志文件分析 000003.log 
F3 70 76 D7             校验和
16 00                   长度为22
01                      类型为1
01 00 00 00 00 00 00 00 key的seq，共八个字节uint64 
01 00 00 00 
01                      tag标志 kTypeValue类型
04                      key的长度
6E 61 6D 65             key的内容
03                      value的长度
6C 7A 62                value的内容
