---
layout: post
title: "Navigating Through Chaos: How to Use LLMs to Survive an Informational Storm"
author: sal
categories: [AI,  Productivity, Python]
image: assets/images/NavigatingThroughChaos.png
comments: false
featured: true
---




In our rapidly changing and increasingly unstable world, the accelerating pace of digital transformation leads to a constant bombardment of information, making it easy to feel overwhelmed by the sheer volume and speed of these changes. Therefore, it is crucial to develop more effective ways to manage and navigate this information overload.

> One promising approach is to use Large Language Models (LLMs) to filter and organize a specific domain of internet knowledge in a predictable, easy-to-interpret, and goal-oriented manner, minimizing distractions.

This article explores how Large Language Models (LLMs) can help manage informational overload, presents my thoughts on the subject, and offers a proof of concept (PoC) for automating the exploration of new knowledge domains.


## The Bottleneck: Human Brain

Despite individual variations in intelligence, all human brains share inherent constraints that limit how quickly and efficiently we process information. These constraints include the limited capacity of short-term memory, which restricts the amount of information we can handle simultaneously, and the speed at which we can assimilate new information and transfer it to long-term memory. IQ essentially reflects these cognitive abilities. Based on current literature [reference], it is possible to prevent cognitive decline with age rather than increase IQ. Therefore, the true challenge lies in how we make the best use of the powerful machine inside our skull.

To achieve this, it is crucial to filter and structure information in a way that matches our cognitive abilities at any given moment makes learning easier and more efficient. 

To discuss further the constraints of the human brain, let's explore an ideal scenario for learning a new domain of knowledge.

Firstly, it is essential to set clear goals for your learning journey. Determine what you want to learn next. From a motivational perspective, choosing a domain that is personally significant will generate more positive emotions during the learning process compared to less significant. However, the vast array of available options can be overwhelming due to our cognitive limitations. While we can comfortably handle several options, presenting ourselves with 100 choices can be paralyzing. That’s why a tool for simplifying the decision-making process would be useful.

Once you have identified a valuable knowledge domain, it is important to approach learning hierarchically. Organizing information hierarchically reduces the demands on our short-term memory while allowing us to see the context of each piece of information. Moreover, our brains naturally organize and structure information in this manner, remembering details from general to specific [reference].

Next, consider how to spread out the learning process effectively. The first important concept is the U-curve of dopamine, which indicates that motivation tends to be highest at the beginning and end of a learning project. To leverage this, start a project that you can complete within a timeframe that sustains your initial excitement and allows you to maintain momentum as you approach the finish. For me, this optimal period is around three weeks. The second crucial element is reinforcing the acquired knowledge through spaced repetition. This method helps transfer information to long-term memory. The idea is to use the knowledge consistently over at least six weeks, reviewing it at exponentially increasing intervals, for example, after 1 day, 3 days, 9 days, and 27 days. This approach allows for partial forgetting, which makes each review session more challenging, thus supporting memorization and at the same time not requiring excessive time for revisions.

So, the ideal learning frame for me based on those constrains would be to quickly define what to learn next, which with reasonable probability is at least one of the best choices to make, explore it hierarchically from general to specific within 3 weeks, and revise several times to at least use this knowledge within 6 weeks.

## Traps of the Dynamic Digital Age

In today's digital age, platforms have become increasingly addictive, with many designed to keep users engaged for as long as possible. They often employ eye-catching images and clickbait headlines to lure users into spending more time on their site. This can lead to users, myself included, losing hours to interesting but ultimately useless content. and that could not only losing time but also overwhelming yourself with data which we don’t need It requires significant willpower to resist these temptations, and with advancing algorithms, these platforms will likely become even more addictive in the future

The ease of content generation has also exploded, leading to an overwhelming amount of information available online. As technology rapidly evolves, the rate of content production accelerates. We are caught in a positive feedback loop where each technological breakthrough speeds up the next, contributing to an ever-growing sea of information. While this might seem beneficial at first glance, providing a wealth of knowledge at our fingertips, it also presents a significant challenge.

The sheer volume of choices available to us can be paralyzing rather than empowering. With countless options to choose from, we can easily exceed our capacity to process information, leading to feelings of being overwhelmed. This phenomenon is compounded by the dynamic nature of our world, where constant technological advancements and societal changes make it increasingly difficult to keep up.

 The key to addressing these challenges lies in developing strategies to filter, organize, and prioritize information effectively, ensuring that we can focus on what truly matters without getting lost in the noise.



## PoC Workflow Explanation

Managing the deluge of information in today’s digital age can be overwhelming. Drawing from my personal experience, I have developed a manual process to handle this chaos. It wos warking quite well but ti requires a lot of will power to stik to it and a lot of my cognitive recourses. So I now aim to automate it by using Large Language Models (LLMs). This chapter explains the workflow designed to efficiently retrieve, process, and rank information, ensuring that only the most relevant resources are highlighted. 

User input 
Search phrases are specific keywords or terms used to query various platforms for pertinent resources. These phrases are carefully selected to ensure that the content retrieved is relevant to the user's areas of interest. The search phrases guide the initial step of gathering information from multiple sources.

Specific questions are detailed inquiries that the workflow aims to answer using the retrieved resources. They serve as a guide for summarization and ensure that the output directly addresses the user's needs. These questions help to filter and focus the information, ensuring that only relevant data is processed and summarized.

Platforms refer to the sources from which the workflow retrieves information. These could include video platforms, websites, academic databases, or any other repositories of digital content. Specifying platforms helps to streamline the search process and ensures that the resources come from credible and relevant sources. which are implemented.

Time Horizon
The time horizon defines the period within which the resources should be considered. It limits the search to recent information, ensuring that the data retrieved is up-to-date and relevant. This parameter helps to filter out outdated content and focus on the most current insights and guidelines.

Max Outputs per Platform
This parameter specifies the maximum number of resources to retrieve from each platform. It helps manage the volume of data and ensures that the workflow does not become overwhelmed with too much information. By setting a limit, the system can focus on the most relevant and high-quality resources available.



<div style="text-align: center;">
  <img src="{{ site.baseurl }}/assets/images/Data_flow.svg" alt="Data Flow" />
</div>



Below is a detailed breakdown of the process visualized in the provided flowchart.

1. Retrieve Resources with Details for Each Query
The first step involves gathering resources from various platforms based on predefined search phrases. These queries are specifically tailored to extract relevant information on topics of interest. In this case, search phrases such as "Huberman exercise routines," "Huberman cold exposure benefits," and others are used to pull detailed content.

2. Combine Resources (Eliminate Duplicates)
Once the resources are retrieved, they are consolidated to remove any duplicates. This ensures that each piece of information is unique, streamlining the subsequent processing steps and avoiding redundancy.

3. Separate Resources with Content from Without
The next step is to filter out resources that lack substantial content. This separation ensures that only those resources which contain meaningful information proceed to the next stages of processing.

4. Add Summaries to Each Resource, Prioritizing Information Needed to Answer Specific Questions
Each resource is then summarized, with a focus on extracting details that are crucial for answering the predefined specific questions. This step is critical for condensing large volumes of information into manageable summaries.

5. Add and Answer Specific Questions in Summaries
Following the summarization, specific questions are addressed within the summaries. This integration helps in directly linking the retrieved information to the user’s queries, providing concise and targeted answers.

6. Separate Resources with Zero Answers
Resources that do not contribute any answers to the specific questions are filtered out. This step further refines the pool of useful information, ensuring that only relevant data is retained.

7. Rank Resources by Number of Answers Provided
The remaining resources are ranked based on the number of questions they answer. This ranking helps in identifying the most comprehensive and informative sources, facilitating easier access to high-quality information.

8. Separate Top Resources from the Rest
Finally, the top-ranking resources are separated from the rest. These top resources are the most valuable as they provide the most answers and relevant information. This final step ensures that the user receives the best possible insights without having to sift through all retrieved data.


Output

top rescoursec hierarchal information

also I can look also at the rest without contetn sourses 


### Example Run

<div style="text-align: center;">
  <img src="{{ site.baseurl }}/assets/images/RunDemonstration.gif" alt="Run Demonstration" />
</div>


## Why Not Just Use Products Like ChatGPT?

By adopting this approach, I can achieve more predictable, stable, and reliable outputs. This is because I understand how the system filters information, rather than working with a complex black box. Additionally, this method enhances my understanding of the workflow, as each Language Learning Model (LLM) performs small, easily interpretable tasks.



## Conclusions

In the digital age, information overload is a significant challenge. This exploration highlights how Large Language Models (LLMs) can help manage this by filtering and organizing knowledge efficiently.

The brain's limited short-term memory and processing speed require structured, hierarchical learning. Clear goals and hierarchical organization reduce cognitive load and improve learning efficiency.

Setting clear, significant learning goals boosts motivation. Using the U-curve of dopamine and spaced repetition enhances long-term memory retention.

Addictive digital platforms and the rapid growth of content contribute to information overload. Effective filtering and prioritization are essential to manage this overload.

Automating information management with LLMs reduces cognitive burden and improves information quality. The developed workflow retrieves, filters, summarizes, and ranks information, providing a structured and transparent method.

The PoC shows LLMs can automate information management, ensuring relevant, high-quality resources. This structured approach offers stable and reliable outputs, enhancing decision-making and learning processes.

Leveraging LLMs helps individuals navigate the information overload, aligning with cognitive abilities and providing a scalable, efficient solution to the challenges of the digital age.