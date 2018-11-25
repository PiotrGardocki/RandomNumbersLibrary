# RandomNumbersLibrary
RandomNumbersLibrary is a simple c++ library created for convenient generating random numbers.
Library supports generating both integer and real types.

Library is based on c++ libraries ```random``` and ```chrono```.
It was made to avoid creating number engines and creating seed from current time.
It automatically creates engine with seed for any thread that tries to generate random number.

That means, **all of threads have their own engines with different seeds**.

### Generators
There are two numbers generators: ```RandomIntegerGenerator<T>``` and ```RandomRealNumberGenerator<T>```.
Both **templates allow only c++ built-in integer and real number types**.

### Usage

```c++
/// including library
#include "RandomNumbers/RandomIntegerGenerator.hpp"
#include "RandomNumbers/RandomRealNumberGenerator.hpp"

/// creating generators
RandomIntegerGenerator<int> randomInt(-10, 10);
RandomRealNumberGenerator<double> randomReal(-10., 10.);

/// setting new range
randomInt.setNewRange(0, 20);
std::pair<int, int> newRange(10, 30;
randomInt.setNewRange(newRange);

/// checking range
randomReal.getMin();
randomReal.getMax();
randomReal.getRange();

/// generating numbers
int var;
var = randomInt.generateRandom();
// or
var = randomInt();
```