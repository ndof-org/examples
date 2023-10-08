# [examples.ndof.org](http://examples.ndof.org)


## JSON Newline Delimited Objects Format

The newline delimited objects format is a text-based data format used to store structured data. It is similar to the JSON format but delimited by newline characters instead of commas. Each line in the file contains a single object, and each object can contain multiple key-value pairs separated by colons.

Here is an example of an object in newline delimited objects format:

```
{
    "name": "John Doe",
    "age": 25,
    "email": "john@example.com"
}
```

This object contains three key-value pairs: "name", "age", and "email". These pairs are separated by colons and enclosed in curly braces.

A newline delimited objects file can contain multiple objects, each separated by a newline character. Here is an example of a file with multiple objects:

```
{"name": "John Doe", "age": 25, "email": "john@example.com"}
{"name": "Jane Smith", "age": 30, "email": "jane@example.com"}
{"name": "Bob Johnson", "age": 40, "email": "bob@example.com"}
```

This format is often used for data interchange or storage in web-based applications because it is lightweight and easy to parse. It is also human-readable



## Multiple object format data: XML, JSON, XML, ...


Newline Delimited Objects format is typically used with JSON, due to its relatively simple and compact format that can easily be put into a single line. However, it can also be applied to XML, HTML, and a few other simple text formats, as long as the data structure doesn't require multi-line entries. Here's the example for JSON, XML, and HTML :
It has many advantages including the ability to stream very large amounts of data, to consume data incrementally, and it can be processed by line even though the complete document is not available.


### JSON Lines File: [data.jsonl](data.jsonl)
A single line in JSON Lines format is a valid JSON object, surrounded by curly brackets {}.
```jsonl
{"name": "John", "age": 30, "city": "New York"}
{"name": "Jane", "age": 35, "city": "Chicago"}
{"name": "Bob", "age": 40, "city": "Los Angeles"}
```


### XML Lines File: [data.xml](data.xml)
A single line in an XML Lines format is a valid XML object, surrounded by opening and closing tags.
However, there's no standard convention for XML lines since XML was designed to be used as a nested and not a line-based format.
So, using XML in this way is not as commonly seen as using JSON Lines. 

```xml
<Person><name>John</name><age>30</age><city>New York</city></Person>
<Person><name>Jane</name><age>35</age><city>Chicago</city></Person>
<Person><name>Bob</name><age>40</age><city>Los Angeles</city></Person>
```


### HTML Lines File: [data.html](data.html)
```html
<div><h1>John</h1><p>Age: 30</p><p>City: New York</p></div>
<div><h1>Jane</h1><p>Age: 35</p><p>City: Chicago</p></div>
<div><h1>Bob</h1><p>Age: 40</p><p>City: Los Angeles</p></div>
```

### Example with multi-format data in a single file: [data.ndof](data.ndof)
```json
{"name": "John", "age": 30, "city": "New York"}
<Person><name>Jane</name><age>35</age><city>Chicago</city></Person>
{"name": "Jane", "age": 35, "city": "Chicago"}
<Person><name>John</name><age>30</age><city>New York</city></Person>
<div><h1>Bob</h1><p>Age: 40</p><p>City: Los Angeles</p></div>
```


These formats are often used in areas such as big data and machine learning where processing large amounts of data is needed. 
They are also used in APIs that return multiple JSON or XML objects and when storing semi-structured data.
As for CSV, it's inherently a newline delimited format, with each line representing one record, with fields separated by commas or some other delimiter, so it doesn't need to be treated or formatted differently.


## Summary

While many file formats could technically be written in a single line, it breaks readability and convention for many formats. That said, the most common file formats that can naturally and conveniently be expressed in single lines include:

#### JSON Lines (.jsonl, .ndjson)
This format is probably the most common when it comes to newline delimited data. Each line in a .jsonl file represents a valid JSON object.

#### CSV (Comma Separated Values)
Each line in a CSV file represents a record and the fields in the record are separated by commas.

#### TSV (Tab Separated Values)
Similar to CSV but the fields are separated with tabs instead of commas.

#### Txt (Text format)
Text files can certainly be written in one line, as there's no structural formatting, though usually are not for readability.

#### Log files
Log files often use a newline delimited format, where each line is a separate log entry.

#### INI (Windows Initialization files)
It can be written in a single line approach with each section separated by a specific character.

Keep in mind, formats like XML, HTML, or YAML can be written in a single line, but it's generally discouraged because it makes them extremely difficult to read and doesn't adhere to the conventions of those file formats.



Please note, using XML, HTML (or any other formats that were designed to be multi-line and nested) in single-line delimited objects format is atypical and has lots of potential issues with readability, complexity, and data integrity. For these formats, it's generally better to use their standard multi-line formats.

---

+ [edit](https://github.com/ndof-org/examples/edit/main/README.md)
+ [github](https://github.com/ndof-org/examples/)
