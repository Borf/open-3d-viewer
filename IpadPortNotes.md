_reddkamel@gmail.com writes:_

Rich, here's an overview of what the WebGL version is capable of.

1. Core capabilities:
  * Load the geometry data (proprietary format) and image textures using the provided models.js file and models/cow\_anatomy directory.
  * From that same directory, load the JSON metadata that is used for layering, grouping, and searching.
  * Display and navigate around the model with basic swipe (up/down/rotate-left/rotate-right) and pinch (zoom) gestures.
  * Hide/show each layer individually.
  * Switch between two models, again using the models.js file and models/ directory structure.

2. Rounding out a usable viewer:
  * Ability to tap an individual item and see what it is, via a label.
  * Full independent opacity control (0.0 to 1.0) of each layer, controlled by a UI comparable to the WebGL version.
  * Ability to search for an individual item by name and have it highlighted, with autocomplete search.
  * Highlighting rules that mirror the WebGL version (i.e., search for or select something and see a ghost version of the rest of the model).

3. Full feature parity with WebGL version:
  * Ability to search for groups of entities as well as individual ones.
  * Smoothed motions and transparency changes.
  * The ability to "pin" a selected item so it stays visible no matter what other opacity changes may happen.
  * The ability to hide any item.
  * "Capsule" navigation of the entire model, meaning that if you go up or down far enough, the camera starts moving as if it were a hemisphere over the top or bottom of the model, thus (in the Body case) allowing you to look down on the top of the head.
  * "Capsule" navigation around whatever item or items are currently selected.

If you're interested, my suggestion would be to work on getting the core capabilities implemented and checked in. (We can get you or others a second data set to ensure that switching between models works.) After that I guess it's a question of how much time you have to commit and whether others want to help.

Which approach to use for porting is an interesting question.
  * The developer of the Android version of Google Body is on this thread; he analyzed the state of the v1 codebase (which differs from open-3d-viewer primarily in the complexity of the metadata model) and ported it to Java wholesale. You could do the same, or you might investigate running some of the open-3d-viewer Javascript code in a wrapped webview -- this might make it faster to get the metadata model up and running, since it's pretty self-contained.
  * You might also look at the Android source itself as checked in, as a model for the ObjC version. My understanding is that it's not quite buildable, but the gap to making it work is not large.
  * If you have time to embark on this, we can probably get Body team members to provide more detailed notes on the JS/Java source files.