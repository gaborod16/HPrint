## Hierarchical Colored Logger Module for Python

HCLogger is a logging module using [Termcolor](https://pypi.org/project/termcolor/) and a hierarchical format to improve readability.

Note: this module was implemented to deal with concurrency. However, it is encouraged to store threads logs into a different log files.

![HCLogger capture][HCLogger]
[HCLogger]: hclogger/tests/function_test.png "HCLogger's looks"

### Installation

Not yet in PyPi.

### Usage

As simple as it could be:

```python
from HCLogger import Logger

logger = Logger(filename='fname.log', verbose=False)
logger.debug('This is a debug message.')
```
![Debug output][debug_message]
[debug_message]: hclogger/tests/debug_message.png

The hierarchy is added to functions. In order to add hierarchy on of the following alternatives must be used:

```python
# The manual call
logger.manual_log_func(func, args*)

# The decorated call
@logger.log_func
def func(args):
	...

func()
```

![Function logging][function_log]
[function_log]: hclogger/tests/function_log.png

Putting it all together:
![Demo capture][demo_capture]
[demo_capture]: hclogger/tests/demo_capture.png "Demo"

## Future work

 - [ ] Add to PyPi
 - [ ] Create web view