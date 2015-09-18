# logstash-grok-patterns
grok patterns for use with logstash


Tests
-----

[![Build Status](https://travis-ci.org/matejzero/logstash-grok-patterns.svg?branch=master)](https://travis-ci.org/matejzero/logstash-grok-patterns)

In the `test/` directory, there is a test suite that tries to make sure that no previously supported log line will break because of changing common patterns and such. It also returns results a lot faster than doing `sudo service logstash restart` :-).

The test suite needs the patterns provided by Logstash, you can easily pull these from github by running `git submodule update --init`. To run the test suite, you also need `ruby 1.9` and the `jls-grok` gem. Then simply execute `ruby test/test.rb`.

Adding new test cases can easily be done by creating new yaml files in the test directory. Each file specifies a grok pattern to validate, a sample log line, and a list of expected results.