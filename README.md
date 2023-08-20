# **IOS App Random Background Generator**
 


## Set up
* Go to `Main` file and on the top right click the **+** to access the library of UI elements accessible to you.
* Add three Labels and one Button anywhere on the screen
* In the labels write **your name**, your **university name**, and **either your current job** or **aspirational job**.



## To Modifying Button 
* Select the button on `Main` and go to the `Attributes Inspector (three horizontal lines)` on the right hand side.
* Change Background Configuration from _Default_ to **Custom** and then change the fill to any color you would like.
* Optionally, change the _Foreground color_ as well.
* Lastly, change the name to something else. Remember, this button will change our background color to a random color.



## Connect UI to logic 
1. Open the `Storyboard` file
1. Click on the `Adjust Editor Options` button on the top right of Xcode
1. Click on the `Assistant` in the drop down
1. `Control` **+** Drag from the button on storyboard to somewhere inside of the `ViewController` class
1. Name your IBAction `changeBackgroundColor`
1. Change the type form `Any` to `UIButton`
1. Open the `ViewController.swift` file and under the `IBAction` you just created, write the following code:
    ```swift
    func changeColor() -> UIColor{

            let red = CGFloat.random(in: 0...1)
            let green = CGFloat.random(in: 0...1)
            let blue = CGFloat.random(in: 0...1)

            return UIColor(red: red, green: green, blue: blue, alpha: 0.5)
        }
    ```

    > **If we run our app now, nothing will happen. We need to call this function when the button is tapped.**
1. Go back to the changeBackgroundColor IBAction and add the following two lines:
    ```swift
        let randomColor = changeColor()
        view.backgroundColor = randomColor
    ```


## Conclusion
* User can run application showing a screen with a button and three labels
* Lable includes: **your name**, your **university name**, and **either your current job** or **_aspirational job**
* The screen has a background color that can changes when the button is tapped




# App Brainstorming
Make a list of your favorite 3-5 applications and identify 2-3 features that make them your favorite app. Its okay if features repeat on different apps
Example App: Instagram
Changing the background color of the messages screen
Deleting old messages

**Applications:** `Instagram`, `YouTube` and `TikTok`
- `Instragram`
    - Feature: New like feature that shows an animation 
* `YouTube`
    * Feature: Double tap to fast forward and rewind the video timestamp
- `TikTok`
    - Feature: The line at the bottom of the screen that displays time status of the video
