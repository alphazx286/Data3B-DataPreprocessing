# 					DATA IMPORTATION

#### **Define the data table concept.**

Data is complex, and all data is different. Accordingly, Data-tables  has a wealth of options which can be used to configure how it will  obtain the data to display in the table, and how it processes that data.



- Processing mode
- Data types
- Data sources



#### Define the data types: categorical, numeric, boolean, dates and strings.

​	In computer science and computer programming, a **data type** or simply **type** is an attribute of **data** which tells the compiler or interpreter how the programmer intends to use the **data**. This **data type** defines the operations that can be done on the **data**, the meaning of the **data**, and the way values of that **type** can be stored.

##### 	Categorical Variable

A categorical or discrete variable is one that has two or more categories (values). There are two types of categorical variable, **nominal**  and **ordinal**. 

A nominal variable has no intrinsic ordering to its categories.  For example, gender is a categorical variable having two categories (male and female) with no intrinsic ordering to the categories. An ordinal variable has a clear      ordering. For example, temperature as a variable with three *orderly* categories (low, medium and high). A **frequency table** is a  way of  counting how often each category of the variable in question  occurs. It may be enhanced by the addition of percentages that fall into each category.

| Univariate Analysis -              Categorical |                   |                                                              |
| ---------------------------------------------- | ----------------- | ------------------------------------------------------------ |
| **Statistics**                                 | **Visualization** | **Description**                                              |
| Count                                          | Bar Chart         | The number of values of the specified            variable.   |
| Count%                                         | Pie Chart         | The percentage of values of the specified          variable. |



##### Numeric Variable

A numerical or continuous variable (attribute) is one that may take on any value within a finite or infinite      interval (e.g., height, weight, temperature, blood glucose, ...). There are two types of numerical variables, **interval** and **ratio**. An interval variable has values whose differences are interpretable, but it does not  have a true zero. A good example is temperature in Centigrade degrees.  Data on an interval scale can be added and subtracted but cannot be  meaningfully multiplied or divided. For example, we cannot say that one day is twice as hot as another day. In contrast, a ratio variable has values with a true zero and can be added, subtracted, multiplied or divided.

|                                     |                   |                                                       |                                                              |
| ----------------------------------- | ----------------- | ----------------------------------------------------- | :----------------------------------------------------------: |
| **Statistics**                      | **Visualization** | **Equation**                                          |                       **Description**                        |
| Count                               | Histogram         | *N*                                                   | The number of values            (observations) of the variable. |
| Minimum                             | Box Plot          | *Min*                                                 |         The smallest value of          the variable.         |
| Maximum                             | Box Plot          | *Max*                                                 |         The largest value of the          variable.          |
| Mean                                | Box Plot          | ![img](http://www.saedsayad.com/images/Mean.png)      |     The sum of the          values divided by the count.     |
| Median                              | Box Plot          | ![img](http://www.saedsayad.com/images/Median.png)    | The middle value. Below and above          median lies an equal number of values. |
| Mode                                | Histogram         |                                                       | The most frequent value.          There can be more than one mode. |
| Quantile                            | Box Plot          | ![img](http://www.saedsayad.com/images/Quantiles.png) | A set of 'cut points'          that divide a set of data into groups containing equal numbers of          values (Quartile, Quintile, Percentile, ...). |
| Range                               | Box Plot          | *Max-Min*                                             |     The difference between maximum and          minimum.     |
| Variance                            | Histogram         | ![img](http://www.saedsayad.com/images/Variance.png)  |                A measure of data dispersion.                 |
| Standard            Deviation       | Histogram         | ![img](http://www.saedsayad.com/images/StDev.png)     |                 The square root of variance.                 |
| Coefficient of            Deviation | Histogram         | ![img](http://www.saedsayad.com/images/CV.png)        |    A measure of data dispersion divided by          mean.    |
| Skewness                            | Histogram         | ![img](http://www.saedsayad.com/images/Skewness.png)  | A measure of symmetry or asymmetry in the distribution          of data. |
| Kurtosis                            | Histogram         | ![img](http://www.saedsayad.com/images/Kurtosis.png)  | A measure of whether the data are peaked or flat relative to a normal distribution. |

##### Boolean Variables

Boolean variables are stored as 16-bit (2-byte) numbers, but they can only be **True** or **False**.

**Boolean** variables display as either:

- `True` or `False` (when **Print** is used), or
- `#TRUE#` or `#FALSE#` (when **Write #** is used).

Use the keywords **True** and **False** to assign one of the two states to **Boolean** variables.

When other  numeric types are converted to **Boolean** values, 0 becomes **False** and all other values become **True**.

When **Boolean** values are converted to other data types **False** becomes 0 and **True** becomes -1.

##### Dates

Holds IEEE 64-bit (8-byte) values that represent dates ranging from  January 1 of the year 0001 through December 31 of the year 9999, and  times from 12:00:00 AM (midnight) through 11:59:59.9999999 PM. Each  increment represents 100 nanoseconds of elapsed time since the beginning of January 1 of the year 1 in the Gregorian calendar. The maximum value represents 100 nanoseconds before the beginning of January 1 of the  year 10000.

Use the `Date` data type to contain date values, time values, or date and time values.

The default value of `Date` is 0:00:00 (midnight) on January 1, 0001.

You can get the current date and time from the DateAndTime class.

You must enclose a `Date` literal within number signs (`# #`). You must specify the date value in the format M/d/yyyy, for example `#5/31/1993#`, or yyyy-MM-dd, for example `#1993-5-31#`. You can use slashes when specifying the year first.  This requirement  is independent of your locale and your computer's date and time format  settings.

##### String Variables

A string is a data type used in programming, such as an integer and  floating point unit, but is used to represent text rather than numbers.  It is comprised of a set of characters that can also contain spaces and numbers.  For example, the word  "hamburger" and the phrase "I ate 3 hamburgers" are both strings.  Even  "12345" could be considered a string, if specified correctly.   Typically, programmers must enclose strings in quotation marks for the  data to recognized as a string and not a number or variable name.

For example, in the comparison:

if (Option1 == Option2) then ...

Option1 and Option2 may be variables containing integers, strings, or other data.  If the values are the same, the test returns a value of  true, otherwise the result is false.  In the comparison:

if ("Option1" == "Option2") then ...

Option1 and Option2 are being treated as strings.  Therefore the test is comparing the words "Option1" and "Option2," which would return  false.  The length of a string is often determined by using a null character.

#### Describe the common data formats: csv, json, xml y xls. 

##### Csv

| Full name        | CSV, Comma Separated Values (strict form as described in RFC 4180) |
| ---------------- | ------------------------------------------------------------ |
| Description      | CSV is a simple format for representing a rectangular array  (matrix) of numeric and textual values.  It an example of a "flat file"  format.  It is a delimited data format that has fields/columns separated by the comma character %x2C (Hex 2C) and records/rows/lines separated  by characters indicating a line break.  RFC 4180 stipulates the use of  CRLF pairs to denote line breaks, where CR is %x0D (Hex 0D) and LF is  %x0A (Hex 0A).  Each line should contain the same number of fields.  Fields that contain a special character (comma, CR,  LF, or double quote), must be "escaped" by enclosing them in double  quotes (Hex 22).  An optional header line may appear as the first line of the file with the same format as normal record lines.  This header will contain names corresponding to the fields in the file and should contain the same number of fields as the records in the rest  of the file.  CSV commonly employs US-ASCII as character set, but other  character sets are permitted. |
| Production phase | May be used at any stage in the life-cycle of a dataset.     |

##### Json

JSON (JavaScript Object Notation) is a lightweight data-interchange  format. It is easy for humans to read and write. It is easy for machines to  parse and generate. It is based on a subset of the  [JavaScript   Programming Language Standard   ECMA-262 3rd Edition - December 1999. JSON is a text format that is completely  language independent but uses conventions that are familiar to programmers of  the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python,  and many others. These properties make JSON an ideal data-interchange language.

JSON is built on two structures:

- A collection of name/value pairs. In various languages, this is realized    as an *object*, record, struct, dictionary, hash table, keyed list, or    associative array.
- An ordered list of values. In most languages, this is realized as an *array*,    vector, list, or sequence.

Example

<!DOCTYPE html>
<html>
<body><h2>Convert a JavaScript object into a JSON string, and send it to the server.</h2>
<script>
var myObj = { name: "John", age: 31, city: "New York" };
var myJSON = JSON.stringify(myObj);
window.location = "demo_json.php?x=" + myJSON;
</script>
</body>
</html>

Result

demo_json.php:

John from New York is 31

##### Xml

XML is a software- and hardware-independent tool for storing and  transporting data.

- XML stands for extensible Markup Language
- XML is a markup language much like HTML
- XML was designed to store and transport data
- XML was designed to be self-descriptive
- XML is a W3C Recommendation

The XML above is quite self-descriptive:

- It has sender information.
- It has receiver information
- It has a heading
- It has a message body.

But still, the XML above does not DO anything. XML is just information wrapped in tags.

Example:

<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
 </note> 

Result

--Note

To: Tove

From: Jani

--Reminder

Don't forget me this weekend!

##### Xls

XLS is an Excel Sheets binary file format, Microsoft Excel’s workbook files in use between 97-2003. Later Excel  versions use the XLSX extension. XLS and XLSX file formats contain all  the information from the worksheets in a workbook, including formatting, charts, images, formulas, etc. 

#### Differentiate between local and remote repositories: url, apis. 

A **software repository**, or “repo” for short, is a storage location for software packages. Often a table of contents is stored, as well as meta-data. Repositories  group packages. Sometimes the grouping is for a programming language,  such as CPAN for the Perl programming language, sometimes for an entire operating system, sometimes the license of the contents is the criteria.

At client side, a package manager helps installing from and updating the repositories. 

At server side, a software repository is typically managed by  source control or repository managers. Some of the repository managers  allow to aggregate other repository location into one URL and provide a  caching proxy. When doing continuous builds many artifacts are produced  and often centrally stored, so automatically deleting the ones which are not released is important.

API is the acronym for Application Programming Interface, which is a  software intermediary that allows two applications to talk to each  other. Each time you use an app like Facebook, send an instant message,  or check the weather on your phone, you’re using an API.



#### Identify the secure data transfer protocols. 

Secure file transfer is data sharing  via a secure, reliable delivery method. It is used to safeguard  proprietary and personal data in transit and at rest. Most secure file  sharing methods use standard protocols, including:

- **Secure File Transfer Protocol (SFTP)**
   SFTP transfers files with the Secure Shell (SSH) connection – SFTP is  an encrypted network protocol that can enable a remote login to operate  over a network that lacks security. SFTP offers encryption of commands and data. It also prevents passwords and  sensitive information from open transmission over the network.
- **File Transfer Protocol – Secure (FTPS)**
   FTPS offers encryption and uses an application layer wrapper, known as  Secure Sockets Layer (SSL) to enable secure and private communications  across a network.
- **Hypertext Transfer Protocol – Secure (HTTPS)**
  HTTPS secures websites when users are providing sensitive information like  credit card numbers or other personal information. The protocol offers  multiple layers of data protection including data integrity, encryption, and authentication.
- **Applicability Statement 2 (AS2)**
   AS2 is a standard used to transfer Electronic Data Interchange (EDI) messages and other data in real time. The AS2 protocol facilitates the ability to exchange AS2 EDI messages and other types of data over the HTTP or HTTPS protocol.



#### Describe the procedures for data importing. 

To use data produced by another application. The ability to import data is very important in software applications  because it means that one application can complement another. Many programs, for example, are designed to be able to import graphics in a variety of formats.

The opposite of importing is *exporting*, which refers to the ability of one application to format data for another application.

##### Hit-data import

Hit-data import lets you send hit data directly into Analytics. This  provides an alternative to using the tracking code, Collection API, the  Mobile SDKs, or the Measurement Protocol. Imported hits are added to  your Analytics property prior to any processing; therefore, your  imported data may be affected by processing-time actions, such as  filters. Because you are importing hits, this data can be seen by all  reporting views for that property (unless you specifically filter them  from selected views).

This type of import supports uploading the following types of data:

- **Refund Data**—align your internal ecommerce reporting with Analytics by importing ecommerce refund data.

##### Extended-data import

Extended-data import adds to (extends) the data already collected and processed, or being processed, for the selected reporting views.  Typically, this extended data is stored in a custom dimension or metric, though in some cases you might want to overwrite the default  information already gathered (for example, importing a campaign's Source or Medium dimension).

You can upload the following data types:

- **User Data**—create segments and remarketing lists that incorporate imported user metadata, such as a loyalty rating or lifetime customer value.
- **Campaign Data**—expand and reuse your existing non-Google campaign codes by importing ad campaign-related dimensions, such as source.
- **Geographical Data**—create custom geographical regions, allowing you to report on and analyze  Analytics data in ways that are better aligned with your business'  organization.
- **Content Data**—group content using imported content metadata, such as author, date published, and article category.
- **Product Data**—gain better merchandising insights by importing product metadata, such as  size, color, style, or other product-related dimensions.
- **Custom Data**—provides support for importing custom data sets.

##### Summary-data import

Summary-data import lets you sum uploaded metrics. Imported summary  data is applied to the selected reporting views after all processing and aggregation of collected data. This can be useful when you receive data in batches some time following hit collection, as summary data import  lets you add to or update your information as it becomes available.

Currently, summary data import supports the following import type:

- **Cost Data**—include 3rd party (non-Google) ad network clicks, cost and impression data to gain a more complete picture of your ad spend.



## bibliography

Web: https://support.google.com/analytics/answer/3191589?hl=en

Web: https://developer.mozilla.org/es/docs/Web/API/URL

Web: https://en.wikipedia.org/wiki/Software_repository

Web: https://docs.github.com/en/free-pro-team@latest/github/using-git/about-remote-repositories







