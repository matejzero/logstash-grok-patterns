Logstash grok patterns for various services
==========================================
A set of grok patterns for parsing various services logging using grok.


Tests
-----
[![Build Status](https://travis-ci.org/matejzero/logstash-grok-patterns.svg?branch=master)](https://travis-ci.org/matejzero/logstash-grok-patterns)

In the `test/` directory, there is a test suite that tries to make sure that no previously supported log line will break because of changing common patterns and such. It also returns results a lot faster than doing `sudo service logstash restart` :-).

The test suite needs the patterns provided by Logstash, you can easily pull these from github by running `git submodule update --init`. To run the test suite, you also need `ruby 1.9` and the `jls-grok` gem. Then simply execute `ruby test/test.rb`.

Adding new test cases can easily be done by creating new yaml files in the test directory. Each file specifies a grok pattern to validate, a sample log line, and a list of expected results.

Other
-----
Postfix grok patterns and tests are from https://github.com/whyscream/postfix-grok-patterns/

Acknowledgement
---------------
I'm using latest logstash-grok-patterns module, latest elasticsearch and latest kibana in order to get evertyhing working.
For writing the grok patterns I depend heavily on [grokdebug](https://grokdebug.herokuapp.com/)