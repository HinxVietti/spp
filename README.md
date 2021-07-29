# Simple Package base Protocol

simple package-base protocol

## Header

| offset | length | desc   | value       | Purpose | data                               |
| ------ | ------ | ------ | ----------- | ------- | ---------------------------------- |
| 0 | 1 | byte | reserved |  | 0xff |
| 1      | 4   | int     | type        |         | spp1/829452403                     |
| 5 | 3 | byte[3] | reserved | | [0xff,0xfe,0x0a] |
| 8      | 4      | uint   | version     |         | 1                                  |
| 12     | 4      | uint   | header-data |         |                                    |
| 16     | 1      | byte   | header-type |         | [HeaderType](## HeaderType (ENUM)) |
| 17     | 4      | uint   | data        |         |  |
| 21 | 1      | byte   | type        |         | [DataType](## DataType (ENUM))                          |

## Header Sample

  sample desc.

| offset | 0 | 8 | 12 | 16 | 17 | 21 |
| ------ | - | - | -- | -- | -- | -- |
| data | ?spp1?? | 0001 | 0512 | 1 | 1024 | 1 |

## SPP1

[header/header-dat/dat/] checksum

## HeaderType (ENUM)

| value | enum   | desc        |
| ----- | ------ | ----------- |
| 0     | unknow | unknow      |
| 1     | string | ansi-string |
| 2     | data   | byte-array  |

## DataType (ENUM)

| value | enum   | desc        |
| ----- | ------ | ----------- |
| 0     | unknow | unknow      |
| 1     | string | ansi-string |
| 2     | data   | byte-array  |

