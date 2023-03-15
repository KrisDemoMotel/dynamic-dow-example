# dynamic-dow-example
An example of how we can have different configurations run, depending on day of week, time of week, etc.

## How it works

As we start the workflow, we check for the day of week and time of day using the `date` command. Depending on the results - if it's before Friday (day 5) or Saturday (day 6), and between the hours of 8 AM and 6 PM, we will run a configuration that does not include a hold step. Otherwise, we run a similar configuration, but it includes a hold step.

### Things to add

Currently this is not a very DRY setup, as the two configs are completely seperate. Ideally, we should instead have it so that it modifies the workflow to add a hold step.

The timezone should be confirmed so it can comply with your requested one
