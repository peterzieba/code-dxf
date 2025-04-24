# code-dxf
## Overview
Rough attempt at making a `.dxf` language extension for VSCode

Currently this only folds "SECTION" "ENDSEC" pairs and recognizes 999 entries as comments.

For a proper reference of the file format, see: 
* [Autodesk 2012 DXF Reference](https://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [Autodesk 2014 DXF Reference](https://images.autodesk.com/adsk/files/autocad_2014_pdf_dxf_reference_enu.pdf)
* [Autodesk DXF Archive](https://aps.autodesk.com/developer/overview/autocad-dxf-archive)

## DXF Terminology
`record` - Is always two consecutive lines. The first is the group code, the second is the value whose type & meaning are determined by that code.

`group code` - An integer that determines the nature of the next line. There are quite a few of these. Common ones are 0 (new section, new entity, or the file end), 999 (comment).

## Make a vs-code extension
* https://github.com/microsoft/vscode-generator-code/blob/main/generators/app/templates/ext-language/vsc-extension-quickstart.md

Contributions are welcome...
