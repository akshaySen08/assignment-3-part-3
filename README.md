# assignment-3-part-3
Internet Computing Assignment 3 Part 3

Steps to run the application:

1. Make sure you have Java installed on your computer.
2. Install eclipse, and editor for writing Java applications.
3. On the left hand side of the eclipse editor click on file option.
4. Select "open application folder from computer".
5. After selecting the folder, right click on the main folder visible on the left hand side work space of application.
6. Click on Run as -> Java Application.

----------------------------------------------------------------------------------------------------------------------------------

StAX is a Java-based API to parse XML document in a similar way as SAX parser does. But there are two major difference between the two APIs −

StAX is a PULL API, whereas SAX is a PUSH API. It means in case of StAX parser, a client application needs to ask the StAX parser to get information from XML whenever it needs. But in case of SAX parser, a client application is required to get information when SAX parser notifies the client application that information is available.

StAX API can read as well as write XML documents. Using SAX API, an XML file can only be read.

Environment Setup
In order to use StAX parser, you should have stax.jar in your application's classpath.
Following are the features of StAX API −

Reads an XML document from top to bottom, recognizing the tokens that make up a well-formed XML document.

Tokens are processed in the same order that they appear in the document.

Reports the application program the nature of tokens that the parser has encountered as they occur.

The application program provides an "event" reader which acts as an iterator and iterates over the event to get the required information. Another reader available is "cursor" which acts as a pointer to XML nodes.

As the events are identified, XML elements can be retrieved from the event object and can be processed further.

When to Use?
You should use a StAX parser when −

You can process the XML document in a linear fashion from top to down.

The document is not deeply nested.

You are processing a very large XML document whose DOM tree would consume too much memory. Typical DOM implementations use ten bytes of memory to represent one byte of XML.

The problem to be solved involves only a part of the XML document.

Data is available as soon as it is seen by the parser, so StAX works well for an XML document that arrives over a stream.

Disadvantages of SAX
We have no random access to an XML document, since it is processed in a forward-only manner.

If you need to keep track of data that the parser has seen or where the parser has changed the order of items, then you must write the code and store the data on your own.

XMLEventReader Class
This class provides iterator of events which can be used to iterate over events as they occur while parsing an XML document.

StartElement asStartElement() − Used to retrieve the value and attributes of an element.

EndElement asEndElement() − Called at the end of an element.

Characters asCharacters() − Can be used to obtain characters such as CDATA, whitespace, etc.

XMLEventWriter Class
This interface specifies methods for creating an event.

add(Event event) − Add event containing elements to XML.

XMLStreamReader Class
This class provides iterator of events which can be used to iterate over events as they occur while parsing an XML document.

int next() − Used to retrieve next event.

boolean hasNext() − Used to check further events exists or not.

String getText() − Used to get text of an element.

String getLocalName() − Used to get name of an element.

XMLStreamWriter Class
This interface specifies methods for creating an event.

writeStartElement(String localName) − Add a start element of given name.

writeEndElement(String localName) − Add an end element of given name.

writeAttribute(String localName, String value) − Write attributes to an element.
