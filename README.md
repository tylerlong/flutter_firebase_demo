# flutter_firebase_demo

A Flutter Firebase demo project.


## Ref

- https://firebase.google.com/docs/cli#install-cli-mac-linux
- https://firebase.google.com/docs/flutter/setup?platform=web


## Create the project

```
flutter create flutter_firebase_demo
```


## Run the project

```
flutter run -d chrome
```


## Install firebase CLI

```
curl -sL https://firebase.tools | bash
```

You will need to enter admin password of your machine.

Update to new version:

```
curl -sL https://firebase.tools | upgrade=true bash
```


## Login firebase

```
firebase login
```

You will need to login your Google account in browser


## List all firebase projects

```
firebase projects:list
```


## Install flutterfire cli

```
dart pub global activate flutterfire_cli
```

Edit `~/.zshrc` and append the following line:

```
export PATH="$PATH":"$HOME/.pub-cache/bin"
```

Now you should be able to run the command `flutterfire` in a new terminal.


## Configure your project for firebase

```
flutterfire configure
```

Enter a project name. Please note that, firebase project name must only contain [0-9a-z-]. (while flutter project name must only contain [0-9-a-z_]).

And most popular names have been taken, such as "flutter-demo". 我取名为 "flutter-demo-2023".

结果由于权限问题失败了。索性直接通过图形界面创建project。创建成功。

再一次执行 `flutterfire configure`, platforms 默认四个都是选中的: android, ios, macos, web。
然后它做的事情是帮我在 firebase console 创建了 apps。并且本地生成了一些文件包含了 app key, app id 之类的。

`flutterfire configure` 这个命令可以多次执行。尤其是新增platform支持的时候必须要执行。
