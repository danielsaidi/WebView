<p align="center">
    <img src ="Resources/Logo_GitHub.png" alt="WebViewKit Logo" title="WebViewKit" width=600 />
</p>

<p align="center">
    <img src="https://img.shields.io/github/v/release/danielsaidi/WebViewKit?color=%2300550&sort=semver" alt="Version" />
    <img src="https://img.shields.io/badge/Swift-5.6-orange.svg" alt="Swift 5.6" title="Version" />
    <img src="https://img.shields.io/badge/platform-SwiftUI-blue.svg" alt="Swift UI" title="Swift UI" />
    <img src="https://img.shields.io/github/license/danielsaidi/WebViewKit" alt="MIT License" title="MIT License" />
        <a href="https://twitter.com/danielsaidi">
        <img src="https://img.shields.io/twitter/url?label=Twitter&style=social&url=https%3A%2F%2Ftwitter.com%2Fdanielsaidi" alt="Twitter: @danielsaidi" title="Twitter: @danielsaidi" />
    </a>
    <a href="https://mastodon.social/@danielsaidi">
        <img src="https://img.shields.io/mastodon/follow/000253346?label=mastodon&style=social" alt="Mastodon: @danielsaidi@mastodon.social" title="Mastodon: @danielsaidi@mastodon.social" />
    </a>
</p>


## About WebViewKit

WebViewKit adds a `WebView` to `SwiftUI`, that can be used to display web sites in your app. 

The result can look like this and can also be presented in sheets, full screen covers etc.:

<p align="center" style="border-radius: 80px; outline: 4px solid white; outline-offset: -4px">
    <img src ="Resources/Demo.gif" width="300" />
</p>

The ``WebView`` view can load any url and be fully configured to fit your needs. For more basic needs, you have a ``SafariWebView`` as well.

WebViewKit supports `iOS 13` and `macOS 11`.



## Installation

WebViewKit can be installed with the Swift Package Manager:

```
https://github.com/danielsaidi/WebViewKit.git
```

If you prefer to not have external dependencies, you can also just copy the source code into your app.



## Getting started

The [online documentation][Documentation] has a [getting started guide][Getting-Started] guide to help you get started with WebViewKit.

The library's main view is ``WebView``, which can display web pages and HTML content.

The easiest way to use this view is to just load a url into it:

```swift
import SwiftUI
import WebViewKit

struct MyView {

    var body: some View {
        WebView(urlString: "https://danielsaidi.com")
    }
}
```

The URL can point to any global URL, as above, but also to files in any bundle:

```swift
let localUrl = Bundle.main.url(forResource: "about", withExtension: "html")
let view = WebView(url: localUrl)
``` 

You can load a custom HTML string into the web view, provide custom configurations, etc.

The library also contains an iOS only ``SafariWebView``, which can load the same kind of content as the ``WebView``. It's basic compared to ``WebView``, but adds a topmost navigation bar and a bottommost toolbar with buttons for additional convenience.

For more information, please see the [online documentation][Documentation] and [getting started guide][Getting-Started].



## Documentation

The [online documentation][Documentation] contains more information, code examples, etc., and makes it easy to overview the various parts of the library.



## Demo Application

The demo app lets you explore the library on iOS and macOS. To try it out, just open and run the `Demo` project.



## Support this library

I manage my various open-source projects in my free time and am really thankful for any help I can get from the community. 

You can sponsor this project on [GitHub Sponsors][Sponsors] or get in touch for paid support.



## Contact

Feel free to reach out if you have questions or if you want to contribute in any way:

* Website: [danielsaidi.com][Website]
* Mastodon: [@danielsaidi@mastodon.social][Mastodon]
* Twitter: [@danielsaidi][Twitter]
* E-mail: [daniel.saidi@gmail.com][Email]



## License

WebViewKit is available under the MIT license. See the [LICENSE][License] file for more info.



[Email]: mailto:daniel.saidi@gmail.com
[Website]: https://www.danielsaidi.com
[Twitter]: https://www.twitter.com/danielsaidi
[Mastodon]: https://mastodon.social/@danielsaidi
[Sponsors]: https://github.com/sponsors/danielsaidi

[Documentation]: https://danielsaidi.github.io/WebViewKit/documentation/webviewkit/
[Getting-Started]: https://danielsaidi.github.io/WebViewKit/documentation/webviewkit/getting-started
[License]: https://github.com/danielsaidi/WebViewKit/blob/master/LICENSE
