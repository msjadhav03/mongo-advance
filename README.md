# Database Profiling

- # Setting Profile Status
```js
db.setProfilingLevel( 2, { filter: { op: "query", millis: { $gt: 2000 } } } )
```
-  `2` : Profiling Level, 
- `{ op: "query", millis: { $gt: 2000 } } ` :  profiler to only log query operations that took longer than 2 seconds.


# Getting Profile Status

- getProfileStatus()
```js
db.getProfilingStatus()
```

# Disabling Profile Status

```js
db.setProfilingLevel(0)
```

# Getting Profile Report

```js
db.system.profile.find()
```

# Getting Latest 5 Most Recent Events

```js
show profile
```

# References
[MongoDB Database Profiling](https://www.mongodb.com/docs/manual/tutorial/manage-the-database-profiler/)
















# Performance Advisor
- Premimum Plan
- Performance Advisor doesn’t suggest indexes that have more than 16 fields.
- The Performance Advisor lists recommended indexes in order of performance
- Provides suggestion for 
- indexes
    1. Unused
    2. Hidden
    3. Redudant
    4. 
- Indexes - rolling fashion index, 
- Collation - Lanuguage specific - rules for comparison
```js
db.setProfiling() # set threshold
```
or 
```js
db.runCommand({
  profile: 0,
  slowms: 200
})
```
- set threshold -  Performance Advisor doesn’t suggest indexes that have more than 16 fields.
- The Performance Advisor doesn’t suggest indexes that have more than 16 fields
- Performance Advisor, redundant indexes are marked with a red Redundant badge.

- indexes
    1. Unused
    2. Hidden - Hiding an index is useful for evaluating the impact of removing an index before doing so.
    3. Redudant
    4. 
# Data Explorer

- Data Explorer doesn’t support building indexes in a rolling fashion for standalone deployments.
- Ops Manager - automation, monitoring, backup
