This is a reproduction of a hard to trace raven bug in `TraceKit.computeStackTrace` where when
passed a valid error object it will return `{}` which results in sentry getting an entry added
with message of `undefined` and stack of `undefined` and makes tracking down this bug incredibly
difficult.