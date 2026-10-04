---
title: "WEEK 40"
date: 2026-10-04
draft: false
description: "An inspirational app for artists"
---

Stine Torndal · 3. semester, Datamatikeruddannelsen (EK Lyngby)

{{< lead >}}
An app to lend a helping hand to artists with art block and lack of inspiration.
{{< /lead >}}

---

## 1. This week's goals and tasks: 

* [x] Survive
* [x] Figure out to potentially implement this week's technologies in ArtPrompt
* [x] Set up Javalin REST routing
* [x] Implement clean 3-layer architecture for Saved Images (DAO / Service / Controller / DTO)
* [x] Add global exception handling with ApiException and structured logging with Logback
* [x] Write integration tests using a dedicated PostgreSQL test database (artprompt_test)

## 2. Progress

* **1:** Done
* **2:** Done, integrated REST
* **3:** Done, fully functional integration with Unsplash API via Java's HttpClient.
* **4:** Done, users can now save their favorite Unsplash images to PostgreSQL (POST /api/v1/images/save) and retrieve their saved gallery (GET /api/v1/images/user/{userId}).
* **5:** Done, working fine with 7 days log
* **5:** Done
  
## 3. Implementing new technologies from Class

This week's assigment: Webhooks, websockets
I have not implemented it to my project as I cannot find a use for it in my backend


## 4. Status / challenges

* [ ] **Time**    
     Not enough time to understand, implement and design architecture. 
* [x] **Architecture and flow**
     The massive scale of a solo project when OOP, separation of concerns and a minimalist approach to coding design makes it very difficult for me to have an overview. 
     

## 5. Next week (week 41)

* [ ] Plan is to make my own exception
* [ ] Make textUI
* [ ] Deploy because that's in class assignment
  