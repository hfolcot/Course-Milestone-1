# The Monkees Website by Heather Olcot

The website is required for a 1960s band who wish to showcase themselves, their work, pictures and a video, and also give their fans a method of contacting them to book performances at events. 

The website fulfils this need with four pages:

### index.html

The home page gives dates of upcoming public performances and shows pictures of the band. It also offers links to the band's social media pages. 

### about.html

The About page gives information about each individual band member.

### music.html

The Music page offers fans a video of one of their performances, as well as a menu where a song can be chosen and played.

### contact.html

The Contact page contains a form that can be filled in and submitted to the band to request a performance at an event.


## Functionality / Technologies

### General

The site links to Bootstrap 3.3.7 and makes use of its form styling and grid system.

The site links to Fontawesome 4.7.0 and makes use of icons for the social media and other links in the footer.

The site uses the Vesper Libre font from Google Fonts.

My own further styling has been done within css/styles.css

### Header and Footer

The Bootstrap grid system was utilised for the grids making up the header and footer. 

The header contains one of the supplied images which is being used as a logo. Clicking/tapping on this logo will take the user to the homepage - functionality that the average user has come to expect from a website.

The links in both header and footer have been amended so that they transition to a darker colour when they are hovered over.

The header is designed to compress into two rows of two links each with no logo and no padding at less than 768px width.

The footer will show only icons and no text at less than 768px width, to prevent cluttering of a smaller screen. 

### index.html

The main feature of the Home page is the showcase of pictures which are offered as a type of slideshow. This was achieved using a keyframes animation with multiple steps, each step being one picture. These keyframes have been repeated in styles.css to allow for functionality within different browsers.

The page should also draw the user's attention to the ability to book the band with a button (Book Us) under the picture slideshow. This button will take the user directly to contact.html. It has made use of the bootstrap styling (btn btn-primary) but with a change of colour to fit in with the colour scheme and draw the user's attention.

Next we have a basic bordered div containing details of the band's next public performance dates.

And finally there are social media icons which take the user to an external website in a separate browser tab.

### about.html

This page contains four separate bordered divs, each containing an unordered list of interesting trivia about each band member.

On a screen smaller than 992px, each band member will be displayed one per row. On a larger screen, they are shown two per row. 

### music.html

This is the page where the band are able to showcase their music in the form of a video and four audio files. (NB the audio files were downloaded from the CI provided github source but do not appear to work; other students have acknowledged that this was the same for them) 

The video uses html5 video controls and has a message in place for when this function is not supported. "Your browser does not support this video".

The video will shrink according to the screen width below 768px, this was achieved using a media query.

The song selection dropdown will take the user to a separate browser tab which plays the selected file. A separate browser tab was preferable otherwise there would have been no option to navigate back to the site without using the browser's back button.

The code for the dropdown box was taken from vvolkov's answer at https://stackoverflow.com/questions/14242466/creating-a-form-which-selects-a-downloadable-file?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa
and edited to work with the page's data.

The Play button again uses Bootstrap css for styling but with an edited colour for the main button and the hover function in styles.css, to fit in with the site's colour scheme.

### contact.html

The form contains fields to enter Name, Email, Phone Number, Date of Event and Comments.

The name, email and phone number are required fields but the date is not, acknowledging that the user may not have a specific date in mind yet. The comments box is also not enforced as required - it is limited to 1000 characters and the placeholder advises such. This was all achieved with the html code.

The styling of the form is done by Bootstrap except for margin, width and padding which are specified in styles.css. The form is set with media queries to fill 80% of the screen up to 768px and 40% of any larger screen widths, to maintain an easy to follow layout.

The text above the contact form was styled using IDs rather than classes to avoid their styles being unintentionally repeated elsewhere in the site.

The Submit button is styled with Bootstrap css for styling but with an edited colour for the main button and the hover function in styles.css, to fit in with the site's colour scheme.

The form uses the Post method but is not currently connected to a back end.

## Testing (Round 1)

The site was tested on a Safari browser on a Macbook by another user who found it easy to use and navigate, and that all functions behaved as expected.

I then tested the following:

(X = Functioning as expected)

Browser/Test | Opera | Firefox | Chrome | Edge | Safari
-----|-----|-----|-----|-----|-----
Display|About page has large gap below footer. All other pages OK|About page has large gap below footer. All other pages OK|About page has large gap below footer. All other pages OK|About page has large gap below footer. All other pages OK|X
Slideshow|X|X|X|Does not work|X
Contact form|X|X|X|X|X
All links|X|X|X|X|X
:hover functions|X|X|X|X|X
Video|X|X|X|X|X
Dropdown Box|X|X|X|X|X
Play button|X|Goes to expected page but error stating supported format not found|X|Goes to expected page but states that audio files isn't supported|Goes to expected page but states that audio files isn't supported
Submit button|X|X|X|X|405 not allowed error


#### Using Chrome's dev tools to test each page is displaying correcty at different screen widths

Screen width/Page display|Galaxy S5|Pixel 2|Pixel 2XL|iPhone 5/SE|iPhone 6/7/8|iPhone 6/7/8 Plus|iPhone X|iPad|iPad Pro
-----|-----|-----|-----|-----|-----|-----|-----|-----|-----
index.html|X|X|Large gap below footer|X|X|X|Large gap below footer|Large gap below footer|Page is only half the vh|
about.html|X|X|X|X|X|X|X|Large gap below footer|Page is only half the vh
music.html|X|Small gap below footer|Large gap below footer|X|X|Large gap below footer|Large gap below footer|X|Page is only half the vh
contact.html|X|X|X|X|X|X|X|X|Page is only half the vh
