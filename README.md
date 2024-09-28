
<div align="center"> <br /> <a href="https://youtu.be/ZBCUegTZF7M?si=ubt0vk70lSjt6DCs" target="_blank"> <img src="https://i.postimg.cc/5NR9bxFM/Sora-README.png" alt="Project Banner"> </a> <br /> <div> <img src="https://img.shields.io/badge/-React_Native-black?style=for-the-badge&logoColor=white&logo=react&color=61DAFB" alt="react.js" /> <img src="https://img.shields.io/badge/-Appwrite-black?style=for-the-badge&logoColor=white&logo=appwrite&color=FD366E" alt="appwrite" /> <img src="https://img.shields.io/badge/NativeWind-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="nativewind" /> </div> <h3 align="center">Video Sharing App by Ogbuigbo</h3> <div align="center"> This project is a video sharing app showcasing seamless user experiences and impressive design. </div> </div>

 <a name="table">Table of Contents</a>

 🤖 Introduction
⚙️ Tech Stack
🔋 Features
🤸 Quick Start
🕸️ Snippets
🔗 Links
🚀 More
<a name="introduction">🤖 Introduction</a>
Built with React Native for seamless user experiences, Animatable for captivating animations, and integrated with the dependable backend systems of Appwrite, this app showcases impressive design and functionality, enabling seamless sharing of AI videos within the community.

If you're getting started and need assistance or face any bugs, feel free to reach out!

<a name="tech-stack">⚙️ Tech Stack</a>
React Native
Expo
Nativewind
Animatable
Appwrite
<a name="features">🔋 Features</a>
👉 Onboarding Screen: Engaging graphics and clear instructions welcome users to the app.

👉 Robust Authentication & Authorization System: Secure email login safeguards user accounts.

👉 Dynamic Home Screen with Animated Flat List: Smoothly animated flat list showcases the latest videos for seamless browsing.

👉 Pull-to-Refresh Functionality: Users can refresh content with a simple pull gesture for up-to-date information.

👉 Full-Text Search Capability: Efficiently search through videos with real-time suggestions and instant results.

👉 Tab Navigation: Navigate between sections like Home, Search, and Profile with ease using tab navigation.

👉 Post Creation Screen for Uploading Media: Upload video and image posts directly from the app with integrated media selection.

👉 Profile Screen with Detailed Insights: View account details and activity, including uploaded videos and follower count, for a personalized experience.

👉 Responsiveness: Smooth performance and adaptability across various devices and screen sizes for a consistent user experience.

👉 Animations: Dynamic animations using the Animatable library to enhance user interaction and engagement throughout the app's UI.

and many more, including code architecture and reusability.

<a name="quick-start">🤸 Quick Start</a>
Follow these steps to set up the project locally on your machine.

Prerequisites

Make sure you have the following installed on your machine:

Git
Node.js
npm (Node Package Manager)
Cloning the Repository
git clone https://github.com/yourusername/video-sharing-app.git
cd video-sharing-app
Installation

Install the project dependencies using npm:
npm install

Expo Go

Download the Expo Go app onto your device, then use it to scan the QR code from Terminal and run.

<a name="snippets">🕸️ Snippets</a>
<details> <summary><code>tailwind.config.js</code></summary>\
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./app/**/*.{js,jsx,ts,tsx}", "./components/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {
      colors: {
        primary: "#161622",
        secondary: {
          DEFAULT: "#FF9C01",
          100: "#FF9001",
          200: "#FF8E01",
        },
        black: {
          DEFAULT: "#000",
          100: "#1E1E2D",
          200: "#232533",
        },
        gray: {
          100: "#CDCDE0",
        },
      },
      fontFamily: {
        pthin: ["Poppins-Thin", "sans-serif"],
        pextralight: ["Poppins-ExtraLight", "sans-serif"],
        plight: ["Poppins-Light", "sans-serif"],
        pregular: ["Poppins-Regular", "sans-serif"],
        pmedium: ["Poppins-Medium", "sans-serif"],
        psemibold: ["Poppins-SemiBold", "sans-serif"],
        pbold: ["Poppins-Bold", "sans-serif"],
        pextrabold: ["Poppins-ExtraBold", "sans-serif"],
        pblack: ["Poppins-Black", "sans-serif"],
      },
    },
  },
  plugins: [],
};

</details> <details> <summary><code>Font Loaded</code></summary>
const [fontsLoaded, error] = useFonts({
  "Poppins-Black": require("../assets/fonts/Poppins-Black.ttf"),
  "Poppins-Bold": require("../assets/fonts/Poppins-Bold.ttf"),
  "Poppins-ExtraBold": require("../assets/fonts/Poppins-ExtraBold.ttf"),
  "Poppins-ExtraLight": require("../assets/fonts/Poppins-ExtraLight.ttf"),
  "Poppins-Light": require("../assets/fonts/Poppins-Light.ttf"),
  "Poppins-Medium": require("../assets/fonts/Poppins-Medium.ttf"),
  "Poppins-Regular": require("../assets/fonts/Poppins-Regular.ttf"),
  "Poppins-SemiBold": require("../assets/fonts/Poppins-SemiBold.ttf"),
  "Poppins-Thin": require("../assets/fonts/Poppins-Thin.ttf"),
});

useEffect(() => {
  if (error) throw error;

  if (fontsLoaded) {
    SplashScreen.hideAsync();
  }
}, [fontsLoaded, error]);

if (!fontsLoaded && !error) {
  return null;
}

</details> <details> <summary><code>Dummy Videos for Appwrite</code></summary>
const videos = [
  {
    title: "Get inspired to code",
    thumbnail:
      "https://i.ibb.co/tJBcX20/Appwrite-video.png",
    video:
      "https://player.vimeo.com/video/949579770?h=897cd5e781",
    prompt:
      "Create a motivating AI driven video aimed at inspiring coding enthusiasts with simple language",
  },
  {
    title: "How AI Shapes Coding Future",
    thumbnail:
      "https://i.ibb.co/Xkgk7DY/Video.png",
    video:
      "https://player.vimeo.com/video/949581999?h=4672125b31",
    prompt: "Picture the future of coding with AI. Show AR VR",
  },
  // Add more videos as needed
];
