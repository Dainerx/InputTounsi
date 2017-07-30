# Input Tounsi
A jQuery plugin for entering and validating Tunisian users' coordinates. It is made very easy to use and easier to customize .

<img src="https://raw.github.com/jackocnr/intl-tel-input/master/screenshot.png" width="424px" height="246px">

If you like it and would like to leave some feeds back please leave me a message on one of my social medias accounts or [personal website](http://dainer.me).

## Table of Contents

- [Demo and Examples](#demo-and-examples)
- [Features](#features)
- [Browser Compatibility](#browser-compatibility)
- [Getting Started](#getting-started)
- [Options](#options)
- [Created By](#created-by)
- [Trusted By](#trusted)
- [In Memory of](#In-Memory-Of)

## Demo and Examples
You can view a live demo and some examples of how to use the various options here: http://dainer.me/Inputtounsi, or try it for yourself using the included demo.html.


## Features
* Automatically validate input elements values of Tunisian user coordinates based on Tunisian criteria.
* Automatically validate the whole form before sending request to the backend.
* Automatically display a message of error if the value entered does not match the Tunisian criteria.
* Automatically display place holders for elements. 
* Ability to override all default options in a very simple way.

## Browser Compatibility
| Chrome | FF  | Safari | IE  | Chrome Android | Mobile Safari | IE Mob |
| :----: | :-: | :----: | :-: | :------------: | :-----------: | :----: |
|    ✓   |  ✓  |    ✓   |  9  |      ✓         |       ✓       |     ✓  |



## Getting Started

1. Include the script along with Jquery
  ```html
  <script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.1/jquery.min.js"></script>
  <script src="//dainer.me/InputTounsi.js"></script>  
  ```

2. Add the plugin script and initialise it on your input element
  ```html
  <input type="text" id="cin">
  <script>
    $("#cin").intlTelInput('cin');
  </script>
  ```
3. InputTounsi supports seven kinds of input, you can only use the supported ones. 

  ```html
    <script>
    $("#name").verifyInputTounsi("name");
    $("#lastname").verifyInputTounsi("lastname");
    $("#phone").verifyInputTounsi("phone");
    $("#email").verifyInputTounsi("email");
    $("#state").verifyInputTounsi("state",$("#city"));
    $("#city").verifyInputTounsi("city");
    $("#address").verifyInputTounsi("address");
    </script>
  ```

Note: In order for state and city elements to work, you have to pass as argument your city element to verifyInputTounsi() triggered by your city element.

## Options
One of the greatest feature InputTounsi offers is overriding basically everything.

**Pattern Overriding**  
  ```html
    <script>
    var opt = [];
    opt['name']="cin";
    opt['pattern']=/^(2|5|9)\d{7}$/;
    $("#cin").verifyInputTounsi(opt);
    </script>
  ```

**Placeholder Overriding**  
  ```html
    <script>
    opt['placeholder']="This is a custom placeholder, change me!";
    $("#cin").verifyInputTounsi(opt);
    </script>
  ```

**Style Overriding**  

  ```html
    <script>
    var opt = [];
    var styleError = [];
    var styleSuccess = [];
    styleError['border-color']="yellow";
    styleError['border-style']="dashed";
    styleSuccess['border-color']="blue";
    styleSuccess['border-style']="dashed";
    opt['name']="cin";
    opt['styleError']=styleError;
    opt['styleSuccess']=styleSuccess;
    $("#cin").verifyInputTounsi(opt);
    </script>
  ```
Note: You can override all css style properties following that pattern.

**Error message Overriding**  

  ```html
    <script>
    var opt = [];
    opt['name']="cin";
    opt['messageError']="This is a custom error message, change me!";
    $("#cin").verifyInputTounsi(opt);
    </script>
  ```

**Error message style Overriding**  

  ```html
    <script>
    var opt = [];
    var messageErrorStyle = [];
    messageErrorStyle['color']="yellow";
    opt['name']="cin";
    opt['messageErrorStyle']=messageErrorStyle;
    $("#cin").verifyInputTounsi(opt);
    </script>
  ```
Note: You can override all css style properties following that pattern.




## Created-By
-[Oussama Ben Ghorbel](http://dainer.me/)

## Trusted-By
* [Innovative Partner](https://github.com/behdad/region-flags)


## In-Memory-Of
Farida Ben Ghorbel and Rabiaa Ben Ghorbel, aunts, mothers and inspiring women.
