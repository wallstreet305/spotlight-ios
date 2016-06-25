# iShowcase

Highlight individual parts of your application using iShowcase

[![CI Status](http://img.shields.io/travis/rahuliyer95/iShowcase.svg?style=flat)](https://travis-ci.org/rahuliyer95/iShowcase)
[![Version](https://img.shields.io/cocoapods/v/iShowcase.svg?style=flat)](http://cocoadocs.org/docsets/iShowcase)
[![License](https://img.shields.io/cocoapods/l/iShowcase.svg?style=flat)](http://cocoadocs.org/docsets/iShowcase)
[![Platform](https://img.shields.io/cocoapods/p/iShowcase.svg?style=flat)](http://cocoadocs.org/docsets/iShowcase)
[![Issues](https://img.shields.io/github/issues/rahuliyer95/iShowcase.svg?style=flat)](http://www.github.com/rahuliyer95/iShowcase/issues?state=open)

## Screenshots

<img style="float : left" src="screenshot/1.png" width="320" height="568">
<img style="float : right" src="screenshot/2.png" width="320" height="568">
<img style="float : left" src="screenshot/3.png" width="320" height="568">
<img style="float : right" src="screenshot/4.png" width="320" height="568">

## Requirements
* Xcode 5 or higher
* Apple LLVM compiler
* iOS 6.0 or higher
* ARC

## Installation

iShowcase is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

    pod "iShowcase", "~> 1.5"

or

### Objective-C

  * Add the `iShowcase.h` and `iShowcase.m` from Objective-C folder to your project
  * Add `#include "iShowcase.h"` to your ViewController

### Swift
  * Add `iShowcase.swift` file to your project

## [Documentation](http://rahuliyer95.github.io/iShowcase/docs)

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

#### Creating Instance

##### Objective-C
``` objective-c
// Create Object of iShowcase
iShowcase *showcase = [[iShowcase alloc] init];

// Other init Methods
initWithTitleFont: (UIFont*) titleFont detailsFont: (UIFont*) detailsFont;
initWithTitleColor: (UIColor*) titleColor detailsColor: (UIColor*) detailsColor;
```

##### Swift
``` swift
// Create Object of iShowcase
let showcase = iShowcase()

// Other init Methods
let showcase = iShowcase(
        withTitleFont: UIFont?,
        withDetailsFont: UIFont?,
        withTitleColor: UIColor?,
        withDetailsColor: UIColor?,
        withBackgroundColor: UIColor?,
        withHighlightColor: UIColor?,
        withIType iType: TYPE?)
````

#### Delegate

``` objective-c
showcase.delegate = self;
```
#### Delegate Methods

``` objective-c
iShowcaseShown // Called When Showcase is displayed
iShowcaseDismissed // Called When Showcase is removed
```

#### Displaying iShowcase

##### Objective-C
``` objective-c
[showcase setupShowcaseForView:(UIView *) title:(NSString *) details:(NSString *)];
[showcase show];

// For Custom Location
[showcase setupShowcaseForLocation:(CGRect location) title:(NSString *) details:(NSString *)];
[showcase show];

// Methods for other UI Elements

setupShowcaseForBarButtonItem:(UIBarButtonItem *) withTitle:(NSString *) details:(NSString *)
setupShowcaseForTableView:(UITableView *) withTitle:(NSString *) details:(NSString *)
setupShowcaseForTableView:(UITableView *) withIndexOfItem:(NSUInteger) sectionOfItem:(NSUInteger) title:(NSString *) details:(NSString *)

```

###### Swift

``` swift
showcase.setupShowcase(forView: UIView, withTitle: String, detailsMessage: String)
showcase.show()

// For custom location

setupShowcase(forLocation: CGRect, withTitle: String, detailsMessage: String)

// Methods for other UI Elements

setupShowcase(forTableView: UITableView, withTitle: String, detailsMessage: String)
setupShowcase(forTableView: UITableView, withIndexOfItem: Int, setionOfItem: Int, withTitle: String, detailsMessage: String)
setupShowcase(forBarButtonItem: UIBarButtonItem, withTitle: String, detailsMessage: String)
```

#### Customizations

##### Objective-C
``` objective-c

// Constants
const int TYPE_CIRCLE = 0;
const int TYPE_RECTANGLE = 1;

setBackgroundColor: (UIColor *) backgroundColor;
setTitleFont: (UIFont*) font;
setDetailsFont: (UIFont*) font;
setTitleColor: (UIColor*) color;
setDetailsColor: (UIColor*) color;
setHighlightColor:(UIColor*) highlightColor;
setIType: (int) type;
setRadius: (CGFloat) radius;
setSingleShotId: (long) singleShotId;
```

##### Swift
``` swift
public enum TYPE: Int {
    case CIRCLE = 0
    case RECTANGLE = 1
}

titleFont: UIFont
detailsFont: UIFont
titleColor: UIColor
detailsColor: UIColor
highlightColor: UIColor
iType: TYPE
titleTextAlignment: NSTextAlignment
detailsTextAlignment: NSTextAlignment
radius: Float
singleShotId: Int64

```

## Credits

Inspired from [ShowcaseView](https://github.com/amlcurran/Showcaseview) by [Alex Curran](https://github.com/amlcurran/)

## Author

rahuliyer95, rahuliyer573@gmail.com

## License

iShowcase is available under the MIT license. See the LICENSE file for more info.
