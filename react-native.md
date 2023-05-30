# React Native

## Getting Started with React Native

* Name three Core Components of React Native and describe what they do.
  * View 
    * The View component represents a container for other components and helps create the structure and layout of the user interface.
  * Text
    * The Text component displays text content in the app with basic styling and formatting options.
  * Image
    * The Image component displays images, supporting local and remote image loading and rendering.

* What problem does React Native solve (why call it native)?
  * React Native solves the problem of developing cross-platform mobile applications with a native-like performance and user experience. 
  * The term "native" in React Native refers to the fact that the framework allows developers to build apps using the same fundamental building blocks as native mobile apps written in languages like Swift for iOS and Java or Kotlin for Android.

* What are the building blocks of a React Native app? How does that compare to a React app?
  * The building blocks of a React Native app are components - reusable units that make up the mobile UI and handle user interactions. 
  * Compared to a React app, React Native components are specifically designed for mobile development and work with native UI elements, while React components are optimized for web development and rendering HTML.

### References

* <https://reactnative.dev/docs/getting-started>
* <https://reactnative.dev/docs/tutorial>
* <https://reactnative.dev/>

## Expo

* What solution does expo provide?
  * Expo provides a solution that simplifies the process of developing, building, deploying, and iterating on iOS, Android, and web apps from the same JavaScript/TypeScript codebase.

* Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the **managed** workflow.

* What is the difference between React Native and Expo?
  * React Native is a framework for building native apps using JavaScript and React, 
  * Expo is a set of tools and services built around React Native, aiming to simplify the development process. 
    * Expo includes a CLI, APIs, and a web-based GUI, making it easier to start a project, handle dependencies, and bundle your app.

### References

* <https://expo.dev/>

## Expo Snack

* Checkout this tool, what does snack allow you to do?
  * Expo Snack is an online tool that allows you to write and run complete React Native projects in your browser without needing to set up a development environment or even download anything. 
    * It's like a "code sandbox" for React Native. 
    * You can experiment with different Expo APIs, share your projects, and even open them directly on a phone or emulator.

### References

* <https://snack.expo.dev/>

## Eejecting

* What does “eject” mean within the context of Expo?
  * Ejecting refers to the process of transitioning your Expo-managed project to a bare React Native project. 
  * It provides more control over the native side of your application, allowing you to include custom native modules which are not supported by Expo.

* When should you not eject?
  * You should avoid ejecting from Expo if you are not familiar with native mobile app development or if your app's requirements can be met within Expo's capabilities. 
    * The managed workflow provided by Expo offers simplicity, ease of use, and several built-in features, making it suitable for many app development scenarios without the need to eject.

* Why might you choose to eject?
  * You might choose to eject from Expo if you need to incorporate custom native code, access specific native features that are not available in Expo, or integrate third-party libraries that rely on native code. 
    * Ejecting allows you to have more control over the native aspects of your app and extend its functionality beyond what Expo provides out-of-the-box.

### References

* <https://docs.expo.dev/archive/glossary/#eject?redirected>
