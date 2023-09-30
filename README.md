# Flutter Issues
Hard earned issues that we can document and reuse every time we need it!

## CocoaPods not installed or not in valid state
I run first 
```bat
sudo gem install cocoapods
```
or 
```bat
$ gem install cocoapods --user-install
$ gem which cocoapods
/Users/eloy/.gem/ruby/2.0.0/gems/cocoapods-0.29.0/lib/cocoapods.rb
$ /Users/eloy/.gem/ruby/2.0.0/bin/pod install
```
but don't work, because command tools of Xcode was not installed.
 you should run 
```bat
xcode-select --install
```
to install command tools of Xcode and then use brew or rvm , ... to install cocoapods.

commands for installing brew:
```bat
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

(echo; echo 'eval "$(/usr/local/bin/brew shellenv)"') >> /Users/edvard/.zprofile
```
finally you can install cocoapods :
```bat
brew install cocoapods

pod install
```

## Android dependency not resolved due to server TLS version
There is a build error which is caused by TLS version that is used in Gradle

In gradle.properties add this to the end of the file
```bat
https.protocols=TLSv1.0
```
