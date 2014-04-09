ti.timelogger
=============

`ti.timelogger` is a CommonJS module for Titanium, which allows you to print out detailed logs to debug your application.

How to use
----------

To use the logger, simply require it in your application, and create a new instance of the logger. You can provide a custom ID for the logger, or leave it empty to get the ID "default".

~~~
var TiTimeLogger = require("ti.timelogger");

var Logger = new TiTimeLogger("mylogger");
~~~

Once the logger is created, you can print out a log by simply using the methods `log`, `info`, `warn` or `error`.

~~~
Logger.info("This is a simple info log");
Logger.error("This is an error");
~~~

Log format
----------

The logger will print out several information in the log line. This is the format used:

[TimeLogger][LOGGERID][LINENUMBER][TIMESTAMP][MSPASSED]: MESSAGE

- **TimeLogger**: A fixed string "TimeLogger".
- **LOGGERID**: This is the ID of the logger, set when the logger was created.
- **LINENUMBER**: The logger will try to guess the line where the log was called.
- **TIMESTAMP**: The current timestamp of the system.
- **MSPASSED**: The number of milliseconds passed since the previous call.
- **MESSAGE**: The message passed in the `log`, `info`, `warn` or `error` methods.
