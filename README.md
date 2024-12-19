# Web Developer Tools

A collection of web-based utilities for developers working with various data formats and file uploads.

## Table of Contents
- [Overview](#overview)
- [Tools](#tools)
  - [File Upload Utility](#file-upload-utility)
  - [JSON Log Extractor](#json-log-extractor)
  - [SAML Decoder](#saml-decoder)
  - [HAR Reader](#har-reader)
  - [All-In-One Docker Container](#all-in-one-docker-container)
- [Usage](#usage)

## Overview

This repository contains a set of standalone HTML tools that can be run directly in a browser without requiring a server. Each tool is designed to handle specific development and debugging tasks.

## Tools

### File Upload Utility
[file_upload.html](file_upload.html)

A drag-and-drop file upload interface with the following features:
- Multiple file upload support
- Progress tracking
- Case number association
- Real-time upload status
- Drag and drop interface

### JSON Log Extractor
[json-log-extractor.html](json-log-extractor.html)

A tool for processing JSON log files with these capabilities:
- Extracts and formats JSON log entries
- Two view modes: Newline Delimited and Prettified Raw Field
- Copy to clipboard functionality
- Download processed results
- Raw value extraction

### SAML Decoder
[saml_decoder.html](saml_decoder.html)

A utility for decoding SAML responses with these features:
- Base64 SAML response decoding
- XML formatting and prettifying
- Copy to clipboard functionality
- Select all content option
- Syntax highlighting

### HAR Reader
[har_reader.html](har_reader.html)

A comprehensive HTTP Archive (HAR) file analyzer featuring:
- Detailed request/response analysis
- Timeline visualization
- Advanced filtering options
- Search functionality
- Context menu with export options
- Request/response details viewer
- Timing breakdown visualization

### All-In-One Docker Container
[diagnostic-tools.tgz](diagnostic-tools.tgz)

A Docker image containing all tools served via nginx web server. To use:

1. Import the Docker image:

```bash
docker load -i diagnostic-tools.tgz
```

2. Run the container:

```bash
docker run -d --name diagnostic-tools -p 8080:80 diagnostic-tools
```

3. Access the tools:
- Open your browser
- Navigate to `http://localhost`
- All tools will be available via the index page

The Docker container provides:
- Nginx web server
- All tools pre-configured
- No external dependencies
- Isolated environment
- Easy deployment

## Usage

You can either:
1. Use individual HTML files:
   - Download the desired HTML file
   - Open it in a modern web browser
   - No server or installation required

2. Use the Docker container:
   - Import and run the Docker image
   - Access all tools via `http://localhost`
   - Requires Docker to be installed

Each tool is self-contained and can be used offline, either as standalone files or through the Docker container.

## Browser Compatibility

These tools are designed to work with modern browsers and have been tested with:
- Chrome (recommended)
- Firefox
- Edge

## Security Note

All processing is done locally in your browser. No data is sent to external servers (except for the File Upload Utility which requires a server endpoint configuration).

## License

MIT License - Feel free to use and modify these tools for your needs.