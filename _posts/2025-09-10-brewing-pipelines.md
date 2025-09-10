--- 
layout: post
title: "Brewing Pipelines ☕➡️🦊"
date: 2025-09-10 06:00:00 +0200
categories: [cicd, gitops, yaml]
tags: [gitlab]

--- 

## I made peace with GitLab and the transition went smoother than expected. Today? Time to take it up a notch: building my very first pipeline.i

And because DevOps is basically metaphors stacked on YAML, I'm pulling out my real-world ritual: making coffee. If I can trust GitLab to brew pipelines, why not trust it to brew espresso too?

---

### Step 1: Rename the Ritual ✍️
In the physical world, I wake up and reach for the moka pot. In the digital world, I wake up my .gitlab-ci.yml.
 First thing's first: rename the job to something that actually makes sense (no more mysterious "test-job-123"), and pick an image - Default is Ruby. Respect to Ruby, but… I'm making coffee, not Rails apps. 
Let's go with something lightweight and universal: alpine.
```yaml
brew_coffee:
  image: alpine
  script:
    - echo "brewing a cup of coffee"
    - mkdir brew
    - touch "brew/coffee.txt"
```

Framework ready. Fox approved.

---

### Step 2: Linux to the Rescue 🐧⚡
Why Linux? Because it's honest. No buttons, no drag-and-drop - just clean utilities that do what you tell them.

So instead of clicking a fancy GUI that pretends to make coffee, I'll spell out the steps with shell commands. Same principle as in my kitchen: heat, pressure, caffeine.

---

### Step 3: Wisdom from the Italians 🇮🇹☕
After digging through Italian coffee forums (deep research, highly technical), I found a tried-and-true moka pot process. 
Step by step, centuries of perfection!
GitLab, meet tradition.
Tradition, meet YAML.

---

### Step 4: Push and Pray 🚀🙏
Commit. Push. Watch the logs roll like boiling water.
This is where GitLab shines: detailed logs that show every single step. 
- No black box. 
- No guessing. 
Pure transparency - you can literally see your digital coffee bubbling up.

---

### Step 5: First Sip 🏁✨
Pipeline green. Logs clean. Coffee brewed (digitally, sadly).
But here's the bigger picture:
Linux makes it real ✅
GitLab makes it visible ✅
Abstractions become relatable ✅

Next stop? Maybe I'll automate breakfast. 🍳 
For now though… pipelines taste like espresso. 🦊☕