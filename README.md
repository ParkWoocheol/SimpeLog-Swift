# SimpleLog-Swift

[![CI Status](http://img.shields.io/travis/Woocheol Park/SimpleLog-Swift.svg?style=flat)](https://travis-ci.org/Woocheol Park/SimpleLog-Swift)
[![Version](https://img.shields.io/cocoapods/v/SimpleLog-Swift.svg?style=flat)](http://cocoapods.org/pods/SimpleLog-Swift)
[![License](https://img.shields.io/cocoapods/l/SimpleLog-Swift.svg?style=flat)](http://cocoapods.org/pods/SimpleLog-Swift)
[![Platform](https://img.shields.io/cocoapods/p/SimpleLog-Swift.svg?style=flat)](http://cocoapods.org/pods/SimpleLog-Swift)

## Installation

SimpleLog-Swift is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "SimpleLog-Swift"
```

## Example

```swift
import SimpleLog_Swift

#if DEBUG
     Logging.isRunning = true
#else
     Logging.isRunning = false
#endif

// Print command line
// | 📘 DEBUG | FILE: .../ExampleViewController.swift, FUNCTION: exampleFunction, LINE: 30, MESSAGE:
Logging.d()

// Print command line
// | 📘 DEBUG | FILE: .../ExampleViewController.swift, FUNCTION: exampleFunction, LINE: 30, MESSAGE: description
Logging.d(description)

// Print command line
// | 📘 DEBUG | FILE: .../ExampleViewController.swift, FUNCTION: exampleFunction, LINE: 30, MESSAGE: description
// | 🗄 Array | Info -> [...], Size -> [...]
// | 🔓 INDEX | 0
// ---------------------------------------------------------
// Variable Name -> [id], Variable Type -> [Optional<Int>], Value -> [Optional(123)]
// ---------------------------------------------------------
// | 🔓 INDEX | 1
// ---------------------------------------------------------
// Variable Name -> [id], Variable Type -> [Optional<Int>], Value -> [Optional(456)]
// ---------------------------------------------------------
Logging.d(array as Array<Any>)

Logging.i(message: "description")
...

Logging.w(message: "description")
...

Logging.e(message: "description")
...
     
```


## Author

Woocheol Park, admin@mrparkwc.com

## License

SimpleLog-Swift is available under the MIT license. See the LICENSE file for more info.
