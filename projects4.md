# PDF Converter API

A simple API to convert Word documents (DOC/DOCX) into PDF files.

## Base URL
https://api.pdfconverter.com/v1

## Authentication

All requests require an API key.  
Include it as a header:  

Authorization: Bearer YOUR_API_KEY## Endpoints

### 1. Convert Word to PDF
**POST** `/convert`

**Parameters**
- `file` (required) – Word document (.doc or .docx)  
- `options` (optional) – conversion settings  

**Example Request**
```bash
curl -X POST https://api.pdfconverter.com/v1/convert \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -F "file=@document.docx"
```


## Error Handling

If something goes wrong, the API will return an error response in JSON format.  

**Example Error Response**
``` json
{
"status": "error",
  "message": "Invalid file format"
}
```

## License

This project is licensed under the MIT License.


