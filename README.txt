MSTUDY-01
for University of Michigan EECS 481 Winter 2017

Jacob Durrah (jdurrah)
Meredith Keesling (merek)
Justin Patrick (jmpat)
Paul Scott (paulscot)

The app should be currently deployed, and so you can visit
http://m-study1.meteorapp.com/ to use it.  If it is unavailable, or if
for any other reason you wish to deploy it locally, please follow these steps:

1. Visit meteor.com and download Meteor onto your machine
2. Clone our MStudy repository from https://github.com/jdurrah1/mstudy.git
3. Open the command prompt in the M-Study-MeteorVersion folder (may need to run as admin)
4. Type "meteor npm install"
5. Type "meteor"
6. Go to http://localhost:3000/ in your browser

Remember, these steps are not always necessary, only if you need to deploy it yourself.


Omega Release functionality:

When loading our app's page, you can see the dashboard, which
displays the clipboard and several buttons.  The clipboard's purpose is to
store text that the user types in, pastes in, or records.  The button's
functions are as follows:

Record -	Clicking this button once will make the browser begin
		recording audio.  When you click a second time, the recording
		will stop, the audio will be saved to a wav file, then converted into
		a flac file to be sent to the Google speech-to-text API.  The API will
		transcribe this into text, then send it back to our app, and this text
		will be added to the MStudy clipboard.

Download .wav -	After starting and stopping a voice recording, you have the option to
		download the recording as a wav file to your computer's downloads folder.

Save -		Stores the message currently on the clipboard into the database.
		All of your saved messages can be seen in the list on the right.

Cut -		Takes the message on the clipboard, copies it to your computer's
		clipboard and empties the MStudy clipboard.

Copy -		Takes the message on the clipboard and copies it to your
		computer's clipboard.

Clear -		Empties the MStudy clipboard.

Download	Download the contents of the MStudy clipboard as a
as .txt -	.txt file to your computer's downloads folder.
		The title of the file is the string's first 16 characters.

Download	Download the contents of the MStudy clipboard as a .doc file
as .doc -	(can be opened in Microsoft Word) to your computer's downloads folder.
		The title of the file is the string's first 16 characters.

Upload		When clicking Choose File and locating a text file on your
a .txt -	computer, you can then click the upload button to fill the clipboard
		with the string contents of that file.

Upload		Click Choose File and select a wav file on your computer.  It will then
a .wav -	upload this, convert to flac, send to the Google speech API, and add this
		transcribed text into the MStudy clipboard.

Appearance	Clicking this will show 8 different color selectors, to change any of the
options -	following 8 colors: page background, page text, buttons background,
		buttons text, clipboard background, clipboard text, saved docs background,
		and saved docs text.  Clicking "apply changes" will apply all of your
		color choices at once.


The list on the right side contains all of the messages you have saved.  In order to save
messages, you must first sign in with an email and password using the Sign In button in
the bar on the top.  Clicking the X button on a message in the list will delete it, and
clicking the << button will copy it to the MStudy clipboard to edit.