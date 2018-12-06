# iOSAutoLabel
iOS开发中,实现UILabel滚动,类似于跑马灯效果;

使用方法:

~~~
self.autoScrollLabel.frame = CGRectMake(CGRectGetMaxX(lab.frame)+5, CGRectGetMinY(lab.frame), SCREENW-CGRectGetMaxX(lab.frame)-15, 20);
[cell.contentView addSubview:self.autoScrollLabel];
~~~

~~~
- (QZAutoScrollLabel *)autoScrollLabel{
    if (!_autoScrollLabel) {
        _autoScrollLabel = [[QZAutoScrollLabel alloc]init];
        _autoScrollLabel.textColor = UIColorFromRGB(0x41210f);
        _autoScrollLabel.font = [UIFont systemFontOfSize:14];
        _autoScrollLabel.text = @"有事您说话！";
        [_autoScrollLabel observeApplicationNotifications];
    }
    return _autoScrollLabel;
}
~~~
