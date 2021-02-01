# 1Xib-1ViewController

XibとviewControllerが1対1となるプロジェクトを作成する。

  - SceneDelegateを削除する
  - storyboardの削除
  - ViewControllerの削除
  - Appdelegateの修正

### SceneDelegateの削除
  - SceneDelegateを削除する
  - AppdelegateにあるUISceneSession Lifecycle以下のメソッド(configurationForConnecting,didDiscardSceneSessions)を削除する
  - Info.plistのUIApplicationSceneManifestのkeyすべてを削除
  
### Storyboardの削除
  - MainStoryboardを削除する
  - info.plist の Main storyboard file base nameを削除 

 ### ViewControllerの削除
  - FirstViewControllerとFirstViewController.xibの作成
  - info.plist の Main storyboard file base nameを削除 
  - xbiのfile's OwerをFirstViewCOntrollerに変更
  -file'sOwnerからcontrolでviewにドラックしてoutletの接続をする

 ### Appdelegateの修正
  -applicationメソッドに下記コードを追加する

```sh
        window = UIWindow(frame: UIScreen.main.bounds)
        window?.rootViewController = FirstViewController()
        window?.makeKeyAndVisible()
```


