-----Date-----

In javascript we have a object Date, it stores the information like the date and time, we can use this object by creating the instance of this, with the help of new
```
let myDate = new Date();
console.log(myDate); //Tue Mar 18 2025 15:14:26 GMT+0530 (India Standard Time)
```

. to give the specific date we can do this
```
//new Date(YYYY,MM,DD)
let specificDate = new Date(2000,06,23); // Sun Jul 23 2000 00:00:00 GMT+0530 (India Standard Time)
//here the july will be there at the 06 and january will be at the 00
```

. to formate these dates we can use the different string methods like this
```
let d = new Date();
console.log(d.toDateString()); //Wed Mar 19 2025
//just liek this we have a lot date method with which we can formate the date
```


. Date with the time (YYYYY, MM, DD, H, M, S)
```
let my = new Date(2025,02,19,11,10,5)
console.log(my) //Wed Mar 19 2025 11:10:05 GMT+0530 (India Standard Time)
co
```


. Getting the date component
```
let today = new Date();

console.log(today.getFullYear());   // 📅 Year (e.g., 2025)
console.log(today.getMonth());      // 🔢 Month (0 = Jan, 1 = Feb, ..., 11 = Dec)
console.log(today.getDate());       // 📆 Day of the month (1-31)
console.log(today.getDay());        // 🗓️ Day of the week (0 = Sunday, 1 = Monday, ..., 6 = Saturday)
console.log(today.getHours());      // ⏰ Hours (0-23)
console.log(today.getMinutes());    // ⏱️ Minutes (0-59)
console.log(today.getSeconds());    // ⏳ Seconds (0-59)
console.log(today.getMilliseconds());// ⏳ Milliseconds (0-999)
console.log(today.getTime());       // ⌚ Timestamp (milliseconds since Jan 1, 1970)
```


.Setting the Date
```
let date = new Date();
date.setFullYear(2030);     // Change year to 2030
date.setMonth(5);           // Change month to June (0-based index)
date.setDate(20);           // Change day to 20th
date.setHours(12);          // Change time to 12:00 PM
console.log(date);
  
```

. Formatign the String
```
let today = new Date();

console.log(today.toDateString());  // Example: "Mon Mar 17 2025"
console.log(today.toISOString());   // Example: "2025-03-17T10:30:15.000Z" (ISO Format)
console.log(today.toUTCString());   // Example: "Mon, 17 Mar 2025 10:30:15 GMT"
console.log(today.toLocaleString()); // Example: "3/17/2025, 10:30:15 AM" (Local format)
console.log(today.toLocaleDateString()); // Example: "3/17/2025"
console.log(today.toLocaleTimeString()); // Example: "10:30:15 AM"

```


.Date Calculations
```
      let oneDay = new Date("2025-01-20");
      let anotherDay = new Date("2025-06-22");
      let difference =  anotherDay - oneDay; //gives the milliseconds
      console.log(difference / (1000 * 60 * 60 * 24));
```

. Add date to the given date
```
let mydate = new Date();
mydate.setDate(mydate.getDate() + 7); //adds the seven days from the current time
console.log(mydate) //Wed Mar 26 2025 11:56:38 GMT+0530 (India Standard Time)
```

. Remove the days to the fiven date
```
let myDate = new Date();
myDate.setDate(myDate.getDate() - 7);
console.log(myDate); //Wed Mar 12 2025 11:59:37 GMT+0530 (India Standard Time)

```

. Comparing the Dates
```
let one = new Date("2025-01-20");
let two = new Date("2025-02-20");
console.log(two>one); //true

```


.Get current timestamps (from the 1970)
```
let mytime = Date.now();
console.log(mytime);  //it gives the tmestaps from the 1970 till now in miliseconds i.e. 1742366400665

//converting this timestamps to the date
let myDate = new Date(mytime);
console.log(myDate); //Wed Mar 19 2025 12:12:31 GMT+0530 (India Standard Time)

```



. UTC(Universal Time Coordinated ) it is the standard time common to every place in the world, and there is the IST, stamds for the indian standard time
we have this function called getTimezoneOffset(), used to give the difference between the utc and the ist
```
let now = new Date();
console.log(now.getTimezoneOffset()); // Example: -330 (for IST - Indian Standard Time)
```

Why -330?
IST (Indian Standard Time) is UTC+5:30 (5 hours 30 minutes ahead of UTC).
getTimezoneOffset() returns the difference from UTC in minutes.
Since IST is ahead of UTC, it gives -330 minutes (5 hours 30 minutes).
Positive values mean the local time is behind UTC.
Negative values mean the local time is ahead of UTC.
