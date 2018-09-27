Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
	        implementation 'com.github.Aqil92:MaterialDatePicker:1.0'
	}

## Some pictures

API 15 | API 26
-|-
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_date.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_date.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_date_land.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_date_land.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_time_12h.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_time_12h.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_time_12h_land.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_time_12h_land.png)

> You can see that in landscape the API 15 images show spinners instead of a calendar view. This is because there is not enough room for the calendar, so the spinners are used as fallback.
