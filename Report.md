   At the beginning of the planning process we divided the work into two. One part was to get the barcode scanner working and the other part was to get the FDA API working. To get the barcode scanner on the app, expo barcode-scanner was installed and then implemented in App.tsx. For the barcode scanner, it asks the user permission to use the camera the first time they use the app, if the user lets them then the barcode scanner is accessible to them. Then there is a BarCodeScanner that saves the value of the barcode so it can be used when we need it. 

  With the barcode scanner and FDA API figured out we moved onto another step and it was setting up the appearance of the app and the backend aspect. To get the app working the way we wanted, we needed to have multiple screens, buttons and input boxes. Each screen had its own function and when the screen was needed in the main code of the app that was being exported there were lines of code that called on these screens. To navigate between screens created we used navigation.navigate. In the main code, the screens were given their name and we used navigation.navigate(‘name of screen’) to move to those screens. The buttons and input boxes were created using the component from react-native that were installed. Using react-native allowed us to use the text, buttons, alert, touchable opacity and view. By following the format given by react native it allowed us to understand how everything worked and connect the backend and user input. The buttons helped move and send the information to the database.tsx and fdaapi.tsx created. The input boxes were there to get input from the user and that information was sent to the database. The input boxes work every time the value in them changes. The input boxes have a function called onChangeText, so when the value in them is changed a function is called and changes the value. 

  The first screen on the app is the login screen. On this screen there is an input box that lets the user put the username they want and there is a login button for them to access the next screen. The second screen created was the home screen. This screen has two buttons that the user can press, one is to create a new recipe and one is to view an existing recipe. The button for creating a new recipe takes the user to a screen named ‘Camera’ . On this screen there is an input box for the user to name the recipe they are creating and there is a button titled ‘add ingredient’. When the button is pressed it will start the barcode scanner and let them scan the items they want. There are two buttons and an input box on this screen. On top of the screen there is an ‘upload recipe’ button and below it is the scanner. Below the scanner there is an input box for the user to put the number of servings they want, once the value of the serving size changes there is a text that is outputted on the bottom of the screen that tells the user the amount of calories. To add the ingredient and the number of servings to the recipe, the user must press the ‘go’ button. Once the first item is scanned, a button titled ‘Scan again?’ appears and the user can scan more items and add them to the recipe by pressing ‘go’. Once they have added everything they want they can press the ‘Upload Recipe’ button and this sends the information to the database. The user can go back to the home button and press the ‘Saved Recipes’ button and it will take them to the ‘Recipes Saved’ screen. On this screen the user puts the name of the recipe they are looking for in the input box, and then they should press the ‘find recipe’ button, this will find the recipe in the database and then they should press ‘load recipe’, this will load the information of the recipe and print out the number of calories, the name of the recipe, and the list of ingredients. This works because the buttons and input boxes use functions created in database.tsx and fdaapi.tsx. 