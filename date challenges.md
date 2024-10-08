Java date challenges often involve dealing with input formats, parsing, validation, and formatting. Here are some common challenges with examples of input and expected output:

1. Parsing Date Strings

Challenge: Parse a date string in a given format.

Input:

String dateString = "2024-10-08";
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");

Expected Output:
A LocalDate object representing the date.

LocalDate date = LocalDate.parse(dateString, formatter);  // Output: 2024-10-08

2. Formatting Date into a String

Challenge: Format a date object into a specific string format.

Input:

LocalDate date = LocalDate.of(2024, 10, 8);
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd/MM/yyyy");

Expected Output:

String formattedDate = date.format(formatter);  // Output: "08/10/2024"

3. Handling Time Zones

Challenge: Convert a date-time from one time zone to another.

Input:

ZonedDateTime dateTime = ZonedDateTime.of(2024, 10, 8, 14, 0, 0, 0, ZoneId.of("America/New_York"));

Expected Output: Convert to Tokyo time.

ZonedDateTime tokyoTime = dateTime.withZoneSameInstant(ZoneId.of("Asia/Tokyo"));  
// Output: 2024-10-09T03:00+09:00[Asia/Tokyo]

4. Comparing Dates

Challenge: Compare two dates to determine which is earlier or later.

Input:

LocalDate date1 = LocalDate.of(2024, 10, 8);
LocalDate date2 = LocalDate.of(2023, 12, 25);

Expected Output:

boolean isAfter = date1.isAfter(date2);  // Output: true
boolean isBefore = date2.isBefore(date1);  // Output: true

5. Calculating Date Differences

Challenge: Find the difference between two dates in days, months, or years.

Input:

LocalDate startDate = LocalDate.of(2023, 12, 25);
LocalDate endDate = LocalDate.of(2024, 10, 8);

Expected Output:

Period period = Period.between(startDate, endDate);
int days = period.getDays();  // Output: 13
int months = period.getMonths();  // Output: 9
int years = period.getYears();  // Output: 0

6. Handling Invalid Date Input

Challenge: Validate the input date and handle exceptions gracefully.

Input:

String invalidDateString = "2024-13-08";
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");

Expected Output:

try {
    LocalDate date = LocalDate.parse(invalidDateString, formatter);
} catch (DateTimeParseException e) {
    System.out.println("Invalid date format");  // Output: Invalid date format
}

7. Adding/Subtracting Time from Date

Challenge: Add or subtract days, months, or years from a date.

Input:

LocalDate date = LocalDate.of(2024, 10, 8);

Expected Output:
Add 5 days and subtract 2 months.

LocalDate newDate = date.plusDays(5).minusMonths(2);  
// Output: 2024-08-13

8. Finding Day of the Week

Challenge: Find the day of the week for a given date.

Input:

LocalDate date = LocalDate.of(2024, 10, 8);

Expected Output:

DayOfWeek dayOfWeek = date.getDayOfWeek();  // Output: TUESDAY

These challenges cover common use cases of date handling in Java. Depending on the library used (java.time, java.util.Date, etc.), the specific methods may differ, but the concepts remain largely the same.

