---
title: 'Adaptive PID Control for Setpoint Tracking Using Reinforcement Learning: A Case Study for Blood-Glucose Control'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - "anna*"
  - "Golnaz Mesbahi*" 
  - Martha White

author_notes:
- "Equal contribution"
- "Equal contribution"
- ""

date: '2025-05-15T00:00:00Z'
doi: ''

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['Report']

# Publication name and optional abbreviated publication name.
publication: RLC 2025 Workshop on Practical Insights into Reinforcement Learning for Real Systems
publication_short: In *RLC'25 RL4RS Workshop*

abstract: Blood-glucose control is a classic example of setpoint tracking, where the controller must continuously adjust insulin delivery to maintain a desired glucose level. While simple feedback controllers, like proportional-integral-derivative (PID), are commonly used, they can not leverage contextual information that could lead to better performance. Reinforcement learning (RL) has shown promise for such control problems, but its use in continual setpoint tracking—where learning happens online during deployment—remains underexplored. In this work, we study how the on-policy RL algorithm PPO performs in blood-glucose control under different observability conditions. 
# We build a continuing blood-glucose control environment based on the Bergman model and evaluate PPO in a series of increasingly difficult scenarios - starting with a deterministic case, then introducing stochasticity, and finally testing how well learned policies transfer across different patients. Our results show that standard PPO struggles even in relatively simple settings, underscoring the need for further research to make RL more reliable for setpoint tracking. However, we find that modifying PPO’s policy to output PID gains—effectively using PPO to tune a PID controller—significantly improves stability and performance, demonstrating a promising direction for RL in process control.

tags: [Bloog-glucose control, PID tuning, Online reinforcement learning]

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: 'https://openreview.net/pdf?id=RzhCmF5oI0'
url_code: 'https://github.com/anna-ssi/bg-rlpid'


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: ''
  focal_point: ''
  preview_only: false

---