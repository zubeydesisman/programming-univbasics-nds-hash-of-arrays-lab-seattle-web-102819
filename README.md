# Hash of Arrays

## Learning Goals

1. Recognize vocabulary term: "hash of arrays"
2. Create a `Hash` of `Array`s
3. Read scalar data from a `Hash` of `Array`s
4. Modify scalar data in a `Hash` of `Array`s

## Introduction

The final "basic" nested structure is the `Hash` of `Array`s.

### Key Image: Result Set

The key image is to think of a result set. You might think of it as a weather
report where you sample a measurement multiple times per day. You might track
`:temperature` at midnight, noon, and 6:00 p.m. Or you might track an
insulin level every two hours as an `Array` pointed to by the key
`:insulin_level`.

## Recognize Vocabulary Term: "Hash of Arrays"

"`Hash` of `Array`s" is an infrequently used term. As you get more experienced
with Ruby, it's typical to merely know that a `Hash`'s key might point to a
scalar value (`1.0`, `"Smith"`) or to an `Array`. While we're starting out with
learning Ruby, though, let's briefly take time to acknowledge that it exists.

If a colleague suggests storing the data as a `Hash` of `Array`s, you'll know
what to code.

## Create a `Hash` of `Array`s

It's most common to create `Hash` of `Array`s in the "literal" format.
Here's a "result set:"

```ruby
daily_weather = {
  temperature: [75, 80, 72],
  precipitation: [0.0, 0.01, 0.03]
  wind_velocity: [4, 3, 2]
  barometric_pressure: [30.32, 30.30, 30.20]
}
```

## Read Scalar Data from a `Hash` of `Array`s

To read data from a `Hash` of `Array`s we provide:

1. A key name
2. An index

```ruby
daily_weather = {
  temperature: [75, 80, 72],
  precipitation: [0.0, 0.01, 0.03]
  wind_velocity: [4, 3, 2]
  barometric_pressure: [30.32, 30.30, 30.20]
}

# Addition
daily_weather[:temperature][2] #=> 72

# Access the whole Array
daily_weather[:temperature] #=> [75, 80, 72]

```

## Modify scalar data in a `Hash` of `Array`s

Again, providing a key and an index will let you modify the inner `Array`s:

```ruby
daily_weather = {
  temperature: [75, 80, 72],
  precipitation: [0.0, 0.01, 0.03]
  wind_velocity: [4, 3, 2]
  barometric_pressure: [30.32, 30.30, 30.20]
}

daily_weather[:temperature][2] = 74 #=> 74
daily_weather[:temperature][2] #=> 74
```

## Conclusion

This concludes our learning of the "basic" nested data structures

* Arrays of Arrays
* Arrays of Hashes
* Hashes of Hashes
* Hashes of Arrays

By mixing these four "basic" nested data structures, we can build complex data
structures that can be "mixed" to model our world's complexity as a data
structure from which Ruby can help us generate _insights_.
