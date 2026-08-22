+++
title = 'Hardware & Modeling for Rocket Launches'
date = 2026-01-15T00:00:00+09:00
draft = false
tags = ['Hardware', 'Modeling', 'Personal Project']
summary = "An ongoing hardware and modeling project exploring amateur rocket launches, from mechanical design to flight instrumentation."
status = 'Very Active'

[cover]
  image = "rocket-project-collage.png"
  alt = "Mosaic of renders, thrust curves and blueprint graphs from the rocket launch project's dev logs"
  hiddenInSingle = true
+++

An active personal project (started 2026) combining hardware design and physical modeling to build and launch model rockets.

The work spans mechanical design of the airframe and recovery system, modeling of flight dynamics to predict trajectory and apogee, and embedded instrumentation to log flight data (altitude, acceleration, orientation) during launches. I'm currently simulating the rocket's flight environment in Unreal Engine.

On the hardware side, I picked up:
- A [NUCLEO-64 STM32WBA65RI eval board](https://www.digikey.jp/en/products/detail/stmicroelectronics/NUCLEO-WBA65RI/26257430) as the flight controller.
- An [ICM20948](https://www.digikey.jp/en/products/detail/pimoroni-ltd/PIM448/10246391) IMU for acceleration/orientation sensing.

It's a hands-on way to keep my electronics and embedded skills sharp outside of work, closing the loop from schematic to flight data.

See [Rocket Project: Solid Engine Simulation](/projects/rocket-launch-project/rocket-solid-engine-simulation/) for a closer look at how the motor's thrust profile is modeled and driven in Unreal Engine, [Rocket Project: Mounting the Engine and Making Its Direction Controllable](/projects/rocket-launch-project/rocket-engine-gimbal/) for the gimbal that steers thrust direction, [Rocket Project: Physics-Driven Engine Mass and a Constraint-Based Gimbal](/projects/rocket-launch-project/rocket-engine-mass-and-physics-gimbal/) for how the gimbal moved to a Physics Constraint so the engine's mass can drop as it burns, and [Rocket Project: A Rotule-and-Slider Mechanism for the Landing Legs](/projects/rocket-launch-project/rocket-landing-leg-deployment/) for the constraint prototyped to deploy the landing legs.

**Source:** [github.com/Potoman/RocketSimulation](https://github.com/Potoman/RocketSimulation)

*Status: active, ongoing.*
