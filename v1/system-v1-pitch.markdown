# App: Colours: Phase #1

Domain: https://colours.brickmmo.com
GitHub: https://github.com/codeadamca/brickmmo-colours 
Application Purpose:
This application will provide a series of tools related to the official LEGO™ colour palette. This will include a small website for visitors to browse, search, and convert colours as well as an API for other BrickMMO applications to incorporate the LEGO ™ colour palette.

## Front-End:
Front end facing application will include the following features:

- Browse LEGO™ colour palette
- Search for LEGO™ colours using colour keywords
- Convert existing colours from text, CMYK, or RGB to the LEGO™ colour palette

Application will include similar UI and features to this HTML Symbols tool:
https://www.toptal.com/designers/htmlarrows/symbols/


## Back-End:
Application will include a control panel to achieve the following:

- Login to control panel
- Add, edit, and delete LEGO™ colours
- Import LEGO™ colour palette from [ReBrickable API:](https://rebrickable.com/api/)

## API:
Application API will include the following API calls:

| Method | Endpoint | Description |
| ---------- | --------- | --------- |
| GET | /api/colours | A list of colours. Returns: A list of all LEGO™ colours. Each colour will include ID, name, RGB, CMYK, transparency, BrickLink ID, and BrickLink name. |
| POST | /api/convert | Converts a specified colour to a LEGO™ colour palette colour **Parameters**:colour (required): RGB, CMYK, or text colour **Returns**: A single colour including ID, name, RGB, CMYK, transparency, BrickLink ID, BrickLink name, a match distance.  |