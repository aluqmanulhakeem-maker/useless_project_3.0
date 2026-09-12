 <img width="1280" height="640" alt="git (1)" src="https://github.com/user-attachments/assets/8920b256-2ba8-4988-b824-5351134eb4bd" />



# AirCanvas 🎯

### Draw in the Air — Your Finger Is the Brush



---

## 📌 Basic Details

### Project Name

**AirCanvas**

### Team Name

`hazardianzz`

### Team Members

| Role          | Name                | College          |
| ------------- | ------------------- | ---------------- |
| **Team Lead** | **Muhammed Luqman** | MESCET Kunnukara |
| **Member 2**  | **Ayman Rasheed**   | MESCET Kunnukara |

---

# 🎨 Project Description

**AirCanvas** is a browser-based, touch-free digital drawing application that allows users to draw on a virtual canvas using nothing but their **finger and a webcam**.

The application uses **MediaPipe Hands** to detect and track the user's hand in real time. The position of the index fingertip is converted into coordinates on an HTML Canvas, allowing the user to create digital drawings by simply moving their finger through the air.

No mouse, touchscreen, graphics tablet, or stylus is required.

> **Your finger is the brush. The webcam is the sensor. The browser is the canvas.**

---

# 😂 The Problem That Doesn't Exist

Have you ever looked at your computer and thought:

> *"I wish I could draw on this without actually touching it."*

Normally, digital drawing requires a mouse, touchscreen, stylus, or graphics tablet.

But we decided to completely ignore all of those options.

So we created a solution to a problem that nobody really asked for:

### **What if you could draw on your computer... with your finger in the air?** ☝️

---

# 🚀 The Solution Nobody Asked For

**AirCanvas** transforms a normal webcam into a virtual drawing interface.

The user simply points their index finger toward the webcam and moves it through the air.

The system:

```text
Webcam
   ↓
MediaPipe Hands
   ↓
Hand Landmark Detection
   ↓
Index Fingertip Tracking
   ↓
Gesture Recognition
   ↓
Position Smoothing
   ↓
HTML Canvas
   ↓
Digital Drawing 🎨
```

The result is a simple and fun **touch-free drawing experience**.

---

# ✨ Key Features

* ☝️ **Touch-free air drawing**
* 🖐️ **Real-time hand tracking**
* ✏️ **Pen mode**
* 🧽 **Eraser mode**
* 🎨 **Multiple colors**
* 📏 **Adjustable brush size**
* ↩️ **Undo**
* ↪️ **Redo**
* 🗑️ **Clear canvas**
* 💾 **Save drawing as PNG**
* ✨ **Smooth fingertip tracking**
* 📊 **Real-time hand/status indicator**
* 🖥️ **Responsive interface**
* 🔒 **No backend required**
* 🗄️ **No database required**
* 🌐 **Runs directly in a web browser**

---
🎥 Project Demo
Video

🎬 Watch the AirCanvas Demo:

https://drive.google.com/file/d/1R7MAev_23gm6cs84eLQpbR2_p37b9xBZ/view?usp=sharing

The demonstration video showcases AirCanvas in action, including:

🖐️ Real-time hand detection
☝️ Index fingertip tracking
🎨 Drawing in the air
✏️ Pen mode
🧽 Eraser mode
🌈 Color selection
📏 Brush-size adjustment
↩️ Undo and redo
🗑️ Clear canvas
💾 Saving the final drawing
🔗 Additional Demos
🎥 Project Demo: https://drive.google.com/file/d/1R7MAev_23gm6cs84eLQpbR2_p37b9xBZ/view?usp=sharing
🌐 Live Application: [Add live demo link]
💻 GitHub Repository: [Add repository link]
# 🛠️ Technical Details

## Technologies Used

### Frontend

* **HTML5**
* **CSS3**
* **JavaScript**

### Computer Vision

* **MediaPipe Hands**

### Graphics

* **HTML Canvas API**

### Camera

* **WebRTC / `getUserMedia()`**

### Development

* **Visual Studio Code**
* **Live Server**

### External Resources

MediaPipe is loaded through a CDN, so no package manager or local installation is required.

---

# 💻 Hardware Requirements

AirCanvas requires only basic hardware:

* 💻 Laptop or Desktop
* 📷 Built-in or external webcam
* 🌐 Internet connection for loading MediaPipe CDN resources

### Recommended

* 4 GB RAM or more
* 720p webcam or better
* Modern processor
* Google Chrome or Microsoft Edge

---

# 📁 Project Structure

```text
air-canvas/
│
├── index.html
├── style.css
└── script.js
```

The project is intentionally lightweight and does not require a backend server or database.

---

# ⚙️ Installation

No package installation is required.

### Step 1 — Create the Project Folder

Create a folder named:

```text
air-canvas
```

### Step 2 — Create the Files

Inside the folder, create:

```text
index.html
style.css
script.js
```

### Step 3 — Add the Code

Add the corresponding HTML, CSS, and JavaScript code to the three files.

### Step 4 — Open in VS Code

Open the project folder using **Visual Studio Code**.

### Step 5 — Install Live Server

Install the **Live Server** extension in VS Code.

---

# ▶️ How to Run

Open `index.html` using **Live Server**.

The application will open at a local address similar to:

```text
http://127.0.0.1:5500/index.html
```

or:

```text
http://localhost:5500/
```

### ⚠️ Important

Do not simply double-click `index.html`.

The browser needs a secure context to access the webcam.

Use:

```text
localhost
```

or:

```text
HTTPS
```

When the browser asks for camera permission, select:

### **Allow Camera Access**

---

# 🧠 How AirCanvas Works

AirCanvas uses computer vision to convert hand movement into digital drawing.

### 1. Webcam Input 📷

The webcam continuously captures video frames of the user.

### 2. Hand Detection 🖐️

MediaPipe Hands processes the video and detects the user's hand.

### 3. Landmark Detection

MediaPipe provides hand landmarks that represent important points on the hand.

### 4. Fingertip Tracking ☝️

The application specifically tracks the **index fingertip landmark**.

```text
Index Fingertip
      ↓
Landmark 8
```

### 5. Coordinate Conversion

The normalized fingertip coordinates are converted into coordinates corresponding to the drawing canvas.

### 6. Position Smoothing ✨

Small movements and camera noise can make the fingertip position jitter.

AirCanvas applies smoothing to make the drawing line more stable.

### 7. Gesture Detection

The application checks the position of the fingers to determine whether the user wants to draw, pause, or remain idle.

### 8. Canvas Drawing 🎨

When drawing is active, the fingertip movement is converted into a continuous line on the HTML Canvas.

---

# ☝️ Gesture Controls

| Gesture                  | Action        |
| ------------------------ | ------------- |
| ☝️ Index finger only     | Draw / Erase  |
| ✌️ Index + middle finger | Hover / Pause |
| ✊ Other gestures         | Idle          |

### Drawing

Raise only your **index finger** and move it through the air.

```text
        ☝️
        │
        │
        ▼
   Draw on Canvas
```

### Pause / Hover

Raise the index and middle fingers.

The application pauses drawing while still allowing the user to position their cursor.

### Idle

Other gestures keep the drawing inactive.

---

# 🛡️ Accidental Stroke Prevention

One important issue with webcam-based hand tracking is that the hand can temporarily disappear from the camera.

If the application immediately connected the old fingertip position to the new position, it could create an unwanted line across the canvas.

AirCanvas avoids this by detecting consecutive missed frames.

When the hand disappears for multiple frames, the previous fingertip position is reset.

This prevents unwanted strokes from appearing when tracking is lost.

---

# 🎨 Drawing Tools

## ✏️ Pen

The default drawing tool.

Use your index finger to create a continuous digital stroke.

---

## 🧽 Eraser

Switch to eraser mode to remove parts of the drawing.

---

## 🎨 Colors

AirCanvas provides a color palette allowing users to change the drawing color.

---

## 📏 Brush Size

The brush size can be adjusted according to the user's preference.

---

## ↩️ Undo

Undo the most recent drawing action.

---

## ↪️ Redo

Restore a previously undone drawing action.

---

## 🗑️ Clear

Remove the current drawing from the canvas.

---

## 💾 Save

Save the finished artwork as a PNG image.

---

# 🔄 Application Workflow

```text
┌──────────────────────┐
│       Webcam         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   MediaPipe Hands    │
│   Hand Detection     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│   Hand Landmarks     │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Index Fingertip      │
│     Tracking         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Gesture Recognition  │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Position Smoothing   │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│    HTML Canvas       │
│      Drawing         │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│ Edit / Save Artwork  │
└──────────────────────┘
```

---

# 🖥️ System Architecture

AirCanvas performs its processing directly in the browser.

```text
              ┌───────────────┐
              │    User       │
              │      ☝️       │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │    Webcam     │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ MediaPipe     │
              │ Hands         │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ JavaScript    │
              │ Processing    │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ HTML Canvas   │
              └───────┬───────┘
                      │
                      ▼
              ┌───────────────┐
              │ Digital Art   │
              🎨
              └───────────────┘
```

No external backend or database is required.

---

# 📸 Screenshots

## Main Interface

![AirCanvas Main Interface](screenshots/aircanvas-main.png)

*Main AirCanvas interface showing the webcam area, drawing canvas, fingertip cursor, status indicator, and toolbar.*

---

## Drawing Mode

![AirCanvas Drawing Mode](screenshots/drawing-mode.png)

*The user raises the index finger and moves it through the air to create a digital brush stroke.*

---

## Tools and Color Palette

![AirCanvas Tools](screenshots/tools-palette.png)

*Drawing toolbar containing pen, eraser, colors, brush size, undo, redo, clear, and save controls.*

> **Note:** Replace the placeholder screenshot paths with your actual screenshots before submitting the README.

---

# 📷 Hardware Setup

AirCanvas does not require an electronic circuit.

The system uses the computer's webcam as the only physical input device.

```text
       ☝️ User Hand
             │
             ▼
      ┌─────────────┐
      │   Webcam    │
      └──────┬──────┘
             │
             ▼
      ┌─────────────┐
      │   Laptop    │
      │             │
      │ MediaPipe   │
      │ JavaScript  │
      │ Canvas      │
      └─────────────┘
```

---

# 🏗️ Build Photos

## Components

![Components](photos/components.jpg)

*Laptop/desktop, webcam, and development environment used for AirCanvas.*

---

## Development

![Build Process](photos/build-process.jpg)

*Development and testing of the AirCanvas interface and hand-tracking system.*

---

## Final Product

![Final Product](photos/final-product.jpg)

*Final AirCanvas application running with real-time hand tracking and air drawing.*

> Replace these placeholder image paths with the actual project photos.

---

# 🎥 Project Demo

### Demo Video

**AirCanvas demonstration video:**
Google Drive demo video

The demonstration showcases:

* Webcam hand detection
* Index fingertip tracking
* Touch-free drawing
* Pen mode
* Eraser mode
* Color selection
* Brush-size adjustment
* Undo and redo
* Canvas clearing
* Saving the final drawing

---

# 🔗 Additional Demos

* **Live Application:** Add your live demo link
* **GitHub Repository:** Add your repository link
* **Project Presentation:** Add your presentation link

---

# 👥 Team Contributions

## Muhammed Luqman — Team Lead

* Designed the overall AirCanvas concept
* Planned the project architecture
* Developed the main application
* Integrated MediaPipe Hands
* Implemented webcam input
* Implemented fingertip tracking
* Implemented gesture recognition
* Implemented position smoothing
* Coordinated development and testing

---

## Ayman Rasheed

* Designed the user interface
* Developed the drawing toolbar
* Implemented the color palette
* Worked on pen and eraser functionality
* Implemented brush-size controls
* Implemented undo and redo
* Implemented clear and save functionality
* Assisted with testing and debugging

---

## [Member 3]

* [Add contribution]
* [Add contribution]
* [Add contribution]

---

# 💡 Why AirCanvas?

AirCanvas demonstrates how **computer vision and modern web technologies** can be combined to create a touch-free human-computer interaction system.

Traditional:

```text
🖱️ Mouse
📱 Touchscreen
✏️ Stylus
🎨 Graphics Tablet
```

AirCanvas:

```text
☝️ Finger
   +
📷 Webcam
   +
🤖 Computer Vision
   =
🎨 Digital Drawing
```

The project turns an ordinary webcam into an interactive drawing interface.

---

# 🌟 What We Learned

Through the development of AirCanvas, we explored:

* Real-time computer vision
* Hand landmark detection
* Gesture recognition
* Webcam integration
* Coordinate mapping
* Canvas-based graphics
* Motion smoothing
* Browser APIs
* User interface design
* Real-time interaction
* Debugging webcam-based applications

---

# 🚀 Future Improvements

AirCanvas can be extended with several advanced features.

### 🤚 Advanced Hand Interaction

* Multi-hand support
* More complex gestures
* Custom gesture controls
* Gesture-based tool selection

### 🎨 Advanced Drawing

* Shape recognition
* Different brush styles
* Gradient brushes
* Neon/glow brushes
* Line and geometric shape tools

### 🔤 Smart Features

* Air handwriting recognition
* Handwriting-to-text conversion
* AI-assisted drawing
* Automatic shape correction

### 📱 Platform Support

* Mobile camera support
* Tablet support
* Better cross-browser compatibility

### 👥 Collaboration

* Real-time collaborative drawing
* Multiple users drawing on the same canvas
* Online artwork sharing

### 🖼️ Export

* JPG export
* SVG export
* PDF export
* Artwork history

---

# 🏆 Hackathon Value

AirCanvas is a simple project with a strong demonstration factor.

It combines:

```text
Computer Vision
       +
Web Development
       +
Human-Computer Interaction
       +
Real-Time Processing
       +
Creative User Experience
```

into a single browser-based application.

The project requires minimal hardware while demonstrating a practical application of **hand tracking and computer vision**.

---

# 🔐 Privacy & Architecture

AirCanvas does not require:

* ❌ Backend server
* ❌ Database
* ❌ User account
* ❌ Cloud storage
* ❌ Complex installation

The application processes the webcam input directly in the browser using the project's JavaScript and MediaPipe integration.

---

# 📝 Conclusion

**AirCanvas** transforms a normal webcam into a touch-free digital drawing interface.

By combining:

**MediaPipe Hands + JavaScript + Webcam + HTML Canvas**

the project allows users to draw digitally using only their finger movements.

Although AirCanvas started as a fun and unnecessary idea, it demonstrates important concepts in **computer vision, gesture recognition, real-time interaction, and web development**.

> **No mouse. No stylus. No touchscreen.**
>
> **Just your finger and the air. ☝️🎨**

---

# ❤️ Made With

Made with ❤️ by **Team hazardianzz**

### TinkerHub Useless Projects

![TinkerHub](https://img.shields.io/badge/TinkerHub-24?color=%23000000\&link=https%3A%2F%2Fwww.tinkerhub.org%2F)

![Useless Projects](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)

---

## 🎯 AirCanvas

### **Draw in the Air — Your Finger Is the Brush.**



---
Made with ❤️ at TinkerHub Useless Projects 

![Static Badge](https://img.shields.io/badge/TinkerHub-24?color=%23000000&link=https%3A%2F%2Fwww.tinkerhub.org%2F)
![Static Badge](https://img.shields.io/badge/UselessProjects--26-26?link=https%3A%2F%2Ftinkerhub.org%2Fevents%2F1M8ORET9A1%2Fuseless-projects-3.0)



