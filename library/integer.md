---
title: "Standard library: Integer methods"
header: /library
layout: default
---
# Integer methods

Integers are one of three types in the Sentient programming language. This
document contains a reference of all integer operators and methods.

##### <a id="+"></a> [+ (operator)](#+)

Performs addition.

```sentient
5 + 3    #=> 8
```

##### <a id="-"></a> [- (operator)](#-)

Performs subtraction.

```sentient
5 - 3    #=> 2
```

##### <a id="*"></a> [\* (operator)](#*)

Performs multiplication.

```sentient
5 * 3    #=> 15
```

##### <a id="/"></a> [/ (operator)](#/)

Returns the quotient after division. See [**divmod**](#divmod).

##### <a id="%"></a> [% (operator)](#%)

Returns the remainder after division. See [**divmod**](#divmod).

##### <a id="-@"></a> [-@ (operator)](#-@)

Performs unary negation.

```sentient
-(2 + 2)    #=> -4
```

##### <a id="=="></a> [== (operator)](#==)

Returns **true** if the integer on the left is equal to the right.

```sentient
2 == 2    #=> true
2 == 3    #=> false
```

##### <a id="!="></a> [!= (operator)](#!=)

Returns **true** if the integer on the left is not equal to the right.

```sentient
2 != 2    #=> false
2 != 3    #=> true
```

##### <a id="<"></a> [< (operator)](#<)

Returns **true** if the integer on the left is less than the right.

```sentient
2 < 1    #=> false
2 < 2    #=> false
2 < 3    #=> true
```

##### <a id="<="></a> [<= (operator)](#<=)

Returns **true** if the integer on the left is less than or equal to the right.

```sentient
2 <= 1    #=> false
2 <= 2    #=> true
2 <= 3    #=> true
```

##### <a id=">"></a> [> (operator)](#>)

Returns **true** if the integer on the left is greater than the right.

```sentient
2 > 1    #=> true
2 > 2    #=> false
2 > 3    #=> false
```

##### <a id=">="></a> [>= (operator)](#>=)

Returns **true** if the integer on the left is greater than or equal to the right.

```sentient
2 >= 1    #=> true
2 >= 2    #=> true
2 >= 3    #=> false
```

##### <a id="abs"></a> [abs](#abs)

Returns the absolute value of the integer.

```sentient
5.abs    #=> 5
-5.abs   #=> 5
```

##### <a id="between?"></a> [between?](#between?)

Returns **true** if the integer is between two integers (inclusive).

```sentient
3.between?(1, 5)
#=> true

5.between?(1, 5)
#=> true

6.between?(1, 5)
#=> false
```

The order of arguments does not matter:

```sentient
3.between?(5, 1)
#=> true
```

##### <a id="cube"></a> [cube](#cube)

Returns the cube of the integer.

```sentient
3.cube    #=> 27
```

##### <a id="divmod"></a> [divmod](#divmod)

Performs integer Euclidean division, returning both quotient and remainder.

```sentient
a, b = 9.divmod(2)    # a: 4, b: 1
```

The divisor must not be zero, else the program will have no solutions.

##### <a id="downto"></a> [downto](#downto)

Iterates from a start integer downto an end integer.

```sentient
total = 0;

5.downto(3, function^ (i) {
  total += i;
});

# total: 12
```

This method only supports [integer literals](../library/literals).

##### <a id="even?"></a> [even?](#even?)

Returns **true** if the integer is even.

```sentient
0.even?    #=> true
1.even?    #=> false
2.even?    #=> true
```

##### <a id="negative?"></a> [negative?](#negative?)

Returns **true** if the integer is less than zero.

```sentient
-1.negative?    #=> true
0.negative?     #=> false
```

##### <a id="next"></a> [next](#next)

Alias for [**succ**](#succ).

##### <a id="odd?"></a> [odd?](#odd?)

Returns **true** if the integer is odd.

```sentient
0.odd?    #=> false
1.odd?    #=> true
2.odd?    #=> false
```

##### <a id="positive?"></a> [positive?](#positive?)

Returns **true** if the integer is greater than zero.

```sentient
1.positive?     #=> true
0.positive?     #=> false
```

##### <a id="pred"></a> [pred](#pred)

Returns the integer's predecessor.

```sentient
3.pred    #=> 2
```

##### <a id="prev"></a> [prev](#prev)

Alias for [**pred**](#pred).

##### <a id="self"></a> [self](#self)

Returns the integer.

```sentient
123.self
#=> 123
```

##### <a id="square"></a> [square](#square)

Returns the square of the integer.

```sentient
3.square    #=> 9
```

##### <a id="succ"></a> [succ](#succ)

Returns the integer's successor.

```sentient
3.succ    #=> 4
```

##### <a id="times"></a> [times](#times)

Iterates up to one less than the integer, starting from 0.

```sentient
total = 0;

5.times(function^ (i) {
  total += i;
});

# total: 10
```

This method only supports [integer literals](../library/literals).

##### <a id="upto"></a> [upto](#upto)

Iterates from a start integer upto an end integer.

```sentient
total = 0;

3.upto(5, function^ (i) {
  total += i;
});

# total: 12
```

This method only supports [integer literals](../library/literals).

##### <a id="zero?"></a> [zero?](#zero?)

Returns **true** if the integer is zero.

```sentient
0.zero?    #=> true
1.zero?    #=> false
```
