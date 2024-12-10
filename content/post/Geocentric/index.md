---
title: Geocentric installation
summary: Brief summary of the key installation steps in Geocentric
date: 2024-12-10

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.

authors:
  - admin

tags:
  - Academic
---

{{< toc mobile_only=true is_open=true >}}

## Overview

1. Geocentric is a simulation platform built on the [deal.II](https://www.dealii.org/) finite-element library, [p4est](https://p4est.org/) mesh handling library, and the [Trilinos](https://trilinos.github.io/) project. It is not an open-source software, so this instruction is just written for myself ❤️.
2. Installation is not a very simple task, compared with the installation of commerical FEM softwares.
3. Fortunately, we have the [The deal.II/ASPECT virtual machine image](https://www.math.clemson.edu/~heister/dealvm/), which implies we do not need to install deal.II or its dependencies manually 👋.


### Procedure

- [ ] Download <mark>dealvm_1.21.ova</mark> from the above website.
- [ ] Download the [Oracle VirtualBox](https://www.virtualbox.org/) and install it.
- [ ] Import the <mark>dealvm_1.21.ova</mark> into the VirtualBox by following the basic instructions (default setting should be enough).
- [ ] Open the virtual Ubuntu system and download the <mark>Geocentric.zip</mark> from the Email attachment.
- [ ] Unzip the <mark>Geocentric.zip</mark> file and move the folder to the Desktop.
- [ ] Install [Eigen](https://eigen.tuxfamily.org/index.php?title=Main_Page) library by downloading the <mark>eigen-3.4.0.tar.gz</mark> file.
- [ ] Unzip the file using the following command and you will get a folder named **eigen-3.4.0**.
- [ ] Rename the folder name to **eigen3** and move it to the following directory.

      ```
      tar -xzvf eigen-3.4.0.tar.gz
      mv eigen-3.4.0 eigen3
      mv eigen3 /home/ubuntu/deal.II/installed/include/
      ```

- [ ] Run the simple test file

      ```
      cd /home/ubuntu/Desktop/Geocentric/solvers/AMCC-ANDPM-new
      sh build.sh
      ./solver 2 parameters/input_e2_debug_couldrun.prm
      ```
      
- [x] Congratulations! You are done with the installation!