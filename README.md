**HTML Validator in C++**

**Purpose**:

  The HTML Validator, written in C++ programming language, is designed to parse the HTML code, extract information about various HTML elements (tags), and perform validation checks based on specific criteria.

**Components**:

  1.	TagInfo Structure:

    •	The TagInfo structure represents information about an HTML tag. It contains members such as tagName, id, classes, text, href, target, and children.
    
    •	TAGNAME: Stores the name of the HTML tag (e.g., "div", "a", "h1").
    
    •	ID: Stores the ID attribute of the tag, if present.
    
    •	Classes: Stores a set of class names associated with the tag, if present.
    
    •	TEXT: Stores the text content within the tag.
    
    •	HREF: Stores the value of the "href" attribute for anchor tags (<a>).
    
    •	TARGET: Stores the value of the "target" attribute for anchor tags.
    
    •	CHILDREN: Stores pointers to child tags of the current tag.
  
  **2.	Utility Functions**:
  
    •	ltrim, rtrim, and trim: These functions trim leading and trailing whitespace characters from a string.
 
    •	extractHREF: Function used to extract the “href” attribute from a string representing an HTML tag.
    
    •	extractTarget: Function used to extract the “target” attribute from an HTML tag in a string.
    
    •	extractID: Function used to extract the “ID” attribute from an HTML tag in a string.
    
    •	extractClasses: Function used to extract the “class” attribute from an HTML tag in a string.
    
    •	extractTagName: Function used to extract the “tag name” attribute from an HTML tag in a string.
    
    •	extractText: Function used to extract the “text content” attribute from an HTML tag in a string.

  **3.	Parsing HTML Code**:
    
    •	The extractCode function parses the HTML code line by line from standard input.
    
    •	This function identifies the opening, closing, and self-closing tags. A tree-like structure is constructed, representing the hierarchy of HTML elements.

    •	It populates instances of the TagInfo structure containing information about each tag.
  
  **4.	Validation Checks**:
    
    •	The validation function recursively traverses the tag tree and performs validation checks based on specific criteria.
    
    •	It checks for the presence of specific attributes (e.g., "id", "href") and content (e.g., text within <h1> tags).
    
    •	Validation checks are performed by updating a vector check with binary values (1 for pass, 0 for fail) corresponding to each criterion.
 
  **Main Function**:

    •	The main function orchestrates the overall execution of the program.
    
    •	It initializes necessary variables, sets up input and output redirection, invokes the HTML parsing, and invokes the          validation function. Then, finally, it outputs the results of validation checks.
  
  **How to Use**:
    
    1. Prepare an HTML file to be validated.
    
    2. Redirect the input of the program to read from the HTML file.
    
    3. Run the program.
    
    4. Check the output to see the results of the validation checks.

  **Example**:
    
    Suppose we have an HTML file with various elements such as <h1>, <a>, <div>, etc. The program will parse the HTML code,      extract information about each tag, and perform validation checks based on specific criteria defined in the code.

  **Limitations and Considerations**:

    1. The program assumes well-formed HTML code and may not gracefully handle all edge cases or malformed HTML.
    
    2. Validation criteria are predefined in the code and may need to be adjusted based on specific requirements or standard

