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
	
	
	 Calendar cal = Calendar.getInstance();
etdate.setOnClickListener(view -> {
                            /*DatePickerDialog
                                    .newInstance(null, cal.get(Calendar.YEAR), cal.get(Calendar.MONTH), cal.get(Calendar.DATE))
                                    .show(getFragmentManager(), null);*/
                            DatePickerDialog dpd = new DatePickerDialog(MainActivity.this, (view1, year, month, dayOfMonth) -> {
                                Toast.makeText(MainActivity.this, String.format("%d", year) + "-" + String.format("%02d", month + 1) + "-" + String.format("%02d", dayOfMonth), Toast.LENGTH_SHORT).show();
                            }, cal.get(Calendar.YEAR), cal.get(Calendar.MONTH), cal.get(Calendar.DATE));
                            dpd.show();
                        }
                );
		
		 etTime
                .setOnClickListener(view -> {
                        /*TimePickerDialog
                        .newInstance(null, cal.get(Calendar.HOUR_OF_DAY), cal.get(Calendar.MINUTE), true)
                        .show(getFragmentManager(), null);*/
                            TimePickerDialog tpd = new TimePickerDialog(MainActivity.this, (view1, hourOfDay, minute) -> {
                                Toast.makeText(MainActivity.this, String.format("%02d", hourOfDay) + ":" + String.format("%02d", minute), Toast.LENGTH_SHORT).show();
                            }, cal.get(Calendar.HOUR_OF_DAY), cal.get(Calendar.MINUTE), DateFormat.is24HourFormat(MainActivity.this));
                            tpd.show();
                        }
                );

## Some pictures

API 15 | API 26
-|-
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_date.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_date.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_date_land.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_date_land.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_time_12h.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_time_12h.png)
![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api15_time_12h_land.png) | ![DatePicker](https://raw.githubusercontent.com/Gericop/DateTimePicker/master/images/api26_time_12h_land.png)

> You can see that in landscape the API 15 images show spinners instead of a calendar view. This is because there is not enough room for the calendar, so the spinners are used as fallback.
