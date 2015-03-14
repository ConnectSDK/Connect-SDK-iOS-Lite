#Connect SDK iOS, Lite Version
Connect SDK is an open source framework that connects your mobile apps with multiple TV platforms. Because most TV platforms support a variety of protocols, Connect SDK integrates and abstracts the discovery and connectivity between all supported protocols.

This repository contains the lite version of the Connect SDK project, and does not include support for platforms that require heavy and/or external dependencies. For the full Connect SDK, clone the [main repository](https://github.com/ConnectSDK/Connect-SDK-iOS).

For more information, visit our [website](http://www.connectsdk.com/).

* [General information about Connect SDK](http://www.connectsdk.com/discover/)
* [Platform documentation & FAQs](http://www.connectsdk.com/docs/ios/)
* [API documentation](http://www.connectsdk.com/apis/ios/)

##Dependencies
This project has the following dependencies.

* libicucore.dylib
* libz.dylib
* Other linker flags: -ObjC
* Automatic Reference Counting (ARC)
* [Connect-SDK-iOS-Core](https://github.com/ConnectSDK/Connect-SDK-iOS-Core) submodule

##Including Connect SDK in your app
###Using CocoaPods
1. Add `pod "ConnectSDK/Core"` to your `Podfile`
2. Run `pod install`
3. Open the workspace file and run your project

You can use `pod "ConnectSDK"` to get the [full version](https://github.com/ConnectSDK/Connect-SDK-iOS).

###Without CocoaPods

1. Clone repository (or download & unzip)
2. Set up the submodules by running the following commands in Terminal
   - `git submodule init`
   - `git submodule update`
3. Open your project in Xcode
4. Locate the Connect SDK Xcode project in the Finder
5. Drag the Connect SDK Xcode project into your project's Xcode library
6. Navigate to your project's settings screen, then navigate to the Build Phases tab
7. Add ConnectSDK as a Target Dependency
8. Add the following in the `Link Binary With Libraries` section
   - libConnectSDK.a
   - libz.dylib
   - libicucore.dylib

###Include Strings File for Localization (optional)
1. Locate the Connect SDK Xcode project in the Finder
2. Drag the ConnectSDKStrings folder into your project's library
3. You may make whatever changes you would like to the values and the SDK will use your strings file

##Contact
* Twitter: [@ConnectSDK](https://www.twitter.com/ConnectSDK)
* Ask a question with the "tv" tag on [Stack Overflow](http://stackoverflow.com/tags/tv)
* Developer Support: support@connectsdk.com
* Partnerships: partners@connectsdk.com

##Credits
Connect SDK for iOS makes use of the following projects, some of which are open-source.

* [SocketRocket](https://github.com/Square/SocketRocket) (Apache License, Version 2.0)
  - modifications:
    - stability
    - self-signed certificate support
    - avoid potential namespace collisions
* [objc-guid](https://code.google.com/p/objc-guid/) (BSD 3-Clause revised)
* [GCDWebServer](https://github.com/swisspol/GCDWebServer) (MIT)
* [XMLReader](https://github.com/amarcadet/XMLReader) (MIT)
  - modifications:
    - properly return an error if XML parsing has failed
* [ASIHTTPRequest](https://github.com/pokeb/asi-http-request) (MIT)

##License
Copyright (c) 2013-2014 LG Electronics.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

> http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
