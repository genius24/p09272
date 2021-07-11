======================================================
Title: ADVANCED TOPICS IN WEB DEVELOPMENT 2 CW1 REPORT
======================================================



### Welcome to my projects report below are the links to all project files

======================================================
Task1  :  extract-to-csv.php
	Link:	
------------------------------------------------------	
Task2a :  normalize-to-xml.php
	Link:
------------------------------------------------------	
Task2b :  air-quality.xsd
	Link:
------------------------------------------------------	
Task3  :  Visualisation.php
	Link:
------------------------------------------------------	
Task4  :  Report.md (current document)
	Link:
======================================================



> ## Project Reflection
>For my task1 (Cleanse and Refactor the Data) , I used a stream parser (e.g fopen instead of readfile) to read line by line of the data, for each line I performed the adjustments required to cleanse and refactor the data. This means that I did not have to wait until the entire data is read before I could process the data. The file is being read in smaller chunks which means that it uses less memory to store data, a less memory intensive program means that it will have better performance. Readfile() opens a file for reading, reads the data, and then prints it to the output buffer at the same time. This is not ideal for a very large file, as it is too memory intensive. Whereas, fopen() reads bytes from a given file handle, this is not only faster but less memory intensive. This with the added bonus of being able to process the data whilst it is being read, whereas with readfile() you can only process the file after it has been read. 
>
>For my task2a, I had the option using a dom parser (XMLReader or SimpleXML) or simply parsing the CSV and outputting the xml myself to a specific file. I choose to use the latter. But let me explain my understanding of XMLReader and SimpleXML. Both tools are good for parcing data, but they differ slightly in the same I described for task1 that fopen() could read file in smaller chunks whereas readfile() reads the entire file before it can be processed, In the same manner SimpleXML reads the file entirely before having access to it, on the other hand XMLReader allows you to gather the data you need to perform an operation, after the operation you can skip to the next node. This means no massive data build up. So once again, XMLReader less memory intensive and SimpleXML very memory intensive. It is much better to use a XMLReader for larger files and a SimpleXML parser for smaller files. For example its very slow to read a file line by line, because we cannot access the data we need quickly enough, But if we have a smaller file, it is better to read it all at once and then find the data we require. This is where I think that SimpleXML is useful for, because with smaller files you don’t have to worry about the memory or the speed at which the data is read. But in a file where you want to process every single line of a document, a XMLReader parser is the better option because it allows processing of the file whist it is read. This would also be the better option if you are going to be processing the data only once or not regularly. This is because if you are going to be reading the same file multiple times, it is much better to just have it all read into memory first and then you can quickly access it afterwards multiple times.
I created the xml file using stream parsers as I found it to be very quick when generating the csv file, so I then decided to also use the same process to generate an xml file. And it was fast, processing the files in under 30 seconds. Stream parsers would be like use an XMLReader in this instance. But simply simply parsing the CSV and outputting the xml myself to a specific file was the option I choose. 
>
>Thoughts on learning objectives:  I managed to meet the objectives successfully, afterwards the data was easily human readable, and much quicker to visualize or make use of the data. It shows how important it is to ensure that large amounts of data are structured to be easily processed for access and better visualization. I managed to produce a cleansed CSV, then an XML. Then I applied the optimized data in a world like environment by implementing and visualizing the data using a web-based charts. I have made use of the following tools; PHP, XML & XPATH, Parsing, DOM (minimal), JavaScript & JSON and Learned 

 




