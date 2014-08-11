Mocha Tap Reporter
======================

This reporter generate TAP format report that works perfectly with Jenkins TAP plugin.

Usage
-------
```
npm install mocha-tap-reporter
mocha --reporter mocha-tap-reporter
```

Example Output
-------------
```
1..3
ok 1 this is test1
not ok 2 this is test2
#  AssertionError: 1 == 2
#      at Context.<anonymous> (/Volumes/Data/workspace/tests/test2.js:10:10)
#      at Test.Runnable.run (/Volumes/Data/workspace/tests/node_modules/mocha/lib/runnable.js:196:15)
#      at Runner.runTest (/Volumes/Data/workspace/tests/node_modules/mocha/lib/runner.js:373:10)
ok 3 this is test3 # SKIP
# tests 3
# pass 1
# fail 1
# skip 1
```

Jenkins TAP Plugin
-------------
If you use Jenkins TAP plugin together, make sure the following option is enabled in your Jenkins jobs:
```
	Post-build Actions -> Publish TAP Results -> Include comment diagnostics (#) in the results table
```
Then you will find error stacktrace are avaiable in "TAP Extended Test Result".
