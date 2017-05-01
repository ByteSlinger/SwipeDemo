# SwipeDemo
Apple IOS Xcode storyboard-ONLY demo of swipe gestures

I saw many examples and snippets on the web about using swipe gestures to navigate between View Controllers but most of them required coding in Swift or Objective-C.  I was pretty sure it could be done with just the Storyboard and after experimenting with it, I came up with this demo.

So, Xcode DOES provide the capability to navigate between multiple view controllers with swipe gestures, WITHOUT having to write any Swift or Objective-C code.  Here are the general steps:

1) Create your multiple View Controllers by dragging them from the object library onto your storyboard.  For demo purposes, you can have them all point to the same default ViewController class created by Xcode.
2) Drag the "Swipe Gesture Recognizer" from the object libary onto your View Controllers for each swipe that you want.  Make sure you pick a different Swipe direction for each one in the same View Controller.
3) CTRL-drag each "Swipe Gesture Recognizer" to the View Controller that you want to display. Select "Show Detail" for the "Action Segue" on each one.
4) Now here's the magic:  for each "Swipe Gesture Recognizer", CTRL-click on the icon in the top bar of the View Controller and a small dark popup window will appear.  Near the bottom of this popup window the last option is "Referencing Outlet Collections".  The small circle to the right of that text will become a plus sign when you hover over it.  CTRL-drag this plus sign to the View in the same View Controller.  A small one-line popup should come up:  "gestureRecognizers".  Click on the words "gestureRecognizers".  This should change the popup window to have "gestureRecognizers" and "View" in the "Referencing Outlet Collections" section.  Do this for every "Swipe Gesture Recognizer" on each of your View Controllers.

Now when you run your app, the Swipe gestures should start functioning as you expect.
