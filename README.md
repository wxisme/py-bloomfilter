# py-bloomfilter
bloomfilter written in python</br>

you can also refer to [java version](https://github.com/wxisme/bloomfilter)

# Test example

## BitSet

```python
from common.bloomfilter import BloomFilter
from bitset.bitset import BitSet
bloomfilter = BloomFilter(0.001, 10000, BitSet())
bloomfilter.add('123')
print(bloomfilter.contains('123'))
print(bloomfilter.contains('456'))
```
Test result:
```
True</br>
False</br>
```

## RedisBitSet

```python
from common.bloomfilter import BloomFilter
from bitset.redis_bitset import RedisBitSet
bloomfilter2 = BloomFilter(0.001, 10000, RedisBitSet())
bloomfilter2.add('123')
print(bloomfilter2.contains('123'))
print(bloomfilter2.contains('456'))
```
Test result:
```
True</br>
False</br>
```

## Extension

In addition, you can extend any data structure you want to use.</br>
All you need to do is inherit the function of BaseBitSet and override it.</br>

# License

py-bloomfilter is released under the [GNU Lesser General Public License v3.0](http://www.gnu.org/licenses/).
You may copy this code directly into your project if you leave the LGPL-comment in place and reference the following hyperlink:
https://github.com/wxisme/py-bloomfilter

