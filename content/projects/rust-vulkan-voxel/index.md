+++
title = '3D Engine Based on Voxelization'
date = 2025-01-10T00:00:00+09:00
draft = false
tags = ['Rust', 'Vulkan', 'Graphics', 'Shader', 'Personal Project']
summary = "Out of pure curiosity about how voxel frameworks work under the hood, I decided to implement a small one myself, from scratch."

[cover]
  image = "ruxel-cover.png"
  alt = "Ruxel voxel renderer output"
  hiddenInSingle = true
+++

Out of pure curiosity about how voxel frameworks work under the hood, I decided to implement a small one myself, from scratch.

On top of that, this was also a chance to dig deeper into the Vulkan API. Rust is one of my preferred languages for its strong typing and safety guarantees, and Vulkan's explicit, low-level control made this a great way to deepen my understanding of GPU pipelines, memory management, and rendering — skills that connect directly to the GPU/shader work I do professionally (e.g. CUDA/OpenGL pipelines for medical video overlay). This small example is a good starting point for a future, more ambitious project.

**Stack:** Rust, Vulkan

**Source:** [github.com/Potoman/Ruxel](https://github.com/Potoman/Ruxel)
