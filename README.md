# DMLPhotoBrowser

[![CI Status](http://img.shields.io/travis/MrDML/DMLPhotoBrowser.svg?style=flat)](https://travis-ci.org/MrDML/DMLPhotoBrowser)
[![Version](https://img.shields.io/cocoapods/v/DMLPhotoBrowser.svg?style=flat)](http://cocoapods.org/pods/DMLPhotoBrowser)
[![License](https://img.shields.io/cocoapods/l/DMLPhotoBrowser.svg?style=flat)](http://cocoapods.org/pods/DMLPhotoBrowser)
[![Platform](https://img.shields.io/cocoapods/p/DMLPhotoBrowser.svg?style=flat)](http://cocoapods.org/pods/DMLPhotoBrowser)

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements&&demonstration
![Demo](https://github.com/MrDML/DMLPhotoBrowser/blob/master/photo.gif)


## Installation

DMLPhotoBrowser is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'DMLPhotoBrowser'
```

## Use
```
(注意此框架依赖 FLAnimatedImage和SDWebImage，具体如何使用请查看demo)
    NSMutableArray *photoItems = [NSMutableArray array];
    int i = 0;
    for (UIImage *image in self.images) {
        
        UIImageView *imageViewSource = self.bgview.subviews[i];
        DMLPhotoItem *item = [[DMLPhotoItem alloc] initWithSourceView:imageViewSource image:image];
        [photoItems addObject:item];
        i ++;
    }
    
    DMLPhotoBrowser *Browser = [[DMLPhotoBrowser alloc] initWithPhotoItems:photoItems selectedIndex:imageView.tag];
    
    [Browser showPhotoBrowser];

```

## Author

NickName:MrDML, E-Mail:dml1630@163.com, QQ:1969339388

## License

DMLPhotoBrowser is available under the MIT license. See the LICENSE file for more info.
