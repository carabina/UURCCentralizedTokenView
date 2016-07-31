# UURCCentralizedTokenView

Customizable Centralized TokenView 

You can run *`pod install`*. And run example app to understand usage of this library.

# Installation
## Manaully
Add *`UURCCentralizedTokenView.h`* and *`UURCCentralizedTokenView.m`*  files to your project.

## CocoaPods
Add the following to your `Podfile`
````ruby
pod 'UURCCentralizedTokenView'
use_frameworks!
````

# Usage

Import the *`UURCCentralizedTokenView`* library to your *`ViewController`*.  
````objective-c
#import <UURCCentralizedTokenView/UURCCentralizedTokenView.h>
````

Create an instance *`UURCCentralizedTokenView`* class with token array. Then, set style of *`UURCCentralizedTokenView`* UI object.

````objective-c
self.tokenView = [[UURCCentralizedTokenView alloc] initWithTokenArray:tokenArray];
self.tokenView.parentViewController = self;
[self.view addSubview:self.tokenView];

// set token view Style
self.tokenView.tokenEdgeInsets = UIEdgeInsetsMake(8, 10, 8, 10);
self.tokenView.unselectedTokenTitleColor = [UIColor colorWithRed:0.72 green:0.11 blue:0.11 alpha:1.0];
self.tokenView.selectedTokenTitleColor = [UIColor colorWithRed:0.72 green:0.11 blue:0.11 alpha:1.0];
self.tokenView.selectedTokenColor = [UIColor colorWithRed:1.00 green:0.94 blue:0.67 alpha:1.0];
self.tokenView.selectedTokenBorderColor = [UIColor colorWithRed:1.00 green:0.94 blue:0.67 alpha:1.0];
self.tokenView.unselectedTokenBorderColor = [UIColor colorWithRed:0.72 green:0.11 blue:0.11 alpha:1.0];
````

You can detect selected token with *`UURCCentralizedTokenViewDelegate`* delegate method which is *`actionToken`*.

````objective-c
- (void)actionToken:(NSNumber *)tokenIndex {
    [self.tokenView setTokenSelected:tokenIndex];
    NSLog(@"%@",tokenIndex);
}
````

# Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request..


# License

UURCCentralizedTokenView is under MIT license.
Copyright © 2016-present Ugur Cetinkaya.
