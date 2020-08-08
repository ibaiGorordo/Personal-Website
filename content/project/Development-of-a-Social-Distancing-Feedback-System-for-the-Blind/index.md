---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Development of a Social Distancing Feedback System for the Blind"
subtitle: "Project for the OpenCV Spatial AI Competition"
summary: ""
authors: []
tags: ["deep learning","edge computing","assistive devices","object detection","visually impaired","depth estimation"]
categories: []

links:
- name: Project's GitHub Repository
  url: https://github.com/ibaiGorordo/Social-Distance-Feedback



date: 2020-08-08T22:24:20+09:00

weight: 1

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "smart"
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
Due to current worldwide outbreak of COVID-19, social distancing has become a new social norm as a measure to prevent the widespread of the pandemic.

However, visually impaired people are struggling to keep independence in the new socially distanced normal¹,². For blind people, it is not possible to easily confirm if they are keeping the social distance with the people around them. 

Moreover, common solutions for the blind such as white cane or dog cannot assist the blind to keep the social distance. Even worse, blind people cannot know if the people close to them is wearing a mask or not, thus they suffer a higher risk of infection.

For those reasons, the objective of my project is to develop a feedback system for the blind that informs about the distance to other people around and whether someone is not wearing a mask.

For that type of project, where the depth and Artificial Intelligence needs to be combined in real time, the OAK-D is the ideal system. As shown in one example of the DepthAI experiments, the OAK-D is able to detect in real time the position of the faces in an image and whether they are wearing a mask or not. By combining this information with the depth information obtained from the stereo cameras, it is possible to estimate the position of the people around the user and if someone is not wearing a mask.

Then, the system will inform the user about the distance to the people around using five haptic motors attached to the OAK-D board. The haptic motors will be related to 5 direction angles: -40, -20, 0, 20 and 40 degrees. For example, if the system detects that there is a person near at an angle of -20 degrees (as in the image above), then the second motor from the left will vibrate. Moreover, in order to inform about how close the person is, the intensity of the motor will change as the detected person gets closers. Finally, if the system detect that there is a person not wearing a mask, the system will inform the user by changing the vibration pattern.

## References
[1] Gus Alexiou. (June 7 2020). Blind People’s Social Distancing Nightmare To Intensify As Lockdowns Ease, https://medium.com/@arinbasu/you-can-use-footnotes-thus-babus%C2%B9-6c485c4eff1e

[2] BBC news. (June 24 2020). Social distancing a ‘struggle’ for those visually impaired, https://medium.com/@arinbasu/you-can-use-footnotes-thus-babus%C2%B9-6c485c4eff1e