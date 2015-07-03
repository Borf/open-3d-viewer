Contact [the mailing list](http://groups.google.com/group/open-3d-viewer-discuss) to discuss these ideas with project organizers.

**0. Android version**
Done, see the android subfolder, especially the BUILDING.txt file.

**1. iOS version**
Particularly iPad. See IpadPortNotes.

**2. Info sidebar**
When an item is selected, show information in a sidebar. (E.g., in the human anatomy case, show article excerpts from Wikipedia.)

**3. Localization**
It should be possible to provide content labeled in multiple languages. There is a small hook built in for this now, in that display names for the sample metadata are currently marked "-en-us" and the viewer is hardcoded to look for this suffix. See also **metadata management**.

**4. Fully detailed history**
Camera position is stored in the URL after the # (try navigating and waiting a moment for it to update). This viewer should also store the layer opacity state, which parts are selected/pinned/hidden, and so on.

**5. Cartographic labeling**
Provide a mode where many (or all) of the model parts visible at any one time are labeled as if they were places on a map: more important things are larger, labels don't overlap, the overall aesthetics of the model are preserved, and so on.

**6. Widget version**
There should be a version of this viewer that, like the Google Maps widget, can be added to any Web site with minimal coding.

**7. Metadata management**
Model metadata (which parts are in which layers, which parts are in which groups, alternate names for parts and groups, which parts represent left/right of something, etc.) is currently created by writing simple text files and running them through Python scripts to produce JSON output. There should be some mildly more sophisticated tool for editing this metadata.

**8. Cross-section viewing**
Allow the ability to "slice" the model and view a labeled version of the cross-section.

**9. Fantastic Voyage mode**
Allow the ability to fly around inside the model, with collisions automatically prevented (if you run into the wall of a structure, you bounce off instead of going through).

**10. Animation**
Allow a model's articulation constraints to be specified; then allow the model to be arbitrarily moved within those constraints, in real time.