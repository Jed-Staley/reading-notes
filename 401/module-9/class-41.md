# Class 41 Reading Notes

## Introduction

This reading covers the fundamentals of React Native, the core components, the problems it solves, and the solutions provided by Expo. It also explains the concept of "ejecting" in the context of Expo and explores additional tools and resources.

## Notes

### Name three Core Components of React Native and describe what they do

1. **View**: The basic building block of UI in React Native, similar to a `div` in HTML. It is used to create layouts by nesting other components.
2. **Text**: A component for displaying text. It supports styling and nesting other Text components.
3. **Image**: A component for displaying images. It supports various image formats and allows for styling and resizing.

### What problem does React Native solve (why call it native)?

React Native solves the problem of building mobile applications that can run on both iOS and Android platforms using a single codebase. It is called "native" because it allows developers to write components that are compiled into native code, providing the performance and look-and-feel of native applications.

### What are the building blocks of a React Native app? How does that compare to a React app?

The building blocks of a React Native app are components, which are the same fundamental concept as in a React app. However, React Native uses its own set of core components (like `View`, `Text`, and `Image`) instead of HTML elements (like `div`, `span`, and `img`). These components are compiled to native code, whereas React components render to the DOM.

### What solution does Expo provide?

Expo provides a set of tools and services for building, deploying, and quickly iterating on React Native apps. It simplifies the development process by managing many of the complexities involved in building native apps.

### Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow

Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the **managed** workflow.

### What is the difference between React Native and Expo?

React Native is a framework for building native mobile apps using React, while Expo is a platform that builds on top of React Native to provide additional tools, services, and libraries. Expo simplifies the development process by offering managed workflows, whereas React Native requires more setup and configuration.

### What does snack allow you to do?

Expo Snack is an online tool that allows you to write, run, and share React Native code directly in the browser. It provides an interactive development environment without the need to install any software locally.

### What does “eject” mean within the context of Expo?

In the context of Expo, "eject" means to exit the managed workflow provided by Expo and gain full control over the native code of the application. This allows developers to add custom native modules and configurations that are not supported by Expo's managed workflow.

### When should you not eject?

You should not eject if you are satisfied with the features and capabilities provided by Expo's managed workflow and do not require any custom native code or configurations. Ejecting increases the complexity of the development process and maintenance.

### Why might you choose to eject?

You might choose to eject if you need to add custom native modules, use native APIs that are not supported by Expo, or if you require advanced configuration options that are not available in the managed workflow.

## Reflection

### What are your learning goals after reading and reviewing the class README?

My learning goals include understanding the core components of React Native, exploring the capabilities and benefits of Expo, and learning how to effectively manage the development and deployment of React Native applications. Additionally, I aim to gain practical experience with tools like Expo Snack and understand the implications of ejecting from the managed workflow.
