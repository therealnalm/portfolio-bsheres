---
title: Assignment 3 Convergent Design
layout: doc
---

# Assignment 3: Convergent Design

## Pitch

> OpenJournal is a social media app that allows you to focus on what matters: you and your friends. Today, mainstream social media apps have lost track of what made them special to begin with. With OpenJournal you can create a journal of memories and thoughts for yourself but also choose to share parts with your closest friends. Unlike other apps, its not designed to pull you in. Rather, its built to help you connect with yourself and friends on a deeper level. OpenJournal is meant to help you live life to the fullest, by allowing providing a simple platform to stay in touch with yourself and thoughtfully engaging with friends. OpenJournal is centered around Journal Entries, longform posts that you can create for yourself, create to spark thought or conversation with friends, or respond to a friend.

## Concepts

# Entry \[Text, Image]

|:---: | :---: |
| Purpose | To allow users to record and/or communicate their thoughts and feelings via text and visuals |
| Operational Principle | A user writes a piece of text to accompany some visuals and it can be viewed later |
| State | caption: Text, visuals: set Image |
| Actions | create(text: String, visuals: Image[]); |

# Journaling \[Entry]

| Purpose | Store and access multiple entries in one location based on a common theme/purpose |
| Operational Principle | You put your entries in a journal to keep them organized |
| State | entries: Set\[Entry] |
| Actions | add(entry: Entry); remove(entry: Entry) |

# Reminding \[Object, Time]

| Purpose | Have something brought to your attention at a later date |
| Operational Principle | A reminder for and object is set for 3 days later, and at that point in time it is brought to your attention |
| State | object: Object; remindTime: time |
| Actions | set(object: Object, time: Time); remind() |

# Platform Sending \[Object, Platform]

| Purpose | Bring an object to a certain platform |
| Operational Principle | You want to send an object to someone on a certain platform |
| State | platform: Platform; object: Object |
| Actions | send(object: Object, platform: Platform) |

# Chain Linking \[Object]

| Purpose | Create a linear relationship between multiple of the same object |
| Operational Principle | Given an object, if you want a new object to follow it, you chain them |
| State | object: Object -> 1 parent: Object |
| Actions | addToEnd(object: Object) |

# Friending \[Party]

| Purpose | Create a mutually accepted relationship between two parties |
| Operational Principle | You and a friend both want to establish a relationship so you become friends |
| State | friendPairs: \[friend1, friend2][] |
| Actions | befriend(friend1: Party, friend2: Party), unfriend(friend1: Party, friend2: Party) |
