# Logger

Simple logging function that uses built in GO **Log** library.

## Table of Contents

1. [Usage](#usage)
    1. [Sample output](#sample-output)
2. [License](#license)
2. [Authors](#authors)

## Usage

```go
logger.Log{
	LogMessage: "Short log message", // This message will always be printed
	Message:    "Long log message", // This message only prints if the debug flags is set to true.
	                           // This can be integrated with the debug flag of the parent application.
}
```

```go
import "github.com/praveenprem/logger"

......

func main() {
	logger.DebugEnabled = true
	logger.Warning(logger.Log{LogMessage:"Short log message", Message:"Long log message"})

	logger.DebugEnabled = false

	var log logger.Log
	log.LogMessage = "Short log message"
	log.Message = "Long log message"

	logger.Error(log)
}
```

### Sample output
```
2019/05/06 20:42:25 WARNING: Short log message
2019/05/06 20:42:25 DEBUG: Long log message
2019/05/06 20:42:25 ERROR: Short log message

Process finished with exit code 1
```

#### Notes

licensed under the MIT License, please refer to the [LICENSE](LICENSE) for more details.

## License

## Authors
   | <div><a href="https://github.com/praveenprem"><img width="200" src="https://avatars3.githubusercontent.com/u/23165760"/><p></p><p>Praveen Premaratne</p></a></div> |
   | :-------: |
