---
layout: post
title:  "What's the compute infrastructure that runs AI?"
date:   2026-06-19 17:10:00 +0530
categories: AI Infrastructure
---

I don't know. Yet. So, I want to explore a bit on infrastructure and software systems for machine learning and AI. I have been doing some reading and experiments. Based on that here is the rough map of things I want to do and the objectives.

Before GPT3.5 days, I had completed a course on [Natural Language Processing](https://coursera.org/share/b4dec70584a6e7c5d53f5a9fad203b43)
To refresh and catch-up I have started with Andrej Karpahty's Let's build GPT and Let's reproduce GPT-2 completion. 
I may do a couple of more in that learning thread, likely not around LLMs but Vision-Language-Action(VLA) models.
My intention is to just get a engineer's hang of coding such ideas to working programs. Learn frameworks like PyTorch along the way.
I do not want to delve too much on the research side of machine learning and artificial intelligence. Focus is on the software systems that run them.

Parallely or post the above activity, start with a mini-project to serve a LLM using vLLM. First try to run on my local desktop with NVidia GPU - RTX 3080. 
Learn how constrained hardware is. Do some optimizations and adjustments to run a model. 
Goal is to learn as much as possible around GPU execution, memory management, concurrency, compiler optimizations etc. Understand the stack till CUDA. Understand the interaction between OS kernel and application software and drivers. Map learnings from previous experience in executing applications and libraries in constrained hardware environment like smartcards, earlier versions of Android and edge devices. Understand benchmarking tools, profiling tools and debugging tools etc.
Post this probably will run inference on public cloud providers on whatever latest GPUs are available for rent. See how the optimization exercise looks on the cloud. Probably using TensorRT (!?)

Few questions I want to answer along the way:
* How is GPU computing parallellized? Learn about DeepSpeed, Megatron, FSDP frameworks.
* What is the memory pipeline look like, from storage to GPU memory, in training and inference. 
* What is the networking like at scale?
* How are concurrent user requests managed? How does scaling compare to traditional cloud computing?
* What's evolving fastest in this space, in tools and techniques?
* How are secrets handled around LLMs? What does the traditional software perimeter around ML models look like?

It has been a month or so of mucking around in this area. The above is the map I have prepared based on that. If you work in this space, feedback on my learning path is welcome. I want to find out if I am wrong, now!

I have a full-time job as principal engineer. So I haven't put a target on timelines. May take many months to a year.

Next write up is about my learning experience from [Let's Build GPT:from scratch, in code, spelled out](https://www.youtube.com/watch?v=kCc8FmEb1nY). Coding is already complete! [GPT](https://github.com/vinayak-g-bhat/gpt)


