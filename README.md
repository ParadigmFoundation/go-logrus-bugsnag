# Logrus Bugsnag
This package is an internal Paradigm preconfigured logrus logger solution that provides integration with bugsnag.  The package relies on an environment variable (`BUGSNAG_APIKEY`) to integrate with bugsnag and the log formatter is pre-configured and may be overridden.

### Usage
The package will prepare a logrus logger with bugsnag reporting given the environment variable `BUGSNAG_APIKEY` is set with a valid key.

```go
    package example

    import "github.com/ParadigmFoundation/go-logrus-bugsnag/logger"

    var mainLogger = logger.New("main")

    func main() {
        mainLogger.Fatal("Crashed :(") // mainLogger can be used as any logrus.Logger
    }
```
