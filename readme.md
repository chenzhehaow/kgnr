Checkout to: `~/Library/Developer/Xcode/UserData/CodeSnippets/`

## clang warning push/pop

``` obj-c
#pragma clang diagnostic push
#pragma clang diagnostic ignored "<#-W warning#>"
<#code#>
#pragma clang diagnostic pop
```

## dispatch_once

``` obj-c
static id <#object#>;
static dispatch_once_t once;
dispatch_once(&once, ^{
    <#object#> = <#value#>;
});
```

## init

``` obj-c
- (id)init{
    if(!(self = [super init])){
        return nil;
    }

    <#code#>

    return self;
}
```

## Log Class:MethodName

``` obj-c
NSLog(@"%@:%@", NSStringFromClass([self class]), NSStringFromSelector(_cmd));
```

## Log Method Name

``` obj-c
NSLog(@"%@", NSStringFromSelector(_cmd));
```

## Pragma section

``` obj-c
#pragma mark - <#section#>
```

## Requires ARC

``` obj-c
#if !__has_feature(objc_arc)
#error <#library#> must be built with ARC.
// You can turn on ARC for only <#library#> files by adding -fobjc-arc to the build phase for each of its files.
#endif
```

*Generated by readme.py: `python readme.py`*
