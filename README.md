step-iron-worker
================

# Iron Worker Step

Use the Iron Worker CLI to run, upload, queue and schedule workers in Iron.io. More info [here](http://dev.iron.io/worker/reference/cli/). This step assumes the iron.json and my_worker.worker files exist in the current executing direcotry.

# Options

* `worker-name` (required) Specify the name of the .worker file. For example, my_worker.worker would be worker-name: my_worker
* `cmd` (required) The iron_worker sub command to use. The iron_worker cli support run, upload, queue, schedule and log.
* `args` (optional) Arguments passed to the iron_worker command.

# Example

``` yaml
deploy:
    steps:
        - jlbribeiro/iron-worker:
            worker-name: my_worker
            cmd: upload
        	args: --env development --max-concurrency 10
```
