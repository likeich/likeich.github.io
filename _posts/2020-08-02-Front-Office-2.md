---
layout: post
title: Front Office 2.0
---

- Written in Java and JavaFX
- Currently over 6000 lines of code written by me personally, 11000+ in total
- 20 Java classes and more FXML files

{% include image.html image_src='/images/frontoffice2/main-pic.webp' description='Main Picture' %}

---

Front Office 2.0 is my current programming project. As such, it is a work in progress and not all features are implemented.

## Purpose

A local car wash business chain with multiple locations has a proprietary database software package written in an old database management system. The system is used to run a wash loyalty program where customers can gain benefits from loading money onto and using a special credit-card-like card. The database program polls card readers on the lots for swipes, receives the card numbers, and checks the user’s account on the database and starts the wash if applicable. The system is synced across multiple car wash locations.

This system is now halting upgrades to bring the computers at the washes up to modern standards and is preventing the company from moving to the forefront of car wash technology. The program I am now writing, Front Office 2.0, will replace that program and enable the business to prosper into the future.

{% include video.html url='/images/frontoffice2/purpose-vid.mp4' %}

## Features

- A cloud database is used to store data that will also be synced offline in case of the loss of the internet connection.
- Simple weather display.
- Link to the Miracle Car Wash business website.
- A card monitor that polls an RS485 network of bar code card readers constantly and displays them in an easy-to-read manner.
- MDB uploader to upload the old database file to Google Cloud FireStore.
- Password-protected program to interact with customer data on the cloud database. This section includes the ability to query for customers, look at card histories, reissue cards, and other actions.
- DDE interactor that interacts with a SCADA software to start the washes.
- Created using the Gradle build system.
- Designed with the Metro UI Design Language in mind.

{% include image.html image_src='/images/frontoffice2/test-setup.webp' description='This is a testing setup to test the polling of the card readers that I put together. It uses an RS232 to RS485 adaptor. In practice, multiple readers will be attached to this system. To poll them, a specific code and acknowledgement has to be sent through a serial port.' %}

---

{% include image.html image_src='/images/frontoffice2/card-monitor.webp' description='The Card Monitor' %}

{% include image.html image_src='/images/frontoffice2/mdb-upload.webp' description='A simple MDB upload in progress' %}

{% include image.html image_src='/images/frontoffice2/loading-card.webp' description='Loading a card from the database' %}

{% include image.html image_src='/images/frontoffice2/washcard-history.webp' description='My personal card history, queried from 630,000+ log files' %}

{% include image.html image_src='/images/frontoffice2/reissue-card.webp' description='Reissuing a card' %}

{% include image.html image_src='/images/frontoffice2/search-card.webp' description='Search for a card' %}

{% include image.html image_src='/images/frontoffice2/delete-card.webp' description='Delete a card menu' %}
