# Dates, Timestamps, Timezones WTF?

**Session by Johannes Ewald @jhnns**

In this discussion about managing dates, timestamps, and timezones we covered some interesting edge cases of using time in software applications. Here's a simplified summary of what we discussed:

* Johannes suggested using ISO strings (e.g., new Date().toISOString()) as the recommended way to represent dates and timestamps. ISO strings provide a standardized format that is not dependent on the user's location. They remain consistent during daylight savings changes, and UTC remains unaffected.

* Avoid relying on UNIX time (number of seconds since January 1, 1970) as it lacks timezone information and can cause confusion across different timezones.

* Storing timestamps with timezone information allows flexibility, enabling the server to be moved to a different timezone without data issues. Note that PostgreSQL does not store timezone information by default, requiring alternative approaches.

* Store timezone identifiers per location rather than assuming future timezones will remain the same. Formats like "Europe/Berlin" ensure accurate representation, accounting for potential political changes.

* Separate date and timezone information when storing dates to ensure clarity and facilitate calculations and conversions.

* Browser's timezone != user's timezone != server timezone

* Many testing tools have limitations in changing timezones, impacting thorough testing of time-dependent functionality.

* The ISO standard also provides a separate format for representing durations 
  
* When passing timestamps as function arguments, prefer strings over date objects to avoid confusion caused by extra information in date objects.

* Consider using template types to enforce string usage for timestamps and prevent unintended date object usage.

* Developers working with Prisma should be aware that it only accepts date instances for specific operations involving dates and timestamps.

* A [Temporal API Spec](https://github.com/tc39/proposal-temporal) is expected to enhance JavaScript engines with improved date and time handling capabilities.

