# Requirements Document

## Capstone Plan:

This application will provide a series of tools related to the official LEGO™ color palette. This will include a smalll website for visitors to browse, search, and convert colors as well as an API for other BrickMMO applications to incorporate the LEGO™ color palette.

## Front-End Features (Navdeep Kaur):

Front end facing application will include the following features:
- Browse LEGO™ color palette
- Search for LEGO™ colors using color keywords
- Convert existing colors from text, CMYK, or RGB to the LEGO™ color palette.

## Back-End Features (Udip Mandora):
Application will include a control panel to achieve the following: - Login to control panel
- Add, edit, and delete LEGOTM colors
- Import LEGO™ color palette from [ReBrickable API:](https://rebrickable.com/api/)

## Technology Stack:

Front-End:
Front-End will use React technology to do all the data transferring and showing content on the web page.

Back-End:
Back-End will use Laravel technology to create the control panel where all the CRUD operations will take place such as add color, delete color and edit color. It is also going to use the API which is mentioned above.

Application Explanation:
LEGO is an important thing for this world now where not only is it playing with bricks anymore but in the technological world LEGO is making a difference too. The APIs LEGO has developed are helping everyone now to share their things digitally as well. The problem this application is going to solve is that this application will provide colors from the Lego color palette using [API](https://rebrickable.com/api/). As LEGO has a lot of colors, this application will use that API to fetch all those colors and use them and convert existing colors from text, CMYK, or RGB to the LEGO™ color palette.

The goal of this application is to change the colors from text, CMYK, or RGB to the LEGO color palette.

## User Story:
1. User will land on home page 
    * Sign in option
2. Seeing random colors suggestion on home page (without sign in) 
3. If user do sign-in, welcome message on home page
4. Manage colors in user’s own account (Add, delete and update)
    * Add color
    * Edit Color
    * Update Color
5. Search for colors by giving color name or rgb
6. As an output, user will see list of colors
7. Click on particular color and see the information in name, RGB and CMYK values 
8. User that color
9. Logout option if signed in

## Must have Features:
- Must have color name
- Must display RGBm CMYK form of a color
- Must have all the colors from API
- User can search any color from the LEGO palette

## Should have Features:
- Display a LEGO brick piece as an example when user clicks on a specific color
- Suggestion of similar colors after finding the specific color given by user

## Nice-to-have Features:
- Animations in lego bricks while going through the page
- Import colors from color palette and then use that to search for colors
- Having options to search for coloors using both color name and rgb value
- Having autocomplete in search funcitonality such as if a user search color which starts from **'R'**, user will have a list of all colors which starts from **'R'**.

# Database Flows & Database Diagram:
![flow chart diagram](/images/v1-flowchart.png)

## Challenges & Potenial Barriers:
1. Fetching data from API
2. Showing information based on different user's accoount
3. Searching operation for colors
4. CRUD operations can take little time
5. Converting color into CMYK form and then display it

## Appendix

| Description | Date |
| ------------- | ----------- |
| Create mock up, wireframes for LEGO prooject & test API | 5/19/2023 |
| Start Work on Back End (Udip Mandora) | 5/26/2023 |
| Start Work on Back End (Navdeep Kaur) | 5/26/2023 |
| Solving errors | 6/3/2023 |
| Finishing whole website | 6/17/2023 |
| Presentation | 6/23/2023 |