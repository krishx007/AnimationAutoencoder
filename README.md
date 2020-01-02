# Animation Autoencoder
Procedurally generate or interpolate between animations for a bipedal humanoid using a multi-pose autoencoder. TFlite is used within Unity to create animations in real time. The autoencoder is trained on animations from 3D content sites (e.g. https://www.mixamo.com/) and data recorded from a curated list of videos after running a pose estimation algorithm

## Dependencies
- Python 3+
- Unity 3D
- Blender 2.7+

## Generate training data
- download a few animations from https://www.mixamo.com/ 
- put files in a directory and run the Blender script to extract 3D joint positions

## Create animations from videos
https://www.tensorflow.org/lite/models/pose_estimation/overview

17 point position to Unity/Blender compliant rigged character format

![](https://thumbs.gfycat.com/TinyScornfulImperatorangel-mobile.mp4)

## Procedural Animations
17 joint positions with an x,y,z coordinate amounts to 51 model inputs. The inputs are encoded in a fully connected deep neural network into a latent space of 3 dimensions

![](https://miro.medium.com/max/1968/1*44eDEuZBEsmG_TCAKRI3Kw@2x.png)
