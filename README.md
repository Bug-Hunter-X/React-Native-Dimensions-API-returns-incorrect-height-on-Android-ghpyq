# React Native Dimensions API Height Issue on Android

This repository demonstrates a common issue with the `Dimensions` API in React Native on Android.  The problem is that `Dimensions.get('window').height` can return inaccurate or 0 height values, particularly when the app initially launches or when the screen orientation changes. This can lead to layout issues and elements not being rendered correctly.

**Problem:** The `Dimensions` API doesn't always provide the correct screen dimensions immediately, causing layout problems. 

**Solution:** Use `Dimensions.addEventListener` to listen for changes and ensure you have the correct dimensions before rendering UI elements that depend on them.  Also, consider using `LayoutAnimation` for smooth transitions during changes.