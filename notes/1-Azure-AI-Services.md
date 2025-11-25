# Azure AI Services
**NOTE**
This file is based off of chapter 1-2 from Tom Taulli's book.

Most of all, it is summarized and quotated with other resources listed in `resources.md`

!()[/asset]
assets/images/ai-architecture-pitfalls.png
## Exam Topics Weigh Scale

- AI Workloads and Considerations (15-20%)
    - Identify features of common AI workloads (computer vison, NLP or natural language processing, document processing, and generative AI workloads)
    - Identify guiding principles for responsible AI (Considerations for fairness, relability/safety, privacy/security, inclusiveness, transparency, and accountability)
    
- Machine Learning Principles on Azure (20-25%)
    - Identify common machine learning techniques (Identify regression machine learning, classification machine learning, clustering machine learning, deep learning techniques AND Transformer architecture)

    - Describe core machine learning concepts (Identify features and labels in a dataset; Describe use of training and validation datasets are used in machine learning)

- Computer Vision Workloads on Azure (15-20%)
    - Identify common types of computer vision solution (Image classification, object detection, optical character recognition solutions, facial detection and facial analysis solutions)

    - Identify Azure tools and services for computer vision tasks (Describe capabilite of the Azure AI Vision or Azure AI Face detection service)

- NLP Workloads on Azure (15-20%)
    - Identify features of common NLP Workload Scenarios (key phrase extraction, entity recognition, sentiment analysis, language modeling, speech recognition and synthesis, and translation)

    - Identify Azure tools and services for NLP workloads (Descrive capabilities of Azure AI Language service and Azure AI Speech service)

- Generative AI Workloads on Azure (15-20%)
    - Identify features of generative AI solutions (generative AI models, common scenarios for generative AI, and responsible AI considerations for generative AI)

    - Identify generative AI services and capabilities in Microsoft Azure (AI Foundry, Azure OpenAI service, Azure AI Foundry model catalog)

## Azure AI Services

The categories: 
- Language processing
- Image recognition
- Intelligent Search
- Content Generation

These services can be implemented in both web and mobile apps and can use the services from Azure or create your custom AI app.

Azure AI services is prebuilt and ready for use.

Their services is backed by Microsoft Azure resilient infrastructure and the ML models are pretained and acessible for buisnesses or workloads of any size.

There is years of AI research to back their models and some are simply "plug-n-play" to your existing workloads.

Developers can access AI tools via REST API or SDKs (e.g. Python or GO).

**API** (application programming interfaces) allows application to connect and communicate.

This allows a website to connect to a database using API calls to fetch data or write data.

**SDKs** (Software Devlopment Kits) bundle the tools, libraries, and documentation to build apps on specific platforms.

Azure AI services also integrates with **Azure Logic Apps** and **Power Automate**.

Azure can run in the cloud, on-premises, or on the edge.

**The edge** is where you put it as close to the data where it was created. (e.g. Internet of Things (IOT) in remote areas to reduce latency and bandwidth clogging internal network; DMZ services)

### Cost of Azure AI Services
AI services such as Azure Machine Learning and Cognitive services are free for 12 months.

Azure Congitive Text analytics or Azure AI Vision has free usage limits during the trial period of 12 months.

Use **Azure Calculator** to estimate costs.

### Create Azure AI Resource

To use Azure AI services, you need to setup a resource first by either these 2 options:

- Multiservice resource: Access AI services using a single key and endpoint. Ideal for AI Speech, AI vision, and AI language for projects that require using several services together. Consolidates billing under one resource.

- Single-service resources: Each services gets their own key and endpoint. Easier to track cost and usage separately.

Steps to create AI Resource for multiservice resource:

1. Log into Azure Portal and sign in.

2. Click -*Create a Resource*- 
**OR**
Search for "Azure AI services" for multiservice resource or the specific service for singe-service resources (e.g. AI Face, AI language, or AI Content Safety)

3. Click **-*Create*-** and fill out the information for the -*subscription*-, -*Resource Group*-, Region, and -*pricing tier*-.

4. Click **-*Review + create*-**

### Studios

After creating the AI resouce, you can start to build out the application by working with -*REST API*-, -**SDKs*-, or create quicker with studios (GUI on Azure Portal for AI services)

Studios can be used by beginners and experienced developers as it is click-and create and customizable.

Studios allows to explore, demo, and evaluate services (e.g. Vision Studio, Language studio, Speech Studio, Content Safety Studio)

- **Vision Studio**: Has image and videp analysis tolls like **object detection**, **image classification**, and **video analysis**.

- **Language Studio**: Text-based AI services like **sentiment anaylsis**, **translation**, and **text summarization**

- **Speech Studio**: Azure's **speech-to-text**, **text-to-speech**, and **real-time translation services** and is helpful to build apps that need voice interaction.

- **Content Safety Studio**: Used for modarating and detecting harmful content and set up safeguards against that content. (e.g violence and hate speech)

**Azure AI Foundary** (formally -*Azure AI Studio*-) combines  Azure AI services into one platform.

Developers can use Azure Foundary to create AI apps using the latest API and models.

## Demo Using Vision studio and Adding 

1. On Azure Portal and logged in, search and select "Computer Vision" in the top search bar.

2. Fill out information for the *subscription*, *resource group*, *region*, *name*, and *pricing tier*. 

3. After information is filled in, click "Create".

4. Once setup, click "*Go to resource*" then click "*Go to Vision Studio*".

5. Upload from your computer or choose a sample image. The AI will take that image and use *Computer Vision* to generate a caption.