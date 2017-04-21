# :clock10: Ternary clock with colorful read-out (web-version)

## What

At school, kids learn to count from 1 to 10 (probably because the number of fingers on your hands ;-). As such, in daily life, the decimal system is the most popular, and most intuitive to use. Computer scientists tend to prefer [binary](https://en.wikipedia.org/wiki/Binary_number) (0-1) or [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) (x0-xF) systems. All of them are just a way of counting quantity. 

In a [ternary or base-3 systems](https://en.wikipedia.org/wiki/Ternary_numeral_system), only 0,1 and 2 are used. Being way less common, reading figures like 12201211 might make your brain-processor to get hot. The clock in this repository shows time by colored squares which represent the tri possible states in a ternary numeral system. 

`21:32:50`|`21:24:43`
----------|----------
![Clock example](images/213250.png) | ![Clock example](images/212443.png)

## Why

Some might find the idea a little crazy, others will say its fun. I think it is an excellent tool to train the brain... and I am probably a little crazy :laughing:

Anyhow, it was a good exercise to write some javascript, it's a challenge every time you want to know the time, and it was great fun after all. 

## How

The logic has been written in javascript, and all of it has been integrated in a minimalistic webpage in order to have a universal interface. In its current configuration the result even renders nicely on a smartphone (oriented in landscape).

## Technical details

### Maths

...comming soon.............

### Sourcecode

```javascript
      function convertToTernaryColors(decimal) { 
        var ternaryColors = ["whitesmoke", "whitesmoke", "whitesmoke", "whitesmoke"];
        var div;
        var rem;
        for (i = 0; i < 4; i++) {
            div = Math.floor(decimal/Math.pow(3, 3-i));
            rem = decimal % Math.pow(3, 3-i);
            switch(div) {
                case 1:
                    ternaryColors[i] = "yellowgreen";
                    break;
                case 2:
                    ternaryColors[i] = "orangered";
                    break;
              } 
            decimal = rem;  
          }
        return ternaryColors
      }
```

## Contributors

If you are having any good suggestions, just drop me a line [:email:](http://nostradomus.ddns.net/contactform.html). 
If feasible, I'll be happy to implement proposed improvements. 
And if you are having lots of time, I'll be happy to share the work with you ;-).

## :globe_with_meridians: License

There is no specific license attached to this script. 
If you like it, have fun with it (at your own risk of course :-D).
Oh, and when using anything from this repository, it is highly appreciated if you mention its origin.
