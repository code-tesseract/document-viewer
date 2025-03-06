# React Office Viewer: PDF, XLS, XLSX, DOCX

## Features

1. **Supported File Types**: Currently supports previewing **PDF, XLS, XLSX, and DOCX** files. More file types will be added in future updates.

2. **Automatic File Type Detection**:
    - The component can automatically recognize file types for **PDF, XLS, XLSX, DOC, DOCX, PPT, and PPTX** based on the file's `ArrayBuffer`.
    - While providing a file name or extension is recommended, it is not strictly required.
    - This mechanism helps prevent incorrect file type detection caused by misleading file extensions.

3. **Full-Featured PDF Viewer**:
    - The PDF viewer includes a fully functional **toolbar** with common features such as:
        - **Pagination**
        - **Zooming**
        - **Rotation**
        - **Printing**
        - **Thumbnail view**

4. **Multi-Language Support**:
    - The component supports both **English and Chinese** for in-app prompts.
    - You can set the preferred language using a parameter (**default: Chinese**).

5. **Built with React 16.8**:
    - The component is implemented based on **React 16.8**, ensuring compatibility with modern React features.

---

## Installation

```sh
npm install react-office-viewer
```

---

## Usage

```javascript
import Viewer from "react-office-viewer";

// If you only need to preview specific file formats, import them individually.
import { SheetViewer, PdfViewer, DocxViewer } from "react-office-viewer";
```

---

## Props and Parameters

```jsx
// Pass a file URL that returns the file stream.
<Viewer file="http://example.com/file.pdf" />

// Or, pass a File object.
<Viewer file={fileObject} />

<input type="file" onChange={this.getFileObject} />
getFileObject = (e) => {
  this.setState({ fileObject: e.target.files[0] });
};

// Additional optional parameters:
const params = {
  fileName: "example.docx", // (Optional) Name of the file
  locale: "en", // Language: 'zh' (Chinese) or 'en' (English)
  width: "100%", // Width of the viewer (string or number)
  height: 600, // Height of the viewer (string or number)
  timeout: 10000, // (Only for sheet/docx viewers) Timeout limit for fetching file URL
};

// Usage with additional parameters
<Viewer file="http://example.com/file.pdf" {...params} />;
```

---

## Demo
### Preview Examples
![PDF Preview](https://github.com/react-office-viewer/react-office-viewer/blob/gh-pages/build/pic/pdf.png)  
![DOCX Preview](https://github.com/react-office-viewer/react-office-viewer/blob/gh-pages/build/pic/docx.png)  
![XLSX Preview](https://github.com/react-office-viewer/react-office-viewer/blob/gh-pages/build/pic/xlsx.png)

---

## Dependencies
This package relies on the following libraries:
- **handsontable**
- **mammoth**
- **xlsx**
- **pdfjs-dist**  

