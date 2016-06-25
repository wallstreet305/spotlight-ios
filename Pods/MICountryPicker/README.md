# MICountryPicker

MICountryPicker is a country picker controller for iOS8+ with an option to search. The list of countries is based on the ISO 3166 country code standard (http://en.wikipedia.org/wiki/ISO_3166-1). Also and the library includes a set of 250 public domain flag images from https://github.com/pradyumnad/Country-List.

## Screenshots

![alt tag](https://github.com/mustafaibrahim989/MICountryPicker/blob/master/screen1.png) ![alt tag](https://github.com/mustafaibrahim989/MICountryPicker/blob/master/screen2.png)

## Installation

MICountryPicker is available through [CocoaPods](http://cocoapods.org), to install
it simply add the following line to your Podfile:
  
    use_frameworks!
    pod 'MICountryPicker'

Show MICountryPicker from UIViewController

```swift

let picker = MICountryPicker()
navigationController?.pushViewController(picker, animated: true)

```
## MICountryPickerDelegate protocol

```swift

// delegate
picker.delegate = self

```

```swift

func countryPicker(picker: MICountryPicker, didSelectCountryWithName name: String, code: String) {
        print(code)
}

```

## Closure

```swift

// or closure
picker.didSelectCountryClosure = { name, code in
        print(code)
}

```

## Author

Mustafa Ibrahim, mustafa.ibrahim989@gmail.com

Notes
============

Designed for iOS 8+.

## License

MICountryPicker is available under the MIT license. See the LICENSE file for more info.
