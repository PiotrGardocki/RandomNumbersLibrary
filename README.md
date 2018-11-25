# RandomNumbersLibrary
RandomNumbersLibrary is a simple c++ library created for convenient generating random numbers. Library supports generating both integer and real types.

### Generators
There are two numbers generators: ```RandomIntegerGenerator<T>``` and ```RandomRealNumberGenerator<T>```.
Both templates allow only c++ built-in integer and real number types.

### Usage

```c++
/// creating generators
RandomIntegerGenerator<int> randomInt(-10, 10);
RandomRealNumberGenerator<double> randomReal(-10., 10.);

/// setting new range
randomInt.setNewRange(0, 20);

/// checking range
randomReal.getMin();
randomReal.getMax();

/// generating numbers
int var;
var = randomInt.generateRandom();
// or
var = randomInt();
```