Used in [[Star topology]]

Smart device, maintains a MAC table.

| Port Number | Mac address |
| ----------- | ----------- |
|           1  |A             |
|            2 | NA            |
| 3            |  NA           |
|  4           |   D          |
| 5           |    E        |

### 1st Gen
The Mac table is populated slowly, if the destination mac isn't in the table, send to all unknown macs, then populate
Afterwards, send only to the destination mac if exist, else don't send

### 2nd Gen
Sends an eco request to all ports every 30s, populating the entire mac table instantly.
Purpose of this is to not `SEND TO ALL UNKNOWN MACS`, because it is a very costly operation, and router has a max transfer speed.