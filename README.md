# Unreal Engine Nanite Tutorial Project

- I wanted to try out a new tutorial not covered in class so I went to youtube and found this video -> https://www.youtube.com/watch?v=MXkWzg6hVys (Nanite Full Tutorial | Unreal Engine 5)

- The goal for me and this project is to learn quixel bridge importer and download some static meshes and build out a small world that all renders in Nanite from scratch, without using templates.

# IMPORTANT
- I was not able to include project files for this since every asset was so large that I could not get it to upload to git successfully. I have instead included a bunch of screenshots from the engine and a description of everything I did.

## Assets used in the store so you could try this
- Quixel bridge - any of the Nanite rocks/cliffs will work
- Stylized Forest (fab.com)
- MW LandScape Auto Material (fab.com)

## Process
- I started with UE 5.4.4 and created an empty world project that already has a sky and landscape.
- I then went to UE fab and downloaded some sample assets to add to the project from quixel that can help me build a landscape.
- Imported Third Person player pawn so I could move around my world.
- Imported a free sample from fab of a mountain range so I could visualize nanite triangles coming in and out of view at different ranges. I have added some screenshots of this in this projects Screenshots folder.
- I could now look at various meshes in the static mesh editor and  modify some properties of them to mess with the nanite rendering system.

- Next, I imported some trees to add to the complexity of the nanite scene.
- All of these assets I found are available for free on Fab.
**Note:** I realized that the trees did not support Nanite right away, so I had to edit the static mesh to add nanite support to one of the tree types. See the screenshot called: treenanite, to see some trees with this feature on and some as a default static mesh with no nanite support.

- I then took a few screenshots to view the trees close up in the editor to show just how many triangles are being rendered when near a tree.
- I also took some from far so you can compare side by side the close up version and what Nanite does to reduce triangle counts from far away.

- As part of this tutorial, I also took a look at the nanite "Overdraw" visualization mode to show where these models have potential errors. See the screenshot naniteOVERDRAW to see how the trees are overdrawn when using nanite and not optiomized, this is shown by the bright hotspots on the trees. This tells you that the engine has a hard time deciding which leaf on the trees to render at any given time, and will take a lot more processing power.

## Quixel Bridge
- The next thing I wanted to accomplish was to download some of the quixel megascans that are photorealistic assets provided for free. CLAIM THESE NOW SINCE THEY WONT BE ACCESSIBLE AFTER DECEMBER 31st.
- I created the account and got logged in within the quixel bridge plugin, and was able to download the nanite ready asset for a large cliff. See screenshots x2. I added them to my level and they worked right away.
- WOW these cliffs have an insane amount of triangles. Look at the screenshot to see how many these have as compared to the trees.

## Conclusion
- At this point, I felt I understood the nanite system enough to get started and take it a step further, so at this point I enabled nanite for everything in the scene and pushed my computer to draw millions of triangles by duplicating my trees all over the world. Without Nanite this would not be possible since it would be too many triangles to draw at any given time. See the screenshot, nanite_MANYTREES
- I then took one in the overview mode, which shows how triangles are formed into nanite instances, then further refined into clusters, and then finally produced as individual triangles. This is the coolest one, check it out. nanite_manytrees_overview

- As a bonus, I checked out Lumen, the advanced real time lighting feature, and have a cool screenshot that shows it in action. lumen_test
- I accomplished learning some of the nanite tools, and also importing quixel bridge assets into my level. I also got more familiar with the ability to quickly duplicate content in my world to start building real levels.

- 
