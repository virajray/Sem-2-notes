### <font color="#ff6000">The Basic Rules 🚨</font>
• XML is case sensitive 
• All start tags must have end tags 
• Elements must be properly nested 
• XML declaration is the first statement 
• Every document must contain a root element 
• Attribute values must have quotation marks 
• Certain characters are reserved for parsing

#### Common Errors for Element Naming ⚠
• Do not use white space when creating names for elements 
• Element names cannot begin with a digit, although names can contain digits 
• Only certain punctuation allowed – periods, colons, and hyphens

#### <font color="#ffc000">XML and HTML were designed with different goals:</font>

- <span style="background:#fdbfff">XML</span> was designed to carry data - with focus on what data is
- <span style="background:#fff88f">HTML</span> was designed to display data - with focus on how data looks
- XML tags are not predefined like HTML tags are

## <font color="#92d050">The XML Tree Structure</font>
XML documents are formed as **element trees**.

An XML tree starts at a **root element** and branches from the root to **child elements**.
All elements can have sub elements (child elements):

```xml
<root>  
  <child>  
    <subchild>.....</subchild>  
  </child>  
</root>
```


![[Pasted image 20240615202122.png]]
<font color="#ffff00">The image above represents books in this XML:</font>
```xml
<?xml version="1.0" encoding="UTF-8**"**?>  
<bookstore>  
  <book category="cooking">  
    <title lang="en">Everyday Italian</title>  
    <author>Giada De Laurentiis</author>  
    <year>2005</year>  
    <price>30.00</price>  
  </book>  
  <book category="children">  
    <title lang="en">Harry Potter</title>  
    <author>J K. Rowling</author>  
    <year>2005</year>  
    <price>29.99</price>  
  </book>  
  <book category="web">  
    <title lang="en">Learning XML</title>  
    <author>Erik T. Ray</author>  
    <year>2003</year>  
    <price>39.95</price>  
  </book>  
</bookstore>
```


