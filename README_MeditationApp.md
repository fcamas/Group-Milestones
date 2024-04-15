### Original App Design Project - README Template
===

https://hackmd.io/AWPu6S0iRcef9TWhTCWgWA

# **Meditation Timer**

An app designed to enhance meditation with personalized timers and music. Utilizing the [AudioDB API](https://www.theaudiodb.com/api_guide.php) for music integration.

## Table of Contents

1. [Overview](#Overview)
2. [Product Spec](#Product-Spec)
3. [Wireframes](#Wireframes)
4. [Schema](#Schema)

## Overview

### Description

The Meditation Timer app provides users with customizable meditation timers and curated music selections to elevate their meditation experience. By integrating with the AudioDB API, users can choose from a variety of soothing sounds and melodies to accompany their meditation sessions.

### App Evaluation

- **Category:** Health & Wellness
- **Mobile:** Yes, it's a mobile application.
- **Story:** The app aims to facilitate users in achieving a deeper state of meditation by providing personalized timers and calming music options.
- **Market:** Targeted towards individuals interested in meditation and mindfulness practices.
- **Habit:** It can be both a daily use app for regular meditators or an occasional use app for those exploring meditation.
- **Scope:** The app offers a narrow focus on meditation features, primarily centered around timer customization and music selection.

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

* User can set a personalized meditation timer.
* User can choose from a selection of meditation music.
* User can start, pause, and reset the meditation timer.

**Optional Nice-to-have Stories**

* User can create and save custom meditation presets.
* User can track their meditation sessions and view statistics.
* User can share their meditation achievements on social media platforms.

### 2. Screen Archetypes

- [ ] **Timer Setup Screen**
  * User can set the duration and intervals for their meditation session.
- [ ] **Music Selection Screen**
  * User can browse and select from a list of meditation music tracks.
- [ ] **Timer Screen**
  * User can start, pause, and reset the meditation timer.
- [ ] **Settings Screen**
  * User can adjust app preferences and customize meditation presets.

### 3. Navigation

**Tab Navigation** (Tab to Screen)

- [ ] Home
- [ ] Timer
- [ ] Music
- [ ] Settings

**Flow Navigation** (Screen to Screen)

- [ ] Timer Setup Screen
  * Leads to Timer Screen
- [ ] Music Selection Screen
  * Leads to Timer Screen
- [ ] Timer Screen
  * Allows navigation to Settings Screen
- [ ] Settings Screen
  * Allows navigation to Timer Setup Screen or Music Selection Screen

## Wireframes

[Add picture of your hand-sketched wireframes in this section]

### [BONUS] Digital Wireframes & Mockups

### [BONUS] Interactive Prototype

## Schema 

### Models

**User**
| Property | Type   | Description                                  |
|----------|--------|----------------------------------------------|
| userId   | String | unique id for the user                       |
| username | String | user's display name                          |
| email    | String | user's email address                         |
| password | String | user's password for login authentication     |

**MeditationSession**
| Property | Type    | Description                                 |
|----------|---------|---------------------------------------------|
| sessionId | String | unique id for the meditation session        |
| userId   | Pointer to User | identifies the user associated with the session |
| duration | Number  | duration of the meditation session in minutes |
| startTime| Date    | start time of the meditation session        |
| endTime  | Date    | end time of the meditation session          |
| completed| Boolean | indicates whether the session was completed |

### Networking

- **Timer Screen**
  - (GET) Retrieve user's saved meditation presets
  - (POST) Save new meditation session data
- **Music Selection Screen**
  - (GET) Fetch list of available meditation music tracks
- **Settings Screen**
  - (PUT) Update user preferences and settings
