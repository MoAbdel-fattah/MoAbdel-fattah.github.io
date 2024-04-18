---
layout: post
title: Basic widgets
date: 2024-4-18 00:00 +0000
categories: [Flutter,Basics]
tags: [flutter]
---

Flutter provides a collection of pre-built widgets that you can use to construct your app's interface. These widgets are like building blocks that you can put together to create anything you can imagine.

Here's a breakdown of the different types of widgets and how they work together:

# Basic Widgets:

- Text: 
 - This widget lets you add text to your app, and you can style it with fonts, colors, and other properties.

- Row & Column: 
 - These widgets help you arrange other widgets horizontally (Row) or vertically (Column). They are based on the web's flexbox layout model.

- Stack: 
 - This widget lets you layer widgets on top of each other. You can position the widgets using the Positioned widget. Stacks are based on the web's absolute positioning layout model.

- Container: 
 - This widget creates a rectangular box that can hold other widgets. You can customize it with a background, borders, padding, and more.

# Material Design Widgets:

Flutter includes a set of widgets that follow Material Design guidelines. These widgets provide a consistent look and feel for your app.

- MaterialApp: 
 - This widget is the foundation for most Material Design apps. It sets up things like the navigation and theme.

- AppBar: 
 - This widget creates a bar at the top of the screen, typically used for displaying the app's title and navigation buttons.

- Scaffold: 
 - This widget is the basic layout structure for Material Design apps. It provides areas for the app bar, body content, and a floating action button.

# Handling User Interaction:

- GestureDetector: 
 - This widget detects gestures like taps, drags, and swipes. You can use it to respond to user input in your app.

- StatefulWidgets: 
 - These widgets are used to manage state in your app. State is data that can change over time, such as the value of a form field or the items in a shopping cart.

# Putting it all Together:

The provided example showcases how to create a shopping list app using different widgets. It demonstrates how stateless widgets are used for presentation and stateful widgets are used to manage changing data.

### Key Points:

- Widgets are the building blocks of Flutter apps.
- There are different types of widgets for different purposes (basic layout, Material Design, handling user interaction, etc.).
- Stateful widgets are used to manage state in your app.
- Keys are used to help the framework efficiently update the UI when widgets change.