--- 
layout: post
title: "Declaring Espresso ☕🦊"
date: 2025-09-15 08:00:00 +0200
categories: [cicd, gitops, yaml]
tags: [gitlab]

---

## We brewed our first GitLab pipeline, but let's be honest: a process isn't real until you can taste the result.
Today's the day. We're moving from theory to flavor - declaring artifacts, splitting stages, and sipping the pipeline output like a proper espresso.

---

### Step 1: Name It or It's Not Real 📝
 In GitLab, a job without artifacts is like coffee without a cup - where's the proof?
 That's where this bit comes in:

```yaml
artifacts:
  paths:
    - brew
```

Think of it like a container holding your finished espresso shot. Without it, your job runs and vanishes, leaving you with… nothing.

---

### Step 2: Stages Make It Flow ⏩
 Coffee isn't one big blur. You brew, then you taste. Pipelines deserve the same rhythm.

```yaml
stages:
  - brew
  - taste
```

Each stage builds on the last, like steps in a ritual. Structured, simple, and much easier to debug when something burns.

---

### Step 3: Sprinkle Some Variables 🌱
 Variables are your recipe notes. They can be global (shared kitchen wisdom) or local (secret barista tricks).

```yaml
variables:
  GLOBAL_FILE_NAME: espresso.txt
```

In this context, the variable doesn't add much flavor - but it's worth appreciating the concept: reuse, consistency, and flexibility baked right into your pipeline.

---

### Step 4: Taste the Output 👅
 Now comes the real test. Did our brew job leave behind all the right notes? Let's check:

```yaml
taste_coffee:
  image: alpine
  stage: taste
  script:
    - test -f brew/$GLOBAL_FILE_NAME

    - grep "Prepare water" brew/$GLOBAL_FILE_NAME
    - grep "Add coffee grounds" brew/$GLOBAL_FILE_NAME
    - grep "Assemble the pot" brew/$GLOBAL_FILE_NAME
    - grep "Heat" brew/$GLOBAL_FILE_NAME
    - grep "Brewing (extraction phase)" brew/$GLOBAL_FILE_NAME
    - grep "Finish brewing" brew/$GLOBAL_FILE_NAME
    - grep "Serve" brew/$GLOBAL_FILE_NAME
    - grep "Clean" brew/$GLOBAL_FILE_NAME
```

Every grep is a sip-checking if the steps are truly there. When they all pass, the pipeline turns green. Espresso approved.

---

### Step 5: Structured Flavor 🏗️☕
Here's the takeaway:
- Declare artifacts = keep your cup full ✅
- Use stages = sip in order ✅
- Add variables = future-proof your recipe ✅


The final taste? A well-structured pipeline that doesn't just run - it flows.
 Green lights, clean logs, and yes… espresso you can trust. 🦊☕