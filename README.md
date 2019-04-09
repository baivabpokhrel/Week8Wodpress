# Project 7 - WordPress Pentesting

Time spent: **7** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report
1. (Required)WordPress => 4.2 - User Authentication
- [x] Summary:
- Vulnerability types: user authentication,
-Tested in version: 4.2
- Fixed in version: 4.2.1
- [x] GIF Walkthrough: 

<img src='https://github.com/baivabpokhrel/Week8Wordpress/blob/master/Gifs/SignIn.gif' title='imageGif' alt='imageGif' />


- [x]Steps to recreate:
Enter "admin" as username and type random password.
Enter "different name" as username and type "admin" as password.

2. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
- [x] Summary: This vulnerability allows remote attackers to create a specially crafted image file name that will inject arbitrary web script.  This abuses the insufficient validation of the file names of uploaded images.
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.6.1
- [x] GIF Walkthrough:

<img src='https://github.com/baivabpokhrel/Week8Wordpress/blob/master/Gifs/Image.gif' title='imageGif' alt='imageGif' />

- [x] Steps to recreate: Create a new media post and upload an image with the following filename format:

```
filename<img src=a onerror=alert(1)>.png
```
3. (Required) WordPress <= 4.3 - Authenticated Shortcode Tags Cross-Site Scripting (XSS)
- [x] Summary: A stored/persistent, Cross-Site script XSS vulnerablilty which allows remote attackers to inject arbitrary web script/HTML by abusing the way unclosed HTML elements
during the processing of shortcode tags are mishandled.
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.3
- [x] GIF Walkthrough:

<img src='https://github.com/baivabpokhrel/Week8Wordpress/blob/master/Gifs/Alert.gif' title='gif 1' alt='gif 1' />

- [x] Steps to recreate: Create a new post and place the following code in the body:

```
<a href="" "onclick=alert(1)">check</a>
```

When a user clicks in the post, the injected code is executed.
# Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

Copyright [yyyy] [name of copyright owner]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
