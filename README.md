# iOS QR Code Generator
A simple Objective-C library which simplify QR Code generation starting from a string.

# Usage
``` objc
#import "QRCodeGenerator.h"

// generate a QR Code with `Hello World` string and default settings: black QR Code, white background, and 200x200 size
imageView.image = [[QRCodeGenerator alloc] initWithString:@"Hello World"] getImage];
```

# Customization
``` objc
#import "QRCodeGenerator.h"

// generate a QR Code with `Hello World` and custom size and aspect
QRCodeGenerator *qr = [[QRCodeGenerator alloc] initWithString:@"Hello World"];
qr.size = CGSizeMake(400.0f, 400.0f); // 400x400 size
qr.color = [CIColor colorWithRGBA:@"#FFFFFF"]; // white QR Code color
qr.backgroundColor = [CIColor colorWithRGBA:@"#000000"]; // black background color

imageView.image = [qr getImage];
```

# License
MIT
