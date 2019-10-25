---
highlightTheme: "github"
---


# Static Analysis of Java with Moose

---

# Technologies
 |
-------------|---------------
![](images/git.png){class=plain}{style="height:100px;"} | ![](images/octocat.png){class=plain}{style="height:100px;"}
![](images/pharo.png){class="plain"}{style="height:100px;"} | ![](images/moose-icon.png){class="plain"}{style="height:100px;"}

---

<!-- .slide: data-background-image="images/pharo.png" data-background-position="90% 10%" data-background-repeat="no-repeat" data-background-size="40% auto" data-background-opacity="0.8" -->

# Pharo

- Language (inspired by Smalltalk)
- Platform (immersive programming)
  - Image-based platform (like VirtualBox)
- Moose is a set of tools running in Pharo

<img src="images/moose-icon.png" class="plain reveal stretch">

---

## Overview

<img src="https://www.plantuml.com/plantuml/svg/JO_13e9034Jl_OeUyHVmeZ6QI20XCH8l71eekhfioUv2ebzlGGxUEfatayukHF9nx2t0SW6a1okECQE9SF3ov2Pk8LraaD4tZ8sqN4DQaWyh5mLxUZ6UziNvXhtw5fEA_SJ6SRRHV74vOcVidCk5sfMH3l-APqn4EulPhA4J_uAqCc4aQpxyoq1IMdBnMkHQEnD8Tp9Ets6liaToPD_110KVv4KfTkrIfGjbW9rAtVi5" class="reveal stretch plain">

Example from my blog <br/>[Analyzing Java with Moose 8](https://fuhrmanator.github.io/2019/07/29/AnalyzingJavaWithMoose.html)

---

# Preliminaries

- [Install and run the Pharo Launcher](http://pharo.org/download).
- Copy `Moose-8` image from the Inria CI:
  **New Image Templates \> Official distributions \> Moose Suite 8.0 (development version) \> Create image**
- Launch the image once it has downloaded.

<img src="images/pharo-launcher.png" class="plain reveal stretch">

---

## Cloning a project from GitHub

<img src="https://www.plantuml.com/plantuml/svg/JP312i9034Jl-Og05_s5Ub54GR4WYCMBXzYckZRToEwse5zlMZruop1lXYIBc2YahXM0SGAOYBlTqrKwpbQYdd57FU4pw8FBDF-tHoDg5qh6KYk-G7QW47-9fDXImxXPvjipjkOBJWiEFJlFkzaSilounjh9aDihLJz6Q_mh7Z1Lwym7ymArXWQomiMEnBtvcu7fGSYdKxwtse50kf7pjWu7aosI9tb55msyKr2Zs5TZbLsjJrYOj1zy0000" class="reveal stretch plain">

--

## Cloning a project from GitHub

Clone with `MooseEasyUtility`

In a Moose Playground (<kbd>CTRL</kbd>+<kbd>O</kbd>+<kbd>W</kbd>):

```smalltalk
javaProjectFileRef := MooseEasyUtility cloneGitHubRepo:
    'https://github.com/bethrobson/Head-First-Design-Patterns'.
```

---

## Creating a Moose Model

<img src="https://www.plantuml.com/plantuml/svg/JP11Yy9038Nl-HM1lUXV62ykiWih3XHanKiFiKrrR3gHcMb1V_t6hWTlUUHxxv6iSw5Kna40vWd0RKGZuvOcmblIApTb1MwMMSVKC3RQSWqV4iwNSfAHNKKflnn5SQ2UyVlJ_nnnC59mSU0qSOYyNQxURNx_XLqGot8xfVP5QuTlPLRjLItTFvSrT9fwS8UGHvBmu7yFB2gXM7xzpWgU1DAPGWHNSJ8v84MIUmxPm0ibDOfZEqVPrNg3jKdxmHy0" class="reveal stretch plain">

---

## Loading model in Moose

<img src="https://www.plantuml.com/plantuml/svg/JP313W5138RlVOecBhp2k10X8IQH275ngDqkGtSgCxCIdbuj1xV-wVVtRpl9XLBfMW7eAm0t4usCAteGtfDUkIfZSBtCsgMAiTAQZ-0sbFAFAuejtHWNKxyyO6jzmU6UquD3vDN8_7uxnoQ8-GOIpfToaexTMgd-qThWNyJud_AgbkC_s14QJJTm-v0xal3Yhnk66w5OTdvjKHy2wKmXsegSJBP8aUIPGpRmGacDubZte-nglSF4fFtW3G00" class="reveal stretch plain">

---

## Visualizing the model (UML)

<img src="https://www.plantuml.com/plantuml/svg/JO_12i9034Jl-Og0b_eBzQA8Wc914CMBXzYckZRTbDsje5zlMZruov0taymy9WgfRmLWd03ofQXdtDAJi0lwu3BD81zbr3wKZALMV85yJo7-kAJOKiEuNXIRCxQs5ynE79xiF6-dvYyEAwoT3BwTKlLZjCQ_u05JjSnYM5wWrj30HDpjdgxIStvoiITnR_ww8TiB-NGiTdPWO95kvBmzni5aY-H9Nj550-yKr2ZsrHXgNRM3kKbh_W40" class="reveal stretch plain">

---

## Analyzing the model

<img src="https://www.plantuml.com/plantuml/svg/JOz12i9034NtEKN0ZLvXt2YYe5WeYEB6HMnJ7KqdCZCLzFIcrOMxVFvx7p9BcMBkMW4OBW2t40sC6teIFgBUkCfJS4DCsiMAiTAQJ-1AYkd7PSMMxeohUR4-OckzuFZ0ySa-y6PYVh5ROkEbzxPAzO_H1l-6UqpLDek-F46ZyGxku5D7uj_yTM1S2eMyBxOssnD85_81Hk8lrtoMZbt9qOeMAP2yaa-cN2cgyHpgOTH-rGVCBDhd7m00" class="reveal stretch plain">

