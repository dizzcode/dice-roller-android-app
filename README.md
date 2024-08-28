# Create an interactive Dice Roller app

## Note 1
You might wonder why you should bother to pass a Modifier argument at all when there's a default. The reason is because composables can undergo recomposition, which essentially means that the block of code in the @Composable method executes again. If a Modifier object is created in a block of code, it could potentially be recreated and that isn't efficient.


Chain a fillMaxSize() method onto the Modifier object so that the layout fills the entire screen.  
DiceWithButtonAndImage(modifier = Modifier  
.fillMaxSize()  
)  



Chain the wrapContentSize() method onto the Modifier object and then pass Alignment.Center as an argument to center the components. Alignment.Center specifies that a component centers both vertically and horizontally.
DiceWithButtonAndImage(modifier = Modifier  
.fillMaxSize()  
.wrapContentSize(Alignment.Center)  
)  


Pass a horizontalAlignment argument to the Column() function and then set it to a value of Alignment.CenterHorizontally.
This ensures that the children within the column are centered on the device screen with respect to the width.


add a Spacer composable between the Image and the Button composables. A Spacer takes a Modifier as a parameter.



Composables are stateless by default, which means that they don't hold a value and can be recomposed any time by the system, which results in the value being reset. However, Compose provides a convenient way to avoid this. Composable functions can store an object in memory using the remember composable.



created an interactive Dice Roller app for Android with Compose!

Summary
Define composable functions.
Create layouts with Compositions.
Create a button with the Button composable.
Import drawable resources.
Display an image with the Image composable.
Make an interactive UI with composables.
Use the remember composable to store objects in a Composition to memory.
Refresh the UI with the mutableStateOf()function to make an observable.
