# Logger

An application of Singleton pattern can be Logger. A Logger is something which is used to log the information pretty much any place of the system. An example code of the Logger would be:

```
class Logger {
  constructor() {
    if(!Logger.instance) {
      Logger.instance = this;
      this.logs = [];
    }
    return Logger.instance;
  }

  log(item) {
   this.logs.push(item);
  }
  
  getLogs() {
    return this.logs;
  }
}


const errorLogging = new Logger();
errorLogging.log("Error1");

const infoLogging = new Logger();
infoLogging.log("Info1");

const logs = infoLogging.getLogs();
console.log(logs); // ["Error1", "Info1"]

const logs2 = errorLogging.getLogs();
console.log(logs2); // ["Error1", "Info1"]

```
