---
title: "Hello HoloLens"
date: "2017-04-11T21:31:00+02:00"
tags: ["hololens","holotoolkit"]
draft: false
---

In this post, I'm recreating my steps taken to implement a non-trivial HoloLens application. The goal is to create some sort of parking lot visualisation, so therefore I will name my objects accordingly (and not `Cube` and `GameObject`, like you see in other tutorials). I also want to explore the possibilities of the HoloToolkit, so therefore we start with installing it into a new Unity-project.

Install the HoloToolkit as explained in its Getting [Started document](https://github.com/Microsoft/HoloToolkit-Unity/blob/master/GettingStarted.md). Personally I prefer to download a release version.

Some remarks regarding importing:

- you don't have to include everything. Only the scripts that you plan to use should be included. Of course, if you are starting to learn, you don't know what you'll need, so just include it all. I typically leave everything in except for the examples
- If the import went well, you should see an extra `HoloToolkit`-menu in the Unity editor
- the guide tells you to create a new scene, but saving and renaming the existing _(untitled)_ scene is enough

While setting up the scene, I did the following:

- remove everything from the scene
- add the `HoloLensCamera`
- don't add any cursors yet (we're only experimenting with gaze)
- don't add the `InputManager`, `EventSystem` or `Managers-GameObject`
- don't add spacial mapping
- create an empty `GameObject` called _CarPark_ and add two cubes. Name them _lot1_ and _lot2_. Like I said: I'm thinking about a case of visualising a parking lot, so therefore I've come up with some meaningfull names instead of cube1 and cube2
- Place the cubes in front of the camera

Apply settings using the HoloToolkit-menu:

![Apply Settings](/blog/hello-hololens/sshot-3.png)

- HoloToolkit > Apply HoloLens Scene Settings > check everything and apply
- HoloToolkit > Apply HoloLens Project Settings > check everything and apply (You will need to reload the project)

Build your project:

- HoloToolkit > Build Window > Open SLN and click "Yes, Build"

Now, tweak your build settings. File > Build settings

![Build settings](/blog/hello-hololens/sshot-4.png)

Hit Build and select App. If this folder doesn't exist, create it first.

Go into the App folder and double click the solution file. Now you can either run your app on the emulator or on a real device. You should see your two cubes. Make sure to select x86 as the processor architecture.

![Build settings](/blog/hello-hololens/sshot-5.png)

In a next post, we will add some gazing features.



