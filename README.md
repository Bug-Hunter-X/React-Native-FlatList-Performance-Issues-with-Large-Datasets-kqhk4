# React Native FlatList Performance Issue

This repository demonstrates a common performance issue encountered when using `FlatList` in React Native with large datasets.  The issue is reproduced by rendering a significant number of items, causing noticeable lag, dropped frames, and ultimately potential crashes.

## Problem

`FlatList`'s default behavior renders all items at once. With large datasets, this leads to memory overload and poor performance. The example shows a basic `FlatList` rendering 1000 items.  On many devices, this will demonstrate performance problems. 

## Solution

The solution involves optimizing `FlatList` using techniques like:

* **`keyExtractor`:**  Providing a unique key for each item is essential for efficient rendering and updates.
* **`ItemSeparatorComponent`:** Improves performance and readability by separating items visually.
* **`removeClippedSubviews`:**  Removes items that are offscreen, drastically improving performance.
* **`windowSize`:** Controls the number of items rendered around the visible area, limiting memory usage.

The solution file shows how to implement these optimizations. 

## Setup

1. Clone this repository
2. Run `npm install`
3. Run `npx react-native run-android` or `npx react-native run-ios`