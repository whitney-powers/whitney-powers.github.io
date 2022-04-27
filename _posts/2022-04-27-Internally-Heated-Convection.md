---
layout: post
title: Internally Heated Convection
#subtitle: Fundamental studies of the properties of internally heated convection
author: Whitney Powers
categories: convection
banner:
  video: /assets/images/website_movie.mp4
  loop: true
  volume: 0.0
  start_at: 0
  image: /assets/images/banners/home.jpeg
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: convection dedalus
sidebar: []
---

## Boundary Driven Convection

When constructing a convection simulation we must choose a method to drive convective motions. A conventional approach is to use a boundary driven (BD) method. For BD convection we drive convective motions with the boundary conditions of our simulation. We specify either the temperature or the heat flux at the top and bottom boundaries, and there are no heat sources or sinks in the interior of the domain. The type of motions a BD model produces are determined by the superadiabicity of our boundary conditions, or the degree to which the boundary conditions are more unstable than an adiabiatic stratification. Highly superadiabatic systems can produce high Mach number flows (of order unity) and can generate shocks. In these systems convection will mix the fluid so that the interior matches the adiabatic stratification, but the properties of convection are still dependent on superadibicity. Unfortunately the appropriate superadiabicity is difficult to determine for real systems as long as convection is efficient enough. Furthermore many real astrophysical systems do not drive convection through heating or cooling a boundary, but rather through radiatively heating or cooling an extended region of the system. Some systems, like a fully convective m-dwarf, do not have an inner boundary and thus we cannot use a boundary driven model.

## Internally Heated Convection

Internal heating is a more robust way of driving convection which can mimic heating from absorbtion, nuclear fusion, or any process where heat is deposited through a region rather than at fixed boundaries. In this system we initialize the simulation with an adiabiatic stratification and add a heat source term via the temperature equation. I am considering a constant internal heating term so that I can study the simplest possible system and determine how heating strenght affects the properties of a convective fluid. I am using the fully compressible equations implemented using the Dedalus pseudospectral framework. I hope to extend this work by considering internal cooling, and then through the implementation of a more realistic non-constant internal heating.


