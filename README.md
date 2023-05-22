# Taiwan E-Invoice Open API

Taiwan Electronic Invoice Open API is based on the Turnkey transmission and MIG file format established by the Ministry of Finance of Taiwan. It adheres to the principles of RESTful architecture and utilizes JWT (Json Web Token) authentication.

To get started, you can register and authenticate your email through the [Users/Register](https://api.utunote.com/swagger) endpoint. Upon successful registration, you will receive a token that can be used for various operations for test.

Please visit our [official website](https://utunote.com) for more detailed information.

中文版說明請至 [Swagger](https://api.utunote.com/swagger) 頁面.


## Basic functionalities

1. Generate invoices and allowances in all formats, including B2B (exchange and storage) and B2C storage.

2. Automatically generate all formats of receipt in PDF format, including invoice receipt (Format 1, Format 2) and allowance receipt (Format 1, Format 2).

3. Perform various operations on invoices and allowances, including "void," "reject," "cancel," and "confirm".

4. Automatically retrieve invoices and allowances downloaded from Turnkey and import to database.

5. Automatically retrieve invoice track numbers distributed by the main platform for each period and import to database.

6. Integrate with government API tools such as the "Electronic Invoice Business API" and the "Business Registration Inquiry API", allowing direct usage within this API.


## Getting Started

All functionalities are accessed using the base URL https://api.utunote.com, following the RESTful principles based on the respective endpoint paths.

For example, to initiate the invoice generation functionality, you would make a POST request to https://api.utunote.com/EInvoiceAPI/Invoice/Invoice.

In most endpoints, you will need to include the JWT token in the Authorization header for authentication.

For example, you would include the JWT token in the Authorization header as follows:

Authorization: Bearer <JWT Token>

Please make sure to replace <JWT Token> with the actual JWT token.


## Directory Descriptions

Each directory has its subdirectories or function descriptions, the following is the description of each root directory:

**EInvoiceAPI**: Contains all functionalities related to electronic invoices.

**BusinessAPI**: Various tools required for searching business registration information, validating mobile barcodes, and other functionalities related to issuing electronic invoices.

**Users**: Functionalities related to user management and operations.
