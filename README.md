## Basic React-PDF Implementation with Page Navigation in TypeScript/React
 This example demonstrates basic usage of React-PDF components with React hooks to track the number of pages and current page. It renders a PDF document and provides simple navigation information.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_4

 tsx

``
import { useState } from 'react';
import { Document, Page } from 'react-pdf';

function MyApp() {
  const [numPages, setNumPages] = useState<number>();
  const [pageNumber, setPageNumber] = useState<number>(1);

  function onDocumentLoadSuccess({  {   void {
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
``

----------------------------------------

## Basic Usage of React-PDF Components
 Example of using React-PDF components to display a PDF document with page navigation.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_2

 typescript

```
import { useState } from 'react';
import { Document, Page } from 'react-pdf';

function MyApp() {
  const [numPages, setNumPages] = useState<number>();
  const [pageNumber, setPageNumber] = useState<number>(1);

  function onDocumentLoadSuccess({  {   void {
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

## React PDF Page Component Basic Usage
 Shows the basic implementation of the Page component within a Document component. The Page component can also work standalone with a pdf prop obtained from Document's onLoadSuccess callback, though some advanced features may be limited.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_39

 jsx

```
<Document>
  <Page />
</Document>
```

----------------------------------------

## Using React PDF Outline Component Event Handler
 Example of implementing the onItemClick callback for the Outline component to handle navigation when a user clicks on an outline item. The callback receives destination information including page index and number.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_47

 jsx

```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

## React Thumbnail Click Handler Example
 Example of an onItemClick handler function for the Thumbnail component that shows an alert when a thumbnail is clicked. The function receives an object with dest, pageIndex, and pageNumber properties.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_52

 javascript

```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

## React Outline Component Event Handler
 Example of an event handler for when an outline item is clicked in React PDF component. The handler receives page and destination information.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_32

 javascript

```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

## Using className prop with String or Array in React-PDF
 Examples of how to set the className prop in the Document component using either a string or an array of strings.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_22

 jsx

```
"custom-class-name-1 custom-class-name-2"
```

 jsx

```
["custom-class-name-1", "custom-class-name-2"]
```

----------------------------------------

## React Ref Creation Examples
 Examples showing different ways to create and use refs with the Page component's inputRef and canvasRef props
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_40

 jsx

```
(ref) => { this.myCanvas = ref; }

this.ref = createRef();
inputRef={this.ref}

const ref = useRef();
inputRef={ref}
```

----------------------------------------

## React Success Handler Implementation
 Example of a success handler function for when the outline is successfully retrieved in React PDF component.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_34

 javascript

```
(outline) => alert('The outline has been successfully retrieved.')
```

----------------------------------------

## Configuring React-PDF with CDN-hosted cMaps
 Alternative configuration for the Document component that uses cMaps hosted on an external CDN instead of local files.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_16

 typescript

```
// Outside of React component
import { pdfjs } from 'react-pdf';

const options = {
   `//unpkg.com/pdfjs-dist@${pdfjs.version}/cmaps/`,
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Defining Custom NoData Content in React-PDF
 Demonstrates different ways to specify custom content for the noData prop in React-PDF. This prop determines what the component displays when no PDF file is specified.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_15

 JavaScript

```
"Please select a file."
```

 JSX

```
<p>Please select a file.</p>
```

 JavaScript

```
this.renderNoData
```

----------------------------------------

## React Component Import Example
 Example of importing a PDF file in a React component
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_13

 javascript

```
import importedPdf from '../static/sample.pdf'
```

----------------------------------------

## React Ref Creation Examples
 Examples of different ways to create and use refs with the Document component
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_14

 javascript

```
(ref) => { this.myDocument = ref; }
```

 javascript

```
this.ref = createRef();
....
inputRef={this.ref}
```

 javascript

```
const ref = useRef();
....
inputRef={ref}
```

----------------------------------------

## Configuring React-PDF Document Component with CDN cMaps
 Alternative approach to using cMaps from an external CDN instead of bundling them with the application. This utilizes the unpkg CDN to serve cMaps files from the pdfjs-dist package.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_7

 tsx

```
// Outside of React component
import { pdfjs } from 'react-pdf';

const options = {
   `//unpkg.com/pdfjs-dist@${pdfjs.version}/cmaps/`,
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Handling Thumbnail Item Click in React-PDF
 Example function for handling click events on thumbnail items in React-PDF. The function receives an object containing destination information, page index, and page number, which can be used to navigate to the requested page.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_36

 JavaScript

```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

## Ref Creation Examples in React
 Multiple approaches to create and use refs with React-PDF components using createRef and useRef hooks.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_26

 JSX

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

## React Error Handler Implementation
 Example of an error handler function for handling outline retrieval errors in React PDF component.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_33

 javascript

```
(error) => alert('Error while retrieving the outline! ' + error.message)
```

----------------------------------------

## Using inputRef with React-PDF Document Component
 Examples of different ways to pass references to the Document component using the inputRef prop with function, createRef, or useRef.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_28

 jsx

```
(ref) => { this.myDocument = ref; }
```

 jsx

```
this.ref = createRef();
...
inputRef={this.ref}
```

 jsx

```
const ref = useRef();
...
inputRef={ref}
```

----------------------------------------

## Configuring React-PDF with Local cMaps
 Configuration for the Document component with options to use locally hosted cMaps. Defines options outside the React component to avoid unnecessary re-renders.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_15

 typescript

```
// Outside of React component
const options = {
   '/cmaps/',
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Rendering Event Handlers
 Callback functions for handling various rendering events including annotation layer, text layer, and general page rendering.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_31

 javascript

```
() => alert('Rendered the annotation layer!')
```

 javascript

```
() => alert('Rendered the page!')
```

 javascript

```
() => alert('Rendered the text layer!')
```

----------------------------------------

## Using References with React PDF Components
 Examples of three different ways to use refs with React PDF  using a callback function, using createRef, and using the useRef hook.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_51

 jsx

```
(ref) => { this.myOutline = ref; }
```

 jsx

```
this.ref = createRef();
...
inputRef={this.ref}
```

 jsx

```
const ref = useRef();
...
inputRef={ref}
```

----------------------------------------

## Handling Errors in React-PDF Document Component
 Examples of different ways to handle and display errors using the error prop, including string, React element, or function approach.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_23

 jsx

```
"An error occurred!"
```

 jsx

```
<p>An error occurred!</p>
```

 jsx

```
this.renderError
```

----------------------------------------

## Configuring React-PDF Document Component with Local cMaps
 Example of setting up the Document component with options to use local cMaps that have been copied to the build output. This ensures proper rendering of PDFs with various character encodings.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_6

 typescript

```
// Outside of React component
const options = {
   '/cmaps/',
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Handling Success Events in React PDF Outline Component
 Example of implementing the onLoadSuccess callback for the Outline component to handle successful retrieval of the document outline. The callback receives the outline object.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_49

 jsx

```
(outline) => alert('The outline has been successfully retrieved.')
```

----------------------------------------

## Configuring React-PDF with CDN-hosted Standard Fonts
 Alternative configuration for the Document component that uses standard fonts hosted on an external CDN instead of local files.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_21

 typescript

```
// Outside of React component
import { pdfjs } from 'react-pdf';

const options = {
   `//unpkg.com/pdfjs-dist@${pdfjs.version}/standard_fonts/`,
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Handling Item Click Events in React-PDF
 Example of an onItemClick callback function for React-PDF. This function is called when an outline item or thumbnail is clicked, allowing custom behavior such as navigation.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_16

 JavaScript

```
({ dest, pageIndex, pageNumber }) => alert('Clicked an item from page ' + pageNumber + '!')
```

----------------------------------------

## Configuring PDF.js Worker in React-PDF
 Different methods to configure the PDF.js worker, including importing the worker, using external CDN, and supporting legacy browsers.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_1

 typescript

```
import { pdfjs } from 'react-pdf';

pdfjs.GlobalWorkerOptions.workerSrc = new URL(
  'pdfjs-dist/build/pdf.worker.min.mjs',
  import.meta.url,
).toString();
```

 typescript

```
import { pdfjs } from 'react-pdf';

pdfjs.GlobalWorkerOptions.workerSrc = `//unpkg.com/pdfjs-dist@${pdfjs.version}/build/pdf.worker.min.mjs`;
```

 typescript

```
pdfjs.GlobalWorkerOptions.workerSrc = new URL(
  'pdfjs-dist/legacy/build/pdf.worker.min.mjs',
  import.meta.url,
).toString();
```

----------------------------------------

## Configuring PDF.js Options in React-PDF
 Example of setting additional PDF.js options in React-PDF. This includes parameters like cMapUrl for character maps and custom HTTP headers for authorization.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_23

 JavaScript

```
{  '/cmaps/' }
```

----------------------------------------

## Configuring React-PDF with Local Standard Fonts
 Configuration for the Document component with options to use locally hosted standard fonts. Defines options outside the React component to avoid unnecessary re-renders.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_20

 typescript

```
// Outside of React component
const options = {
   '/standard_fonts/',
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Specifying PDF File Sources in React-PDF
 Examples of different ways to provide PDF files to the Document component using the file prop, including URL, imported file, or parameter object.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_26

 jsx

```
"//example.com/sample.pdf"
```

 javascript

```
import importedPdf from '../static/sample.pdf'
```

 jsx

```
{  '//example.com/sample.pdf' }
```

----------------------------------------

## Configuring PDF.js Options in React-PDF
 An object for passing additional parameters to PDF.js, such as cMapUrl for character maps, custom HTTP headers, and authentication settings.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_37

 javascript

```
{  '/cmaps/' }
```

----------------------------------------

## Handling Successful Source Retrieval in React-PDF
 A callback function executed when document source is successfully retrieved from the file prop. It takes no parameters.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_36

 javascript

```
() => alert('Document source retrieved!')
```

----------------------------------------

## React Thumbnail Class Name Examples
 Examples showing how to pass class names to the Thumbnail component either as a space-separated string or as an array of strings.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_53

 javascript

```
"custom-class-name-1 custom-class-name-2"
["custom-class-name-1", "custom-class-name-2"]
```

----------------------------------------

## Configuring React-PDF Document Component with CDN Standard Fonts
 Alternative approach to using standard fonts from an external CDN instead of bundling them with the application. This utilizes the unpkg CDN to serve standard font files from the pdfjs-dist package.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_12

 tsx

```
// Outside of React component
import { pdfjs } from 'react-pdf';

const options = {
   `//unpkg.com/pdfjs-dist@${pdfjs.version}/standard_fonts/`,
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Configuring React-PDF Document Component with Local Standard Fonts
 Example of setting up the Document component with options to use local standard fonts that have been copied to the build output. This ensures proper rendering of PDFs that use standard fonts.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_11

 tsx

```
// Outside of React component
const options = {
   '/standard_fonts/',
};

// Inside of React component
<Document options={options} />;
```

----------------------------------------

## Importing CSS for PDF Text Layer Support
 This import statement adds the necessary CSS styles to properly display the text layer in PDFs rendered by React-PDF. This is required for text selection functionality.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_6

 typescript

```
import 'react-pdf/dist/Page/TextLayer.css';
```

----------------------------------------

## Page Loading Event Handlers
 Callback functions for handling page loading success and failure events.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_30

 javascript

```
(error) => alert('Error while loading page! ' + error.message)
```

 javascript

```
(page) => alert('Now displaying a page number ' + page.pageNumber + '!')
```

----------------------------------------

## Handling Error Events in React PDF Outline Component
 Example of implementing the onLoadError callback for the Outline component to handle errors that occur while retrieving the document outline. The callback receives the error object.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_48

 jsx

```
(error) => alert('Error while retrieving the outline! ' + error.message)
```

----------------------------------------

## Setting Class Names for React PDF Components
 Examples showing two ways to set custom class names for React PDF components - using a string with space-separated class names or an array of class name strings.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_50

 jsx

```
"custom-class-name-1 custom-class-name-2"
```

 jsx

```
["custom-class-name-1", "custom-class-name-2"]
```

----------------------------------------

## Configuring Next.js for React-PDF Without Turbopack
 This Next.js configuration resolves canvas dependency issues when using React-PDF without Turbopack by setting the canvas alias to false in webpack config.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_10

 diff

```
module.exports = {
+  (config) => {
+   config.resolve.alias.canvas = false;

+   return config;
+ },
}
```

----------------------------------------

## Text Layer Event Handlers
 Callback functions for handling text layer loading success and failure events.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_29

 javascript

```
(error) => alert('Error while loading text layer items! ' + error.message)
```

 javascript

```
({ items, styles }) => alert('Now displaying ' + items.length + ' text layer items!')
```

----------------------------------------

## Configuring Next.js Prior to v15 for React-PDF
 This configuration disables SWC minification in Next.js versions prior to v15.0.0-canary.53, which may be necessary for React-PDF to work correctly.
 //github.com/wojtekmaj/react-pdf/blob/main/packages/react-pdf/README.md#2025-04-11_snippet_12

 diff

```
module.exports = {
+  false,
}
```

----------------------------------------

## React Ref Implementation
 Examples of different ways to implement refs with the Outline component in React PDF, including function refs and createRef/useRef approaches.
 //github.com/wojtekmaj/react-pdf/blob/main/README.md#2025-04-11_snippet_35

 javascript

```
(ref) => { this.myOutline = ref; }

this.ref = createRef();
...inputRef={this.ref}

const ref = useRef();
...inputRef={ref}
```
