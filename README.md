# path undefined error

From node_mobules/.bin/cucumberjs
```bash
$ node_modules/.bin/cucumberjs
Feature: Example

  Scenario: Things
  ? When something happens
  ? Then things pass

Warnings:

VError: a handler errored, process exiting: PrettyFormatter::handleFeaturesResult: Path must be a string. Received undefined
    at /Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/runtime/event_broadcaster.js:78:21
    at next (native)
    at tryCatcher (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/util.js:16:23)
    at PromiseSpawn._promiseFulfilled (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/generators.js:97:49)
    at Async._drainQueue (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/async.js:138:12)
    at Async._drainQueues (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/async.js:143:10)
    at Immediate.Async.drainQueues (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/async.js:17:14)
    at runCallback (timers.js:574:20)
    at tryOnImmediate (timers.js:554:5)
    at processImmediate [as _immediateCallback] (timers.js:533:5)
caused by: TypeError: Path must be a string. Received undefined
    at assertPath (path.js:7:11)
    at Object.relative (path.js:1229:5)
    at formatLocation (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/formatter/utils.js:18:25)
    at PrettyFormatter.logIssue (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/formatter/summary_formatter.js:200:58)
    at /Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/formatter/summary_formatter.js:236:16
    at Array.forEach (native)
    at PrettyFormatter.logIssues (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/formatter/summary_formatter.js:235:19)
    at PrettyFormatter.handleFeaturesResult (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/formatter/summary_formatter.js:139:14)
    at Function.<anonymous> (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/user_code_runner.js:59:25)
    at next (native)
    at tryCatcher (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/util.js:16:23)
    at PromiseSpawn._promiseFulfilled (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/generators.js:97:49)
    at Function.<anonymous> (/Users/omargonzalez/code/experiments/cukes/node_modules/bluebird/js/release/generators.js:201:15)
    at Function.run (/Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/user_code_runner.js:118:22)
    at /Users/omargonzalez/code/experiments/cukes/node_modules/cucumber/lib/runtime/event_broadcaster.js:68:58
    at next (native)

```


From -g cucumber
```bash
$ cucumberjs 
Feature: Example

  Scenario: Things
  ? When something happens
  ? Then things pass

Warnings:

1) Scenario: Things - features/example.feature:2
   Step: When something happens - features/example.feature:3
   Message:
     Undefined. Implement with the following snippet:

       When('something happens', function (callback) {
         // Write code here that turns the phrase above into concrete actions
         callback(null, 'pending');
       });

2) Scenario: Things - features/example.feature:2
   Step: Then things pass - features/example.feature:4
   Message:
     Undefined. Implement with the following snippet:

       Then('things pass', function (callback) {
         // Write code here that turns the phrase above into concrete actions
         callback(null, 'pending');
       });

1 scenario (1 undefined)
2 steps (2 undefined)
0m00.000s
```