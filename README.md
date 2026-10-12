✋ Hand Gesture Presentation Controller
A browser-based presentation controller that uses your webcam to recognize hand movements and navigate slides. This project is built as a single HTML file, with hand tracking powered by MediaPipe Hands.
✨ Features
Live camera preview with hand-landmark visualization.
Swipe right to move to the next slide.
Swipe left to move to the previous slide.
Swipe down to move to the next slide.
Swipe up to move to the previous slide.
On-screen Previous and Next buttons.
Pause and resume gesture recognition.
Keyboard arrow-key navigation.
A responsive layout for desktop and mobile-sized screens.
Swipe detection includes a movement threshold, dominant-direction check, cooldown, and re-arming after the hand becomes still to help reduce repeated or accidental navigation.
🧰 Built With
HTML5
CSS3
JavaScript
MediaPipe Hands for hand tracking, loaded from jsDelivr
📁 Project Structure
```text
.
├── Hand_Gesture_Presentation_Accurate(1).html
└── README.md
```
The HTML file includes the page structure, styling, JavaScript logic, and embedded slide images.
🚀 Getting Started
Option 1: Run locally
Download or clone this repository.
Open the project folder.
Serve the HTML file through localhost using a local web server.
Open the local URL in a modern browser.
Click Start Camera and allow camera permission.
Keep one hand visible in good lighting and swipe clearly in one direction.
> **Important:** Camera access generally requires a secure context, such as `localhost` or HTTPS. Opening the HTML file directly with a `file://` URL may not allow camera access in some browsers.
Option 2: Publish with GitHub Pages
Upload the HTML file and this `README.md` to your GitHub repository.
Open the repository's Settings → Pages.
Configure GitHub Pages to deploy from your chosen branch and folder.
Save the settings and wait for GitHub to publish the site.
Open the published HTTPS URL and allow camera access.
The page loads MediaPipe from a CDN, so an internet connection is needed for the hand-tracking library.
🖐️ Gesture Guide
Hand movement	Action
Swipe right ➡️	Next slide
Swipe left ⬅️	Previous slide
Swipe down ⬇️	Next slide
Swipe up ⬆️	Previous slide
Click Next	Next slide
Click Previous	Previous slide
Keyboard → or ↓	Next slide
Keyboard ← or ↑	Previous slide
The camera preview is mirrored, and the code accounts for that when interpreting horizontal swipes.
🎯 Tips for Better Recognition
Use good, even lighting.
Keep one hand fully visible inside the camera frame.
Start with your hand near the centre of the frame.
Swipe clearly in one direction rather than diagonally.
Move far enough for the gesture to pass the detection threshold.
Briefly hold your hand still between swipes so the controller can re-arm.
If the tracker does not load, check your internet connection and reload the page.
⚠️ Current Scope and Limitations
This version navigates the presentation displayed inside the webpage.
It does not directly control the separate Microsoft PowerPoint desktop application. A browser page cannot normally send commands to another desktop application without an additional local helper or integration.
Camera permission and browser support are required.
MediaPipe is loaded externally from a CDN, so the hand-tracking feature requires internet access.
The current presentation images are embedded in the HTML file.
🔒 Privacy
The page requests camera access to process the live hand image in the browser. Review the HTML and any external libraries before using it in a sensitive environment. This project does not describe a server-side video-upload feature.
🛠️ Troubleshooting
Camera does not start
Check that the browser has camera permission.
Use a modern browser and open the page through `localhost` or HTTPS.
Make sure another application is not exclusively using the camera.
Hand tracker fails to load
Check your internet connection.
Reload the page so the MediaPipe library can load from the CDN.
Slides change more than once
Make a clear swipe, then hold your hand still briefly before the next swipe.
Avoid diagonal or very small movements.
Gestures are not detected reliably
Improve lighting, keep your hand fully in frame, and swipe more distinctly.
🤝 Contributing
Suggestions and improvements are welcome. You can open an issue or submit a pull request with a clear explanation of the change.
📄 License
No license has been specified yet. Add a `LICENSE` file before granting others permission to reuse, modify, or distribute this project.
---
Made as a browser-based hand gesture presentation control project.
