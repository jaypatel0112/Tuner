# TUNER APP
![Tunner](https://github.com/user-attachments/assets/63538daf-7e49-411d-bfc2-ac7686b49f1d)


Welcome to **TUNER APP**, a music application where users can explore and play songs from various genres and artists. This app is designed to provide a seamless music experience with a user-friendly interface and robust features.

## Features

### 1. **Greetings Page**
- Upon launching the app, users are greeted with a welcoming page that showcases the passion for music.
- A "Let’s Play" button directs users to the main interface.

### 2. **Tab Bar Controller**
- The app features a tab bar with two main sections:
  - **Genre (Music) Bar**: Displays different music genres.
  - **Favorite (Like) Bar**: Shows a list of songs liked by the user.

### 3. **Google Firebase Authentication**
- Users can sign in using their Google accounts for easy access to the app.

### 4. **Genre Page**
- Displays various music genres fetched from an API in JSON format.
- Each genre is represented with an image and name.

### 5. **Favorite Songs**
- Users can like songs, which are then stored in the "Favorite" section.
- Songs can be played or paused with a single tap.
- Users can remove songs from their favorites list.

### 6. **Navigation and Album Details**
- Selecting a genre (e.g., "Pop") navigates to a list of artists within that genre.
- Each artist's page shows their albums, including album art, name, and release date.
- Selecting an album displays its songs, which can be played or added to favorites.

### 7. **Audio Playback**
- The app uses **AVPlayer** to handle audio playback, allowing users to play and pause songs seamlessly.

## APIs Used

- **URLSession**: Fetches data (genres, albums, artists, and songs) from the Deezer API in JSON format.
- **AVPlayer**: Manages audio playback, including loading, playing, and pausing songs.
- **Google Firebase**: Simplifies user authentication with Google Sign-In.

## Challenges Faced

1. **UI Design and Constraints**:
   - Designing collection view cells and applying constraints was time-consuming and required extensive troubleshooting.
   
2. **Data Handling**:
   - Learning to use **URLSession** and **JSONDecoder** to fetch and display data from the API was a significant challenge.
   - Managing audio data with **AVPlayer** required careful handling of song IDs and durations.

3. **Navigation**:
   - Implementing navigation between different views (genre, artist, album, and song) using segues was complex.

4. **Limitations**:
   - No logout button due to time constraints.
   - Lack of a search feature, which would enhance user experience.
   - Minor glitches that occasionally required restarting Xcode.

## Future Improvements

- Add a **logout button** and a **user profile page**.
- Implement a **search feature** to allow users to find songs by name, genre, or artist.
- Enhance the UI/UX for a more polished experience.

## What I Learned

- Gained hands-on experience with **URLSession**, **AVPlayer**, and **Google Firebase**.
- Learned to manage complex navigation and data flow in an iOS app.
- Understood the importance of proper UI constraints and design.
- Discovered the power of **CocoaPods** for integrating third-party libraries like Firebase.

---

This project was an exciting and challenging journey, and I’m proud of what I’ve accomplished. I look forward to improving it further and building more apps in the future!**TUNER APP**<br/>
I have created a song application where user can play different song from different genres and different singers. 

In this app, when a user starts with the application the user will be directed to the greetings page as shown on the left side. I have set a cover page for it which shows the passion for the song. When a user tries clicking on the button saying “Let’s Play” it gets directed to the tab bar controller which has 2 slides: i) Genre(Music) bar and ii) Favorite(Like) bar. The default one is the Genre.

I have however used a google firebase authentication for Sign In purpose. Using this user can login through the google account of his own which can be an easy access to the application use.

The screenshot on the right shows how the genre page looks. This shows all the different types of genre names and image which are getting fetched as data using API in JSON form and getting it inserted in the genre view cell in the UIImage view. However, this tab bar controller also have a “Like” bar tab where you can go on by clicking  on it.

When you click on it this slide shows all the songs which you have liked. This slide has the view cell which contains image, song name and duration along with the like button option in-case a user wants to remove the song from their list of favorites. When a user taps on a song it starts playing and tapping on it for the second time stops it from playing. But if you want to see different songs, the user needs to again go back to the Music section of the slide which sends the user back to the music genre.

When you click on a particular genre, let's say “Pop” it shows all the singers which have songs in that genre like Justin Bieber, Doja Cat, Ed Sheeran etc…. This is through the navigation controller. Every slide from genre slide has an option to go to the list of like songs. So the user can access it whenever he wants as he won’t have to come back to the homepage every time.

This slide gives a user list of all the albums sung by the singer in the form of view cell as well. In this user can select the album he wants to play and the release date which is along with the data coming through the API. This is also stored in the form of a view cell which has images for every album, it’s name and date of release.

When a user clicks on the album he is directed to the list of the songs which has song name and time stored in the view cell with an option to like it which is stored in the like section. When the user taps on the song from the list it starts playing and tapping again on it pauses it.

**Project Discussion:**

So, the API features I have used are URLSession, AVPlayer, and Google Firebase. Discussing each API in detail below:
URLSession: In this program URLSession makes a network request using a URL provided from Deezer application to extract different Genres, Album, Singers and Songs of those singers using the JSON data coming through the url.
AVPlayer: This API from apple is used to play the playback of the audio content as well as used to pause it too. This task like loading is also handled by it coming from the URL from Deezer app. However, it is used to initialize, control and manage the content within the audiomanager class.
Google Firebase: I have used this API to make login simple for a user as they can use a simple method for signing into the app using their google email id.

There were definitely many challenges I faced while doing this project. The very first was the phase of this project, I was not able to decide which part I should do first. In short, I was not able to figure out where I should start, however I started with creating a homepage first. Most of my screens are collection view cells so my next big challenge was fitting the view cell and giving it constraints which was one of the most tedious tasks for which I googled a lot because when I gave constraints to one thing the other showed a disturbance. This was basically done on static data, not the data coming from the url. So, I was able to set it at first. Using only navigation clicks did not have to work so I had to use segue for navigation as I had to go to the different slides from every view cell in the genre, album, and singer view controller. But this was just all about the UI of the view controller. The challenges raised its level when I had to pass the data to the UI to show because I had to learn how the URLSession API worked to extract the data from the url provided. For that I had to learn how the JSONDecoder works which decodes the Json data coming from the url and presents it on my app for different parts like images of artists, and genres. Along with it I also used AVPlayer to load a song which manage the audio data coming through the url at first it seems easy but this was the first time for me which I deal with audio data because it is easy to use the string data put it as required but for audio data it was a bit difficult cause I had to take care of each song id, and song duration each time for every song data coming and also learned a lot stuffs while dealing with it. 
However, the app works fine but it’s not perfect as there are certain limitations to it as this is the very basis of the song app. Beginning with the login page as I set up the firebase for login I haven’t actually kept a log out button for this because of the time constraint as I was able to implement this feature in the last couple of days as my main purpose was learning so. As I was not able to set the profile page I would like to improve as it is one of the main pages which every user needs to see. Along with this, one limitation or a back step for this app is not having a search option as users sometimes know the song name but don’t know what genre it falls in or whose actually is the singer. So, the user usually searches for the song but in this there is no search option which is a feature I think was required but I was not able to provide.
When I started with the assignments there were a couple of problems I was facing like not being able to link buttons properly or not able to run the test but later when I reinstalled the xcode it ran correctly. Even after that there were some minor glitchs which I saw but they were not creating a problem. They go away if we restart the xcode.
I always thought that how hard can it be to drag and drop the features and make them work but this proved me wrong. It is tough and exciting at the same time. When I started I did not know how well or how I was going to complete this project but I was always excited to do something because it was the very first time that I was working alone on an ios application project. There were some positives too to work on this like I got to learn a lot of things regarding the API’s and also about the concepts which were implemented in the project. Also, I learned one great thing that as I used a cocoapods for firebase setup they create you a workspace separately where your whole project gets added to. That was something amazing. This whole project will be something I will not forget for a long time.
I am attaching the link of the project video with this project file.
