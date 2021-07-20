[![npm version](https://img.shields.io/npm/v/winston-log-viewer.svg?style=flat)](https://www.npmjs.com/package/winston-log-viewer)

**Winston-log-viewer** is npm CLI package for pretty printing winston log files, the file log should be in this format:
```
{"level":"info","Trying to create user","params":[{"name":"mohammad"}],"timestamp":"2021-07-19T13:30:44.185Z"}
{"level":"debug","It's better to user have age","timestamp":"2021-07-19T13:30:44.185Z"}
{"level":"error","message":"user's name should be unique","params":[{"name":"mohammad"}],"timestamp":"2021-07-19T13:32:22.286Z"}
```

### Usage
* `npm i -g winston-log-viewer`
* `tail -f logFile.log | winston-log-viewer`
Or
* `tail -f logFile.log | npx winston-log-viewer`

PS: if you want to test package locally after clone you can run this command `tail -f winston-sample.log | ./bin/winston-log-viewer`
Manifesto: Server logs should be structured. JSON's a good format. Let's do
that. A log record is one line of `JSON.stringify`'d output. Let's also
specify some common names for the requisite and common fields for a log
record (see below).

It's written based on [Bunyan CLI for pretty printing log files](https://github.com/trentm/node-bunyan/blob/master/bin/bunyan)

