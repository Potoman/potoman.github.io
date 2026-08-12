+++
title = 'Improve Conan Install Step'
date = 2022-06-01T00:00:00+09:00
draft = false
tags = ['Conan', 'CMake', 'C++', 'Build Systems', 'Open Source']
summary = "Contributed a feature to Conan to automatically inject package information into the CMake install step."
+++

The goal was to make the CMake side of a Conan package smoother to use: automatically injecting package information (include paths, libraries, definitions, etc.) at the CMake install step, instead of requiring consumers to wire that up by hand.

**Stack:** Conan, CMake, C/C++
