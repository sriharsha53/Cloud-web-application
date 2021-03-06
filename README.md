Image Manipulation Web App
==========================

**Team**
##### Mohammed Aamer Fnu
##### Vikas Reddy Vanteru
##### Sri Harsha Jilludumudi
##### Anand Kumar Taridalu Subrahmanyam

URL: http://dem-ode.appspot.com/
------------------------------------

> Created a Google App Engine application 
> to perform image manipulations submitted by the user
> using URL with additional parameters. User can rotate
> the image, change the Contrast, Sharpness, Brightness and
> i_m_feeling_lucky feature provided by Image API which adjusts
> image contrasts and color levels.

## Google AppEngine web services used in the project
 - Image Transformation API (with PIL)
 - Google Cloud Datastore and Blobstore
 - NDB Datastore API
 - Memcache - for Page Hits
 - Urlfetch - for fetching Image URL
 - Image Library
 - Mail
 - I am feeling lucky Image API

## Functionality
 - The user can use both local images and image urls for editing
 - The user can apply the image enhancers to desired level by adjusting the slider levels as required
 - The user will be able to download the edited image from the page
 - The user will be able to provide feedback in text and also give rating for the website
 - The user-ratings and feedback are shown real-time at the end of the page, after user gives feedback

##Highlights

#### The page hits are observed for the web-site using memcache

### Customized access management 
######  using OTP (One Time Passcode) authentication mechanism
**passcodes expire when session ends** | **passcodes emailed** | **uses MD5 hash with random padding**
- The user is allowed to enter a valid email id, if the email format is not correct, user is notified and prompted again
- When a valid email is entered by the user, he gets a 6-digit alpha-numeric passcode to his email immediately
- User can then enter this one-time passcode(OTP) to login into the website
- User cannot re-use this passcode for future logins. It is valid only for **ONE** time and expires when session ends
- The passcode is generated by manipulating the MD5 hash code and adding a random padding which is valid only for the user session. This makes the authentication mechanism a **robust** and **secure** one

### Image Enhancements
- Python PIL and Google App-Engine's Images library have been used to manipulate the images
- JPG and PNG are the formats accepted, with size-limit per image is maximum of 3 MB.

### Feedback
- Feedback is taken from user using the star-rating and text-box inputs
- These two values are stored in the datastore
- All user feedbacks are retrieved from the datastore, and are displayed at the bottom of the page

# Version
1.0

# Example
An Sample image url is submitted by the user.

 - Web app homepage
**dem-ode.appspot.com**



