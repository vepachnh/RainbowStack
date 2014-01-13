RainbowStack
============

A UI component looks like Quiz Up result page

![ScreenShot](https://github.com/aceisScope/RainbowStack/raw/master/screenshot0.PNG) -->Expanded-->
![ScreenShot](https://github.com/aceisScope/RainbowStack/raw/master/screenshot1.png)


###Description

This project is humble trial to simulate the result page of Quiz Up. 

###How to Use

1.   `#define BAR_HEIGHT 20` defines the actual height of rainbow bars at bottom.

2.  Assign the number of stacks(views) in total. An assert will be thrown if this number is larger than 4. Because in the original 
Quiz Up app it is 4. But this doesn't mean its capability is limited to 4.

``` objective-c
    - (NSInteger)numberOfStacks; 
```
3.
Assign each view for stack index. 
``` objective-c
   - (UIView*)rainbowStacks:(RainbowStacks*)rainbowStacks viewForStack:(NSInteger)stack;
```
This idea is similar to the `UITableView cellForRowAtIndex`.
For example: 

``` objective-c
    self.view1 = [[UIView alloc] initWithFrame:CGRectMake(0, 0, self.view.frame.size.width, self.view.frame.size.height * 1.2)];
    self.view1.backgroundColor = [UIColor colorWithRed:51./255 green:51./255 blue:51./255 alpha:1];
    self.view1.layer.shadowColor = shadowColor;
    self.view1.layer.shadowOffset = shadowOffset;
    self.view1.layer.shadowOpacity = YES;
``` 

##TODO(maybe)
I'm not sure if recycle is necessary, because it is quite unrealistic to put many views into this stack...
