# MathProbability

[![Build Status](https://travis-ci.org/polysaturate/math_probability.png?branch=master)](https://travis-ci.org/polysaturate/math_probability)
[![Coverage Status](https://coveralls.io/repos/polysaturate/math_probability/badge.png?branch=master)](https://coveralls.io/r/polysaturate/math_probability?branch=master)
[![Code Climate](https://codeclimate.com/github/polysaturate/math_probability.png)](https://codeclimate.com/github/polysaturate/math_probability)

Quickly find factorals, summations, permutations, combanations and probability answers

## Installation

Add this line to your application's Gemfile:

    gem 'math_probability'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install math_probability

## Usage
General Usage:

    5.factoral
    => 120
    prob = MathProbability::Probability
    
Sigma(Summation) | Usage: sigma(start, end, formula)

    prob.sigma(1,4,"4*x-3")
    => 28
    
Permutation without repeating | Usage permutation_no_repeat(objects, at_a_time)

    prob.permutations_no_repeat(8,5)
    => 6720
    
Permutation with repeating | Usage permutation_no_repeat(objects, at_a_time)

    prob.permutations_with_repeat(8,5)
    => 32768
    
Combinations | Usage combinations(objects, at_a_time)

    prob.combinations(10,4)
    => 210
    
Probability | Usage probability(choices, outcomes, reduce=true)

    prob.probability(1,4)
    => {:decimal=> 0.25, :percentage=>"25.0%", :fraction=>"1/4"}
    prob.probability(2,4)
    => {:decimal=> 0.5, :percentage=>"50.0%", :fraction=>"1/2"}
    prob.probability(2,4,false)
    => {:decimal=> 0.5, :percentage=>"50.0%", :fraction=>"2/4"}
    
## Running tests

    $ git clone git://github.com/polysaturate/math_probability.git
    $ bundle install
    $ rake   

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
