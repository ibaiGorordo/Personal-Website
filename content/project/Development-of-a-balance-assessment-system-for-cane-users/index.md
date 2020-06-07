---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Development of a Balance Assessment System for Cane Users"
summary: ""
authors: []
tags: ["balance analysis", "millimeter wave radar", "base of support", "assistive devices", "cane","inertial sensor","deep learning", "edge computing", "object detection", "inertial sensor"]
categories: []
date: 2020-06-07T18:13:13+09:00

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
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

It is estimated that around 30% of the elderly fall each year worldwide. The use of assistive devices such as canes or walkers increases the stability of the elderly by increasing the area of the Base of Support (BoS). However, the fall rate of assistive device users is similar or even higher than of non-device users. Moreover, balance has been found to be a stronger indicator for the estimation of the fall risk in the elderly.

The main objective of this research is the development of a real time balance assessment system for cane users. The system would measure the balance in real time in order to provide an indicator of the risk of fall of the user. For that purpuse, in our research we use attached various sensors to single tip cane in order to estimate the balance at each moment. In our research, balance is estimated by measuring the position of the Center of Gravity (CoG) inside the BoS. 

The BoS is estimated using a millimeter wave radar sensor attached to the cane that measures the 3D position of the feet with respect to the position of the tip of the cane. Also, since the radar is moving as the cane moves, it is necessary to know the movement of the cane, both the orientation and the displacement. For thar purpose, we use an inertial sensor attached to the cane in order to estimate both the gait phase, 3D orientation and 3D kinematics.

Moreover, due to the reduced resolution of radar sensors, in some cases it is hard to verify if the radar is correctly tracking the position of the feet or if it is tracking the position of other objects near the feet. For that reason, we trained a Deep Learning object detection model in order to detect the position of the feet inside a video frame. This object detection is combined with the 3D point cloud of reflected points from the radar in order to generate a more robust estimation of the position of the feet.
