## 1. FAT Main Memory Requirements
a)  250 * 1024^2 = 262144000 blocks because block size is 1KB

b)  262144000 entries

c)  On table entrie must be 32 bit

d)  262144000*4*2 = 2097152000 / 1024 / 1024 / 1024 = 1,9 GB

## 2. Random Access of Files
a) We calculate: 10 * 1024 + 256 * 1024 + 256 * 1024 * 1024 = 268707840 and 107834590 is in 268707840, \
  so we know it is in the double indirect block but I dont know further :)

b) We take the first block-reference in the FAT table and then we need to \
  go futher 107.834.590 times in the FAT to get to the block we want

## 3. UFS (i-node) File Size
  For 4KB: \
    10 * 4096 + 4096 * 1024 + 4096 * 1024 * 1024 + 4096 * 1024 * 1024 * 1024 = 4TB
  For 1KB: \
    10 * 1024 + 1024 * 256 + 1024 * 256 * 256 + 1024 * 256 * 256 * 256 = 17,2GB

## 4. UFS File Size
a)  512 byte is not sufficient because the maximum file size could just be 1GB \
  For 512 bytes:\
    10 * 512 + 512 * 128 + 512 * 128 * 128 + 512 * 128 * 128 * 128 = 1082201088 byte = 1GB

b)  It wont change the fact that we should use 1024, because 12 GB is still fitting into 17,2GB \
  For 1024 bytes: \
    10 * 1024 + 1024 * 256 + 1024 * 256 * 256 + 1024 * 256 * 256 * 256 = 17247240192 byte = 17,2GB
