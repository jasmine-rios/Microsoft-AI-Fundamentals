# Overview of AI Workloads and Key Use Cases

This file is based off of chapter 3 from Tom Taulli's book.

The building blocks of powering AI:

- Content Moderation
- Personalization
- Computer Vision
- NLP
- Knowledge Mining
- Document Intelligence

## AI Principals
Ethical and practical considerations for AI is based on the following principals

- Accountability
- Inclusiveness
- Reliability
- Safety
- Fairness
- Transparency
- Security
- Privacy

## How does AI act so human?

It learns from data to make predictions that enable decision making, problem solving, understand language, recognize images, and create new media for consumption.

AI is a bunch of technologies and methods that build on each other to solve problems.

![Figure from book showing ai composition](/assets/images/ai-comp.png)

A lot of people think AI uses it's knowledge to minic us and take over. It's not the use case of actual AI.

It simply mimics human intelligence to help developers/engineers with problem solving, decision making, language understanding, and pattern recognition **intelligently** used on humans guiding them.

### Machine Learning (ML)
*Machine Learning (ML)* is under AI and allows machines to learn from data patterns.

ML does this through *algorithms* to identify patterns of the data feed and make a prediction or decisions.

Use cases: Recommendation systems, Fraud detection, and predictive analytics

### Deep Learning

*Deep Learning* is a subset of ML that uses artifical neural networks inspired by the human brain.

Kind of like... our brains ::

A good example I have seen on this on the phemonmena of "The Six Degrees of Seperation" being expressed by data science.

[Something Strange Happens When You Trace How Connected We Are Vertitasium - Youtube ](https://www.youtube.com/watch?v=CYlon2tvywA&pp=ygUhc2l4IGRlZ3JlZXMgb2Ygc2VwYXJhdGlvbiBzY2llbmNl)

Use Cases: image recognition, speech processing, and natural language understanding.

### Generative AI

This is the type that every knows as ChatGPT or a chat bot.

It creates new content in the form of text, images, audio, and video

Use Cases: Automated content creation, image synthesis, and creative problem solving.

## SO its not... alive?

No...but think of it like CyberPunk 2072 where you mechanizing your character with new add ons rather than a whole cyborg.

Each layer of CyberPunk 2072 works together in the background and the game gets easier the more you use your add-ons.

Completing a side mission is easier with it but you might not notice side missions are easier until you un-equip it.

## Content Moderation

*Content Moderation* spots and filters out harmful content before it hits production/public view **actively**.

Use cases: Social media, online forums/communities, or ecommerse sites

### Azure AI Content Safety Studio

**NOTE**
Used to be called Azure Content Moderator and requires Azure will require users to switch to *Azure AI Content Safety Studio* by **Feburary 2027**

Features of Azure Content Moderator
    - *Text moderation*
        Scans text for offensive content, including profanity and explicit material
    
    - *Image moderation*
        Analyzes images for adult content and can detect within images using *OCR*
    
    - *Custom term lists*
        Enables the creation of custom lists to filter specific terms according to content policies

    - *Video moderation*
        Evaluates videos for adult content, providing time markers for identified material

Here are the main features of Azure AI Content Safety Studio:
    
    - Moderate text content
        Test content easily with whatever size dataset. It's got a GUI to run tests and results. You can adjust sensitivity levels, set content filters, and manage blocklists to make sure your moderation system is just right for your needs.
    - Prompt shields
        This feature evaluates text to identify potential risks to LLMs from user input attacks
    - Groundedness detection
        Accesses if AI-gen text response text responses actual and factual
    - Protected material detection
        Identify custom content categories for personalized moderation.
    - Custom categories API
        Enables create and train of custom categories for personalized moderation 
    - Analyze text and image APIs
        
    - Template and workflows


