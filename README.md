# Compare-Different-Language
In this repository, I mention how to crate alert in diiferent language for mobile divice so that anyon can easyly understand which code is simple or complex


#Alert
##SwiftUI, iOS, Xcode
```swift
@State private var showingAlert = false
Button(action: {
            self.showingAlert = true
        }) {
            Text("Show Alert")
        }
        .alert(isPresented: $showingAlert) {
            Alert(title: Text("Important message"), message: Text("Wear sunscreen"), dismissButton: .default(Text("Got it!")))
        }
```
## UIKit, iOS, Xcode
```swift
let alert = UIAlertController(title: "Alert", message: "Message", preferredStyle: UIAlertControllerStyle.Alert)
alert.addAction(UIAlertAction(title: "Click", style: UIAlertActionStyle.Default, handler: nil))
self.presentViewController(alert, animated: true, completion: nil)
```

## Dart, Flutter
```
showAlertDialog(BuildContext context) {

  // set up the button
  Widget okButton = FlatButton(
    child: Text("OK"),
    onPressed: () { },
  );

  // set up the AlertDialog
  AlertDialog alert = AlertDialog(
    title: Text("My title"),
    content: Text("This is my message."),
    actions: [
      okButton,
    ],
  );

  // show the dialog
  showDialog(
    context: context,
    builder: (BuildContext context) {
      return alert;
    },
  );
}
```
## React Native
```javascript
Alert.alert(
  'Alert Title',
  'My Alert Msg',
  [
    {
      text: 'Ask me later',
      onPress: () => console.log('Ask me later pressed')
    },
    {
      text: 'Cancel',
      onPress: () => console.log('Cancel Pressed'),
      style: 'cancel',
    },
    {
      text: 'OK',
      onPress: () => console.log('OK Pressed')
    },
  ],
  {cancelable: false},
);
```
## Java, android,
```java
AlertDialog alertDialog = new AlertDialog.Builder(MainActivity.this).create();
alertDialog.setTitle("Alert");
alertDialog.setMessage("Alert message to be shown");
alertDialog.setButton(AlertDialog.BUTTON_NEUTRAL, "OK",
    new DialogInterface.OnClickListener() {
        public void onClick(DialogInterface dialog, int which) {
            dialog.dismiss();
        }
    });
alertDialog.show();
```
## Xamarin C#, Android
```csharp
private void CreateAddProjectDialog() {
    //some code
    var alert = new AlertDialog.Builder (this);
    alert.SetTitle ("Create new project");
    alert.SetView (layoutProperties);
    alert.SetCancelable (false);
    alert.SetPositiveButton("Create", HandlePositiveButtonClick);
    alert.SetNegativeButton("Cancel", HandelNegativeButtonClick);
}
```

## Ionic Framework
```
openFilters() {
    let alert = this.alertController.create({
        title: 'Example',
        subTitle: 'Example subtitle',
        buttons: ['OK']
    });

    alert.present();
}
```

* Flutter: Currently on iOS and Android – but the long-term vision for Flutter is to offer an integrated solution that allows developers to write one code for both desktop & mobile, and for the web.
* React Native: iOS and Android – but there are select libraries that allow you to use the same code to build iOS, Android, web, and Windows10 apps.


1. Different Blog sys that Flutter is best for future Cross platform apps development, React Native is god for basic but when we need advance feature we need to more effort, take too much time to fix the bug, net to change framework to run apps in different platform, yet it has vast community and big market place than flutter

2. Flutter certainly wins over here due to its simplicity. However, React Native is popular for delivering excellent user experience on both the platforms. Flutter has the extra advantage of reusing the code while React Native is less suitable due to its architecture.

* StackOverFlow Popularity of Programming language
http://sotagtrends.com/?tags=[ionic-framework,react-native,flutter,xamarin]&relative=false

* For more please visit : https://www.thedroidsonroids.com/blog/flutter-vs-react-native-what-to-choose-in-2020
