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
        These APIs examine text and images for harmful content, offering multiple severity levels for nuanced moderation
    - Template and workflows
        These templates and customizable workflows provide an interactive platform to build tailored content moderation systems. The platform supports real-time ,pderation of user-generated and AI-generated content, includes Mirosoft's built-in blocklist for profanity, and allows the upload of custom blocklists to address specific needs.

## Personalization

*NOTE*
Will be deprecated in OCT 2026; Still on exam

*Azure AI Personalizer* is a tool that helps your **apps makes smarter decisions** by using *reinforcement learning*: a type of ML where the AI learns by feeding back on its actions. Basically, it imporves by trail and error

It **looks at context of your app**, **what the user is doing or where they are**, and considers a possible **set of actions** to figure out the **best decision**.  

When it makes a decision, you give it feedback, called a *reward*, which helps it learn and improve its choices in real time.

### Personalization Use Cases
Use cases:

- Ecommerce context to **boost chances** they will buy.

- Content recommendations such as figuring out which suggested article will **get most clicks**

### How Personalization Works

- Context
    The **information about your app**, users, or scenarios that **can influence decisions** (e.g. location, device type, user preferences)

- Actions
    A set of **potential decisions or items**, each with its own attributes (e.g. a list of products or articles)

- Reward 
    A score between **0 and 1** that shows **how good the decision was** (e.g. if a user clicks on a recommended article, it gets a score of 1)

## Computer Vision

*Computer vision* is a branch of AI that enables computers to **understand and analyze visual information from images and videos**. It attempts to **mimic the way humans see**.

By processing visual inputs, computer vision systems can detect objects, extract key details, and make decisions based on what they observe.

Azure AI Vision offers powerful tools that utilize computer vision to analyze images and videos. Its features include:

- Image analysis
    This tool extracts **detailed information from images**, such as identifying objects, faces, or inappropriate content. It can also generate automatic descriptions of what the image contains.

- OCR
    This feature recognizes and **extracts text from images**, whether **printed or handwritten notes**. This is useful for processing **buisness documents**, **reciepts**, invoices, or handwritten notes**

- Object detection
    This tool **locates and identifies objects** within an image. It provides details about the **objects positions** and **how many** instance of each object are present.

- Face recognition
    This feature detects **human faces in images** and provides attributes such as **age, emotion, and gender**. It can also perform **facial identification and verification**.

- Video analysis
    This tool includes features like **spatial analysis and video retrieval**. Spatial analysis **monitors movement in video feeds**, which is helpful for **understanding foot traffic** or ensuring **safety compliance**. Video retrival creates **searchable indexes** of videos using **natural language**.

Azure AI Vision also supports *digital asset management (DAM)*, whic helps you **organize, store, and retrieve media while managing digital rights**. For example, you can **group images based on logos, faces, objects, or even colors**. You can also automatically generate **captions and tag images iwth keywords** to make them easier to find.

## Natural Language Processing (NLP)

*Natural language processing (NLP)* is a technology that helps machines **understand and respond to human launguage**.

At its core, NLP breaks down human language-- spoken or written -- into something machines can understand.

Computers don't just recognize words, but can also **figure out intent behind full sentences or paragraphs**.

You use this when talking to Siri if you have an iPhone or using chat bots to get help online.

One of NLP's biggest jobs is making sense of the messy, unstructured way that humans communicate (e.g. slang).

Machines are used to structured data and NLP bridges that gap.

It also does grammer and context to respond more naturally.

NLP is behind a lot of the AI-powered technology we use today.

NLP gets the meaning (e.g. "What's the weather like"; picks out "weather" and "like" and processes whole sentence to understand you are asking for a forecast)

This deeper understanding, called *semantics*, is what makes NLP different from basic text matching. 

It's what helps AI generate responses that feel more human and natural.

*Azure AI Language* let's you work with NLP. It combines three tools under one roof and adds new features:

- Text analytics
- QnA Maker
- LUIS (Language Understanding)

These features listed above come in two flavors: 

- Preconfigured (Use AI models as-is without tweaking anything)

- Customizable (Train the model with your own data)

Here is things you can do with Azure AI Language:

- *Named entity recognition (NER)*
    Automatically **tags** words or phraces into **catergories** like people. places, dates, etc.

- *Personally identifying Information (PII) detection*
    **Finds sensitive data** such as phone numbers or ID numbers, and **hides it**.

- Language detection
    Figures out **what language a document is written in and returns a code for it**.

- Sentiment analysis and opinion mining
    Analyzes text to determine if it's **postive or negative**.

- Summarization
    **Pulls key sentences from a document** to create a summary.

- Key Phrase extraction
    Identifies the **main idea** in the text.

- Entity linking
    **Inserts links from words** or phrases in the text to their **cooresponding Wikipedia pages**, helping to improve clarity.

- *Custom text classification*
    Lets you  **train an AI** model to categorize documents based on your **own categories**.

- *Custom NER*
    Allows you to train a model to **identify custom labels in your text**

- *Conversational Language Understanding (CLU)*
    Builds custom models that **understand and extract valuable info from user messages**.

- *Question answering*
    Provides the **best answer to user questions**, which is ideal for chatbots and voice-enabled apps.

## Knowledge Mining

Knowledge mining uses AI to interpret vast amounts of data. Often, the focus is on *unstructured data*, which is information that lacks a predefined format, such as text documents, email, texts, images and videos.

In contrast, *structured data* is organized in a standard format, typically in tables with rows and columns, making it **searchable and analyzable**.

The process for knowledgeme mining is farely simple, you gather your data, enhance it with AI tools like language or image recognition, and then explore it through search and visualizations. This way, you can quickly find the connections you need to make better decisions.

Microosft has developed *Azure AI Knowledge Mining* to make this procress easier. It **combines AI, ML, and seach technology** to help you extract, enrich, and explore your data. Here are some key features:
    
- Cognitive skills
    These are **Prebuilt AI** models that **automatically extract and structure information from text, images, and other media**. For example, they can pull texy from scanned documents, detect different languages, extract key phrases, and identify objects in images.

- Enrichment
    Knowledge mining goes beyond just keyword searching by enhancing your data. It can categorize information, pull out entities like names or locations, and translate text.
    Plus you can build your own AI models to add custom enrichments based on your specific needs.

- Customizable indexing
    This tool helps you create a **searchable index of your data**, mkaing it easy for users to find relevant information quickly. You can also **customize how the index is built to fit your particular use case**

- Integration with Azure search
    Knowledge mining works hand-in-hand with the **Azure Cognitive Search** serive, which is a search-as-a-service solution. This means you can easily **scale your search capabilities and manage queries across enriched data** without breaking a sweat.

## Document Intelligence

*Document intelligence* also referred to as *document AI*, uses AI to automate the **extraction, comprehension, and organization of data** from various documents, such as **forms, invoices, and receipts**. 

This technology **transforms unstructured information into structured, actionable data**, improving efficiency and accuracy in data processing.

## Document Intelligence V. Knowledge Mining

Easy to confuse with knowledge mining but is focused on the extraction and structuring data from documents to automate data entry/processing

Knowledge mining is more for analyzing large volumes of data to make patterns, relationships, and insights across the whole datascape.

Both use AI to process data but document intelligence is at the **document level**
and **knowledge mining works at a broader l,cross-document level** to facilitate comprehensice data exploration and discovery.

## Azure AI Document Intelligence service

The main features of *Azure AI Document Intelligence* service:

- General extraction models
    These models are designed to **work across a wide range of documents without needing customization**. They can pull out key details like text, tables, **key-value pairs**, and the **overall structure** of a document.
    This makes them good for organizations that handle various types of documents and need consistent data extraction.
    Whether the document is structured, semi-structured, or unstructured, these models provide quick, reliable results without needing any training or labeling.

- Prebuilt models

    Azure also provides **ready-to-use models** for **common document types**, such as invoices, receipts, identity documents, and tax forms. These models are preconfigured to extract specific data fields like dates, payment amounts, or personal details. For example, the prebuilt models can handle W-2 forms and include support for other documents, such as 1099 tax forms and health insurance cards

- Custom models
    If you have more specific needs, Azure lets you create cusom models tailored to your business. You can train these models using your own data, so they know exactly what information to look for in your documents.

    Azure offers two type of custom models: **template models**, which are great if your documents follow a similar structure, and **neural models**, which are flexible enough to handle documents with different layouts.

## Generative AI

*Azure OpenAI Service* **provides developers with a comprehensive toolkit to create generative AI applications that can transform various buisness operations**.

It allows for the development of custom AI copliots and agents, giving companies the flexiblility to **integrate AI into their workflows**. One of the standout features is its support for different AI models, such as **GPT-4o, GPT-Turbo, embeddings, and Wisper**.

The **Azure OpenAI studio**, which serves as the **main user inferface** simplifies the management and customization of these models.
Users can explore, fine-tune, and deploy models directly from the studio. This makes it an **assessible solution for both technical and nontechnical users**.

Azure OpenAI supports advanced capabilies, such as *retrival augmented generation (RAG)*. This technique allows developers to run models on specific datasets, providing more accurate and contextually grounded outputs.
For organizations looking to automate knowledge-based tasks, this feature enchances AI's ability to generate precise responses based on their proprietary information.

For example, a company can **implement RAG by integrating Azure OpenAI Service with Azure AI Search to create a chatbot**that answers employee questions about internal policies, like health benefits.
By indexing company documents and using RAG, the AI can retrive relevant information and provide accurate, **context-specific responses** to employee inquiries.

In the creative domain, Azure OpenAI models like **DALL-E open new doors for content generation**.
This allows designers and marketers to **produce unique visuals from simple text prompts**. The technology has been particularly impactful in media and entertainment, where quick, dynamic creation is crucial to keeping up with customer demand.

The test will be centered on differences betwen services

## Guiding Prinicipals for Responsible AI

AI is an awesome and makes life easier but comes with risks.

One of the big risks is *bias* in AI models which can lead to **unfair results**. 
For example, a loan-approval system that discriminates based on gender because it was trained on biased data.
This can have serious consequences such as **inequalities, damage of trust in AI systems, and legal or regulatory repercussions for business**.

The other risks are:

- **Potential for errors**, such as autonomous vehicle malfunctions, that could cause accidents.

- Concerns about **how AI uses data**, especially sensitive information like patient data in medical bots, which could be exposed if not securely stored.

- AI solutions that **may not be inclusive to all users**, such as a home assistant without audio output that excludes visually impared users.

- **Accountability concerns** in AI decision making, such as wrongful convictions **due to faulty facial recognition**.

To address these challenges, Microsoft has created 6 guiding principles for *responsible AI*, which fall into 2 main categories

- Ethical AI
    Ensures that AI systems are designed and used in a way that aligns with moral principals like accountability, transparency, security. and privacy.

- Explainable AI
    Focuses on making AI systems transparent and easy to understand; includes principals like fairness, transparency, security, and privacy.

Microsoft's 6 guidelines are common for questions on the exam, so you should memorize them and understand how they apply to different scenarios.

## Accountability

When you are designing and deploying AI systems, the **responsiblity lies with you to ensure it operates ethically and safely**.
You need to make sure the technology **aligns with both legal and industry standards** --essentially you make sure it's fair, responsible, and trustworthy.
Take Microsoft's approach: **creating a framework that prioritizes accountability, starting with impact assessments early on**.
These assessments look at **how AI might afffect individuals, organizations, and society**.
By keeping a close eye on these evaluations, especially when something could go wrong, you can **manage risks throughout the AI's lifespan**.

But accountability doesn't end with the launch. Microsoft advocates for **human oversight, making sure that AI doesn't run the show without meaningful human input**.
The people managing these systems need the right tools to maintain control and step in when necessary. **This keeps you from becoming overly reliable on AI outputs-- ensuring that human accountability is always part of the equation -- especially in more complex or high-stakes situations**

To keep things in check, **it's essential to set up internal review teams**. These teams can oversee key decisions realted to **AI development and deployment, particularly in sensitive areas like health care, employment, or facial recognition**.
If misused, these tools can potentially cause physical or emotional harm or infringe on people's rights.
It's important to have clear legal boundaries to prevent overreach and protect individual freedoms.

**Laws and regulation play a huge role in maintaing AI accountability**, but only part of the puzzle. Businesses, governments, and other stakeholders also have to rake responsibility. 
Microsoft, for instance, has developed its own guiding principals for working with sensitive tech like facial recognition.