TITLE: Basic React-PDF Implementation with Page Navigation in TypeScript/React
DESCRIPTION: This example demonstrates basic usage of React-PDF components with React hooks to track the number of pages and current page. It renders a PDF document and provides simple navigation information.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_4

LANGUAGE: tsx
CODE:
```
import { useState } from 'react';
import { Document, Page } from 'react-pdf';

function MyApp() {
  const [numPages, setNumPages] = useState<number>();
  const [pageNumber, setPageNumber] = useState<number>(1);

  function onDocumentLoadSuccess({ numPages }: { numPages: number }): void {
    setNumPages(numPages);
  }

  return (
    <div>
      <Document file="somefile.pdf" onLoadSuccess={onDocumentLoadSuccess}>
        <Page pageNumber={pageNumber} />
      </Document>
      <p>
        Page {pageNumber} of {numPages}
      </p>
    </div>
  );
}
```

----------------------------------------

TITLE: Basic Usage of React-PDF Components
DESCRIPTION: Example of using React-PDF components to display a PDF document with page navigation.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_2

LANGUAGE: typescript
CODE:
```
import { useState } from 'react';
import { Document, Page } from 'react-pdf';

function MyApp() {
  const [numPages, setNumPages] = useState<number>();
  const [pageNumber, setPageNumber] = useState<number>(1);

  function onDocumentLoadSuccess({ numPages }: { numPages: number }): void {
    setNumPages(numPages);
  }

  return (
    <div>
      <Document file="somefile.pdf" onLoadSuccess={onDocumentLoadSuccess}>
        <Page pageNumber={pageNumber} />
      </Document>
      <p>
        Page {pageNumber} of {numPages}
      </p>
    </div>
  );
}
```

----------------------------------------

TITLE: Handling Thumbnail Item Click in React-PDF
DESCRIPTION: Example function for handling click events on thumbnail items in React-PDF. The function receives an object containing destination information, page index, and page number, which can be used to navigate to the requested page.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_36

LANGUAGE: JavaScript
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: React PDF Page Component Basic Usage
DESCRIPTION: Shows the basic implementation of the Page component within a Document component. The Page component can also work standalone with a pdf prop obtained from Document's onLoadSuccess callback, though some advanced features may be limited.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_39

LANGUAGE: jsx
CODE:
```
<Document>
  <Page />
</Document>
```

----------------------------------------

TITLE: React Thumbnail Click Handler Example
DESCRIPTION: Example of an onItemClick handler function for the Thumbnail component that shows an alert when a thumbnail is clicked. The function receives an object with dest, pageIndex, and pageNumber properties.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_52

LANGUAGE: javascript
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: Using React PDF Outline Component Event Handler
DESCRIPTION: Example of implementing the onItemClick callback for the Outline component to handle navigation when a user clicks on an outline item. The callback receives destination information including page index and number.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_47

LANGUAGE: jsx
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: Page Loading Event Handlers
DESCRIPTION: Callback functions for handling page loading success and failure events.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_30

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while loading page! ' + error.message)
```

LANGUAGE: javascript
CODE:
```
(page) => alert('Now displaying a page number ' + page.pageNumber + '!')
```

----------------------------------------

TITLE: Handling Item Click in React-PDF
DESCRIPTION: A callback function for when an outline item or thumbnail is clicked in a PDF viewer. It receives an object with destination, page index, and page number information.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_30

LANGUAGE: javascript
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: React Outline Component Event Handler
DESCRIPTION: Example of an event handler for when an outline item is clicked in React PDF component. The handler receives page and destination information.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_32

LANGUAGE: javascript
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: Handling Item Click Events in React-PDF
DESCRIPTION: Example of an onItemClick callback function for React-PDF. This function is called when an outline item or thumbnail is clicked, allowing custom behavior such as navigation.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_16

LANGUAGE: JavaScript
CODE:
```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

TITLE: React Ref Creation Examples
DESCRIPTION: Examples showing different ways to create and use refs with the Page component's inputRef and canvasRef props
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_40

LANGUAGE: jsx
CODE:
```
(ref) => { this.myCanvas = ref; }

this.ref = createRef();
inputRef={this.ref}

const ref = useRef();
inputRef={ref}
```

----------------------------------------

TITLE: Rendering Event Handlers
DESCRIPTION: Callback functions for handling various rendering events including annotation layer, text layer, and general page rendering.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_31

LANGUAGE: javascript
CODE:
```
() => alert('Rendered the annotation layer!')
```

LANGUAGE: javascript
CODE:
```
() => alert('Rendered the page!')
```

LANGUAGE: javascript
CODE:
```
() => alert('Rendered the text layer!')
```

----------------------------------------

TITLE: React PDF Page Rotation Usage
DESCRIPTION: Demonstrates the rotation property usage in React PDF. The rotate prop accepts degrees (90, 180, 270) to control document orientation. 90 rotates right, 180 flips upside down, and 270 rotates left. This rotation applies globally, overriding individual page rotation settings.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_38

LANGUAGE: jsx
CODE:
```
<Document rotate={90}>
  <Page />
</Document>
```

----------------------------------------

TITLE: Handling Page Loading and Rendering Events in React-PDF
DESCRIPTION: Example callbacks for page loading and rendering events. These functions handle successful page loading, rendering completion, or errors during these processes.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_46

LANGUAGE: JavaScript
CODE:
```
(error) => alert('Error while loading page! ' + error.message)
```

LANGUAGE: JavaScript
CODE:
```
(page) => alert('Now displaying a page number ' + page.pageNumber + '!')
```

LANGUAGE: JavaScript
CODE:
```
(error) => alert('Error while loading page! ' + error.message)
```

LANGUAGE: JavaScript
CODE:
```
() => alert('Rendered the page!')
```

----------------------------------------

TITLE: Handling Successful Source Retrieval in React-PDF
DESCRIPTION: A callback function executed when document source is successfully retrieved from the file prop. It takes no parameters.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_36

LANGUAGE: javascript
CODE:
```
() => alert('Document source retrieved!')
```

----------------------------------------

TITLE: Handling Successful PDF Load in React-PDF
DESCRIPTION: A callback function executed when a PDF document is successfully loaded. It receives the loaded PDF object which contains document information.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_33

LANGUAGE: javascript
CODE:
```
(pdf) => alert('Loaded a file with ' + pdf.numPages + ' pages!')
```

----------------------------------------

TITLE: Importing CSS for PDF Text Layer Support
DESCRIPTION: This import statement adds the necessary CSS styles to properly display the text layer in PDFs rendered by React-PDF. This is required for text selection functionality.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_6

LANGUAGE: typescript
CODE:
```
import 'react-pdf/dist/Page/TextLayer.css';
```

----------------------------------------

TITLE: Tracking PDF Loading Progress in React-PDF
DESCRIPTION: A callback function that reports the loading progress of a PDF document. It receives an object with loaded and total bytes, allowing calculation of percentage complete.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_32

LANGUAGE: javascript
CODE:
```
({ loaded, total }) => alert('Loading a document: ' + (loaded / total) * 100 + '%')
```

----------------------------------------

TITLE: Handling Text Layer Events in React-PDF
DESCRIPTION: Example callback functions for text layer loading and rendering events. These functions handle text layer items being successfully loaded, rendering completion, or errors during these processes.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_45

LANGUAGE: JavaScript
CODE:
```
(error) => alert('Error while loading text layer items! ' + error.message)
```

LANGUAGE: JavaScript
CODE:
```
({ items, styles }) => alert('Now displaying ' + items.length + ' text layer items!')
```

LANGUAGE: JavaScript
CODE:
```
(error) => alert('Error while rendering text layer! ' + error.message)
```

LANGUAGE: JavaScript
CODE:
```
() => alert('Rendered the text layer!')
```

----------------------------------------

TITLE: Structure Tree Handler Functions
DESCRIPTION: Callback functions for handling structure tree loading success and failure events.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_28

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while loading structure tree! ' + error.message)
```

LANGUAGE: javascript
CODE:
```
(structTree) => alert(JSON.stringify(structTree))
```

----------------------------------------

TITLE: React Success Handler Implementation
DESCRIPTION: Example of a success handler function for when the outline is successfully retrieved in React PDF component.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_34

LANGUAGE: javascript
CODE:
```
(outline) => alert('The outline has been successfully retrieved.')
```

----------------------------------------

TITLE: Configuring PDF.js Options in React-PDF
DESCRIPTION: An object for passing additional parameters to PDF.js, such as cMapUrl for character maps, custom HTTP headers, and authentication settings.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_37

LANGUAGE: javascript
CODE:
```
{ cMapUrl: '/cmaps/' }
```

----------------------------------------

TITLE: Text Layer Event Handlers
DESCRIPTION: Callback functions for handling text layer loading success and failure events.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_29

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while loading text layer items! ' + error.message)
```

LANGUAGE: javascript
CODE:
```
({ items, styles }) => alert('Now displaying ' + items.length + ' text layer items!')
```

----------------------------------------

TITLE: React Ref Creation Examples
DESCRIPTION: Examples of different ways to create and use refs with the Document component
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_14

LANGUAGE: javascript
CODE:
```
(ref) => { this.myDocument = ref; }
```

LANGUAGE: javascript
CODE:
```
this.ref = createRef();
....
inputRef={this.ref}
```

LANGUAGE: javascript
CODE:
```
const ref = useRef();
....
inputRef={ref}
```

----------------------------------------

TITLE: Handling Success Events in React PDF Outline Component
DESCRIPTION: Example of implementing the onLoadSuccess callback for the Outline component to handle successful retrieval of the document outline. The callback receives the outline object.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_49

LANGUAGE: jsx
CODE:
```
(outline) => alert('The outline has been successfully retrieved.')
```

----------------------------------------

TITLE: React Error Handler Implementation
DESCRIPTION: Example of an error handler function for handling outline retrieval errors in React PDF component.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_33

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while retrieving the outline! ' + error.message)
```

----------------------------------------

TITLE: Using inputRef with React-PDF Document Component
DESCRIPTION: Examples of different ways to pass references to the Document component using the inputRef prop with function, createRef, or useRef.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_28

LANGUAGE: jsx
CODE:
```
(ref) => { this.myDocument = ref; }
```

LANGUAGE: jsx
CODE:
```
this.ref = createRef();
...
inputRef={this.ref}
```

LANGUAGE: jsx
CODE:
```
const ref = useRef();
...
inputRef={ref}
```

----------------------------------------

TITLE: Handling Successful Source Retrieval in React-PDF
DESCRIPTION: Example of an onSourceSuccess callback function for React-PDF. This function is called when the document source is successfully retrieved from the file prop.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_22

LANGUAGE: JavaScript
CODE:
```
() => alert('Document source retrieved!')
```

----------------------------------------

TITLE: Handling Source Error in React-PDF
DESCRIPTION: A callback function triggered when an error occurs while retrieving the document source from the file prop. It receives the error object.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_35

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while retrieving document source! ' + error.message)
```

----------------------------------------

TITLE: Handling Successful Document Load in React-PDF
DESCRIPTION: Example of an onLoadSuccess callback function for React-PDF. This function is called when a document is successfully loaded, providing access to the loaded PDF object.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_19

LANGUAGE: JavaScript
CODE:
```
(pdf) => alert('Loaded a file with ' + pdf.numPages + ' pages!')
```

----------------------------------------

TITLE: Using className prop with String or Array in React-PDF
DESCRIPTION: Examples of how to set the className prop in the Document component using either a string or an array of strings.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_22

LANGUAGE: jsx
CODE:
```
"custom-class-name-1 custom-class-name-2"
```

LANGUAGE: jsx
CODE:
```
["custom-class-name-1", "custom-class-name-2"]
```

----------------------------------------

TITLE: Tracking Load Progress in React-PDF
DESCRIPTION: Example of an onLoadProgress callback function for React-PDF. This function is called multiple times as the document loads, allowing progress tracking.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_18

LANGUAGE: JavaScript
CODE:
```
({ loaded, total }) => alert('Loading a document: ' + (loaded / total) * 100 + '%')
```

----------------------------------------

TITLE: Handling PDF Load Error in React-PDF
DESCRIPTION: A callback function triggered when an error occurs while loading a PDF document. It receives the error object as a parameter.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_31

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while loading document! ' + error.message)
```

----------------------------------------

TITLE: Configuring PDF.js Options in React-PDF
DESCRIPTION: Example of setting additional PDF.js options in React-PDF. This includes parameters like cMapUrl for character maps and custom HTTP headers for authorization.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_23

LANGUAGE: JavaScript
CODE:
```
{ cMapUrl: '/cmaps/' }
```

----------------------------------------

TITLE: Specifying PDF File Sources in React-PDF
DESCRIPTION: Examples of different ways to provide PDF files to the Document component using the file prop, including URL, imported file, or parameter object.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_26

LANGUAGE: jsx
CODE:
```
"https://example.com/sample.pdf"
```

LANGUAGE: javascript
CODE:
```
import importedPdf from '../static/sample.pdf'
```

LANGUAGE: jsx
CODE:
```
{ url: 'https://example.com/sample.pdf' }
```

----------------------------------------

TITLE: PDF Annotation Loading Callbacks
DESCRIPTION: Event handler examples for successful and failed annotation loading operations.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_27

LANGUAGE: javascript
CODE:
```
(annotations) => alert('Now displaying ' + annotations.length + ' annotations!')
```

----------------------------------------

TITLE: Ref Creation Examples in React
DESCRIPTION: Multiple approaches to create and use refs with React-PDF components using createRef and useRef hooks.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_26

LANGUAGE: JSX
CODE:
```
// Function ref
(ref) => { this.myCanvas = ref; }

// CreateRef usage
this.ref = createRef();
//...
inputRef={this.ref}

// UseRef usage
const ref = useRef();
//...
inputRef={ref}
```

----------------------------------------

TITLE: Custom Text Renderer Function
DESCRIPTION: Example of a custom text renderer function that replaces instances of 'ipsum' with marked text
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_41

LANGUAGE: javascript
CODE:
```
({ str, itemIndex }) => str.replace(/ipsum/g, value => `<mark>${value}</mark>`)
```

----------------------------------------

TITLE: Configuring Parcel 2 for PDF.js Worker
DESCRIPTION: This modification shows how to adjust the PDF.js worker URL specifically for Parcel 2 bundler by using the npm: protocol in the URL.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_13

LANGUAGE: diff
CODE:
```
 pdfjs.GlobalWorkerOptions.workerSrc = new URL(
-  'pdfjs-dist/build/pdf.worker.min.mjs',
+  'npm:pdfjs-dist/build/pdf.worker.min.mjs',
   import.meta.url,
 ).toString();
```

----------------------------------------

TITLE: Setting External Link Target in React-PDF
DESCRIPTION: Examples of possible values for the externalLinkTarget prop to control where links in PDF annotations will open.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_25

LANGUAGE: jsx
CODE:
```
"_self"
```

LANGUAGE: jsx
CODE:
```
"_blank"
```

LANGUAGE: jsx
CODE:
```
"_parent"
```

LANGUAGE: jsx
CODE:
```
"_top"
```

----------------------------------------

TITLE: Handling Source Retrieval Errors in React-PDF
DESCRIPTION: Example of an onSourceError callback function for React-PDF. This function is called when an error occurs while retrieving the document source from the file prop.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_21

LANGUAGE: JavaScript
CODE:
```
(error) => alert('Error while retrieving document source! ' + error.message)
```

----------------------------------------

TITLE: Defining Custom NoData Content in React-PDF
DESCRIPTION: Demonstrates different ways to specify custom content for the noData prop in React-PDF. This prop determines what the component displays when no PDF file is specified.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_15

LANGUAGE: JavaScript
CODE:
```
"Please select a file."
```

LANGUAGE: JSX
CODE:
```
<p>Please select a file.</p>
```

LANGUAGE: JavaScript
CODE:
```
this.renderNoData
```

----------------------------------------

TITLE: Error Handler Function
DESCRIPTION: Example of an error handler function for annotation loading errors
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_42

LANGUAGE: javascript
CODE:
```
(error) => alert('Error while loading annotations! ' + error.message)
```

----------------------------------------

TITLE: React Thumbnail Class Name Examples
DESCRIPTION: Examples showing how to pass class names to the Thumbnail component either as a space-separated string or as an array of strings.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_53

LANGUAGE: javascript
CODE:
```
"custom-class-name-1 custom-class-name-2"
["custom-class-name-1", "custom-class-name-2"]
```

----------------------------------------

TITLE: Importing CSS for PDF Annotation Support
DESCRIPTION: This import statement adds the necessary CSS styles to properly display annotations in PDFs rendered by React-PDF. This is required for features like links to work correctly.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_5

LANGUAGE: typescript
CODE:
```
import 'react-pdf/dist/Page/AnnotationLayer.css';
```

----------------------------------------

TITLE: Configuring React-PDF with Local cMaps
DESCRIPTION: Configuration for the Document component with options to use locally hosted cMaps. Defines options outside the React component to avoid unnecessary re-renders.
SOURCE: https://github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_15

LANGUAGE: typescript
CODE:
```
// Outside of React component
const options = {
  cMapUrl: '/cmaps/',
};

// Inside of React component
<Document options={options} />;
```
