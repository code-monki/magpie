# Analysis

This document provides the system analysis of the MCMS.

## Definitions

- **Administrator** - an object representing a person with system management privileges
- **Article** - an object that represents an article (PDF format)
- **Book** - an object that represents an eBook (PDF or ePub format)
- **Magazine** - an object that represents an electronic magazine (PDF or ePub format)
- **User** - an object representing a person with the privleges to search or read articles, books, or magazines managed by the MCMS

### Article Analysis

An article is contained in a single PDF file that can be downloaded or viewed. Each article should have the following "metadata":

- Title
- Subtitle
- Author(s)
- File location
- File name
- Publication Date
- Article Source
- Copyright date
- Keywords

In some cases it is likely that all of the above metadata may not be available and in those cases the metadata item will either not exist or have a value of null/undefined.

### Book Analysis

A book is contained in a single file in PDF or ePub format<sup>*</sup> Each book should have the following metadata:

- Title
- Subtitle
- Author(s)
- File location
- File name
- Publication Date
- Publisher
- Copyright date
- ISBN
- Keywords

As with articles, any metadata items that are not available should have a value of null/undefined.

### Magazine Analysis

A magazine is contained in a single file in PDF format<sup>*</sup> Each magazine should have the following metadata:

- Title
- Subtitle
- Author(s)
- File location
- File name
- Publication Date
- Publisher
- Volume
- Issue
- Copyright date
- ISSN
- Keywords

As with articles, any metadata items that are not available should have a value of null/undefined.


