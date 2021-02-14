# Photo Color Discriminator

An app for analysing corona virus test tubes.
The app checks for hues of the test tubes and creates a report based on these values.
Test report then converted into an excel file and can be emailed to the given email address.

A demo for the application can be watched below

[![A demo video for the app](http://i3.ytimg.com/vi/BcswwtCdFYo/hqdefault.jpg)](https://youtu.be/BcswwtCdFYoE)

# Main Screen

![Main Menu Screen](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/main-menu.jpg)

User can navigate through app in this screen. 

Buttons :
- [Start Test](https://github.com/Rentran/Photo-Color-Discriminator/blob/main/README.md#testings)
- [Enter Patient Values](https://github.com/Rentran/Photo-Color-Discriminator/blob/main/README.md#patient-values) 
- [Settings](https://github.com/Rentran/Photo-Color-Discriminator/blob/main/README.md#settings) 
- Lock : Locks the app so user can not get out of the app or see notifications. Also unlocks the app if locked. 

# Settings

![Settings](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/adjust-grids.jpg)

This page is used to change settings in the app.

Available options :
- Show Columns : To show which columns should be showed when preparing test reports. Columns can be edited in Patient Values Page.
- Column Names : To change name of columns. For example, a column can be changed from "Names" to "Patient Number".
- Qr Split Char : To change which char will be used to split read qr for columns. For example if "." is given as split char, a qr data like "1.mehmet.demir" will be split into columns 1,2 and 3 as "1", "mehmet" and "demir" respectively when entering patient values.
- Receiver's Email : To change email address that will receive test report when "Send Email" button is pressed in test report screen.
- Hospitial Name : To change name of the hospital given in the excel 

# Patient Values

![Settings](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/patient-values.jpg)

This page is used to enter values for test tubes like name, surname, id, etc. values are corresponding to the columns in the settings.

User can enter these values either manualy or by reading a qr by pressing "Read From QR" button in the corresponding tube. 

This values then showed in the report and excel file. 

# Barcode Reader

![Read Qr](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/read-qr.jpg)

Reads data from barcode and writes it to chosen tubes patient value.

# Testings 

# Take A Picture Of Samples

![Take A Picture](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/take-picture.jpg)

Takes a picure of the sample

# Preview A Picture Of Samples

![Preview Picture](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/preview-photo.jpg)

Shows a preview of the image taken by the user.

# Show Grids

![Show Grids](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/show-grids.jpg)

Shows grids to be analysed by the app. App will check and analyse inside of grids for test tubes.  

# Adjust Grids

![Adjust Grids](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/adjust-grids.jpg)

Gives the user ability to adjust grids to fit the image. User can increase and decrease grid size from top, right, left and bottom.

# Test Report

![Test Report](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/test-report.jpg)

Shows Test Report prepared by analysing the image. A1 and B1 are positive and negative references respectively.

Negative reference means negative result closest to yellow (positive) color. (Negative result with the biggest valid hue).

Positive reference means positive result closest to red (negative) color. (Positive result with the smallest valid hue).

In the report, hues lower or greater than positive and negative references
are considered valid while hues between them or represent another color (like green or blue) are considered invalid. 

Hues lower than negative reference and valid can be taken as negative test results while Hues bigger than positive reference and valid can be considered positive.

This way, user can tell which test results are positive or negative.

Pressings and selecting a tube from the list shows taken, unprocessed (left) and processed (right) versions of the image of the tube above the references.

Buttons
- Repeat Test : User is taken to take a photo screen and test report id doesnt change.
- Finish Test : User is taken to main menu and test report id is changed.
- Send Email : The report in excel format is emailed to the given email address (Address is given in the settings).

An example of the email can be viewed below

![Excel](https://raw.githubusercontent.com/Rentran/Photo-Color-Discriminator/main/pictures/excel.jpg)
