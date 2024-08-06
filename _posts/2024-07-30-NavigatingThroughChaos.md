---
layout: post
title: "Navigating Through Chaos: How to Use LLMs to Survive an Informational Storm"
author: sal
categories: [AI,  Productivity, Python]
image: assets/images/NavigatingThroughChaos.png
comments: false
featured: true
---

In our rapidly changing world, the accelerating pace of digital transformation leads to a constant bombardment of information. This deluge of data makes it easy to feel overwhelmed by the sheer volume and speed of these changes. In addition to that, platforms like YouTube captivate our attention with endless engaging content, consuming more of our time. Their addictive nature intensifies the challenge, highlighting the urgent need for effective strategies to manage information overload.

> One promising approach is to use Large Language Models (LLMs) to filter and organize a specific domain of internet knowledge in a predictable, easy-to-interpret, and goal-oriented manner, minimizing distractions.

This article explores how LLMs can help manage informational overload, presents insights into human brain limitations, the traps of our unstable reality, and offers a proof of concept (PoC) for automating the exploration of new knowledge domains.

## The Bottleneck: Human Brain

Despite individual variations in intelligence, all human brains share inherent constraints that limit how quickly and efficiently we process information. These constraints include the limited capacity of short-term memory and the speed at which we can assimilate new information and transfer it to long-term memory. IQ essentially reflects these cognitive abilities. Current literature suggests it is possible to prevent cognitive decline with age rather than increase IQ [1]. Therefore, the true challenge lies in how we make the best use of the powerful machine inside our skull. To achieve this, it is crucial to filter and structure information in a way that matches our cognitive abilities at any given moment, making learning easier and more efficient.

To discuss further constraints of the human brain, let's explore an ideal scenario for learning a new domain of knowledge.

Firstly, it is essential to set clear goals for your learning journey. Determine what you want to learn next. Choosing a domain that is personally significant will generate more positive emotions during the learning process[2, 3]. However, the vast array of available options can be overwhelming due to our cognitive limitations. While we can handle several options comfortably, presenting ourselves with 100 choices can be paralyzing [4]. Therefore, a tool for simplifying the decision-making process would be useful.

Once you have identified a valuable knowledge domain, it is important to approach learning hierarchically. Organizing information hierarchically reduces the demands on our short-term memory while allowing us to see the context of each piece of information. Moreover, our brains naturally organize and structure information this way, remembering details from general to specific [5].

Next, consider how to spread out the learning process effectively. The U-curve of dopamine indicates that motivation tends to be highest at the beginning and end of a project. To leverage this, start a project that you can complete within a timeframe that sustains initial excitement and brings you to the point where you can see the end. This concept is reflected in Agile methodologies such as Scrum [6], which emphasizes short development cycles called sprints, typically lasting 1-4 weeks, and productivity books like The 12 Week Year [7], where a quarter is condensed into three weeks. For me, this optimal period is around three weeks. Then to help transfer new knowledge to long-term memory, reinforce acquired knowledge through spaced repetition [8]. This technique, involves consistently using the knowledge over several weeks or months. Generally, the longer the duration, the higher the chance of transferring it to long-term memory. I typically use a 6-week period. Review the material at exponentially increasing intervals, such as after 1 day, 3 days, 9 days, 27 days, and so on. This approach allows for partial forgetting, making each review session more challenging and thus supporting memorization without requiring excessive time for revisions.

Therefore, the ideal learning strategy would be to quickly define a meaningful learning objective, explore it hierarchically over approximately three weeks, and revise it multiple times using spaced repetition techniques.

## Essential Traps in Our Digital World

In today's digital age, several factors contribute to the sense of information overload.

One major factor is the increasingly addictive nature of informational platforms like Youtube, which are designed to keep users engaged providing videos with eye-catching images and clickbait headlines. This can result in users, myself included, losing hours to interesting but ultimately useless content. Not only does this waste time, but it also overloads us with unnecessary data.

Moreover, the rapid advancement of technology creates a positive feedback loop, where each breakthrough accelerates further innovation. This exponential growth means that within the same period of time, we encounter increasingly more new technologies and tools to learn, which can easily surpass our cognitive capacities.

Additionally, the simplicity of content creation, particularly with AI tools, has significantly increased the amount of information available online. As technology develops, this phenomenon accelerates further, and the volume of choices available to us can be paralyzing rather than empowering.

Therefore, the key to addressing these challenges lies in developing strategies to filter, organize, and prioritize information effectively, ensuring that we can focus on what truly matters without getting lost in the increasing noise.


## Automating Web Information Management with LLMs

Learning something new involves venturing into the unknown, essentially navigating chaos. The goal is to make this process stable and predictable, leveraging the benefits of both chaos and order. From my personal experience, I developed a step-by-step manual process to manage this challenge. While effective, it required considerable willpower to maintain focus and resist platforms-served temptations. Additionally, it consumes a significant portion of my cognitive resources. Therefore, now I aim to automate this process using LLMs. This chapter outlines a workflow designed to efficiently retrieve, filter, rank, and organize information from a wide range of knowledge domains simultaneously.

### User Input Parameters

The goal of this workflow is to simplify the decision-making process for the user by limiting the available options, as an excess of choices can generate chaos. Therefore, the user only needs to set the most important parameters. Below is a list of key parameters that need to be configured for a search:

**Search Queries**

These are the queries that users typically write in Google or YouTube. This is a crucial parameter. To streamline the parameters, each phrase retrieves up to 10 resources. Users can broaden their exploration by defining multiple similar phrases in one run, each approaching the problem from slightly different angles.

**Specific Questions**

These questions directly relate to the content of each source. They provide objectives and criteria for evaluating the sources. Sources that answer fewer questions will rank lower.

**Platforms**

Users can specify the platforms to search. Currently, YouTube, Google, and GitHub are available. This allows for searching multiple platforms within one run.

**Time Horizon**

Users can set a Time Horizon parameter to declare how old the resources can be. This helps to filter out outdated content and focus on the most current insights and guidelines.

**Max Outputs per Platform**

To manage the volume of data, users can set a maximum number of resources to retrieve from each platform. This helps in focusing on the most relevant resources without being overwhelmed by too much information. Typically, this is set between 3 to 9.

### Workflow Breakdown

Below is a detailed breakdown of the workflow, as visualized in the provided flowchart, detailing the steps involved for processing information on a single platform.


<div style="text-align: center;">
  <img src="{{ site.baseurl }}/assets/images/Data_flow.svg" alt="Data Flow" style="margin-bottom: 30px;" />
</div>


**Retrieve Resources for Each Query**

Gather resources from the specified platform based on predefined search queries, using the Time Horizon parameter to ensure that the resources are not outdated. For each search query, up to 10 resources are retrieved.

**Combine Resources (Eliminate Duplicates)**

Consolidate the retrieved resources for each query to remove any duplicates. This ensures that each piece of information is unique, streamlining the subsequent processing steps and avoiding redundancy.

**Separate Resources with Content from Without**

Filter out resources that lack substantial content, including video transcripts or site content. Only resources with content available proceed to the next stage.

**Add Summaries to Each Resource, Prioritizing Information Needed to Answer Specific Questions**

Summarize the content of each resource, prioritizing details that are crucial for answering the predefined specific questions.

**Add and Answer Specific Questions**

Address specific questions within each resource based on its content. This integration ensures that the content directly addresses the user’s specific questions.

**Separate Resources with Zero Answers**

Filter out resources that do not contribute any answers to the specific questions. This step refines the pool of useful information, ensuring that only relevant data is retained.

**Rank Resources by Number of Answers Provided**

Rank the remaining resources based on the number of questions they answer. This ranking helps identify the most comprehensive and informative sources.

**Separate Top Resources from the Rest**

Finally, separate the top-ranking resources from the rest. These top resources are the most valuable, providing the most answers and relevant information.

### Output

The output is structured hierarchically in YAML format, with the best resources organized by platform. Using YAML allows for easy viewing in text editors like VS Code, where the data can be seen as toggled lists, enabling quick search and navigation through the hierarchical information. An example output format is provided below:

```yaml
platform_name_1:
  title_1:
    url: "https://example.com/link_1"
    content: '''side content or youtube video transcript 
                or detailed summary 
                if the content was big for LLMs input'''
    summary: "summary"
    Q&A:
      question_1:
        'answer_1'
      question_2: 
        'answer_2'
  title_2:
    '...'
platform_name_2:
  '...'
etc: "..."  
```
This format ensures that the user can quickly access and understand the most relevant information, organized in a way that supports efficient learning and decision-making.

Additionally, for each run, a separate YAML file is generated to show the rejected data. This data is grouped by the reason for rejection, providing insight into why certain sources were excluded. 


### Why Not Just Use Products Like ChatGPT? 

By using the outlined approach, I achieve more predictable, stable, and reliable results. This method allows me to understand how the system filters and organizes information, as each LLM performs small and specific tasks. Unlike relying on a complex black box, this approach offers transparency and control. Moreover, I can simultaneously search a wide domain of knowledge in a hierarchical manner, enabling me to quickly see the context of the information. This comprehensive search helps me choose the proper sources to read, and if I don't find what I'm looking for, it likely means it doesn't exist.

### Source Code

The source code for the PoC, which utilizes Ollama with local LLMs, specifically Llama3:8b, can be found [here](https://github.com/MariuszJM/Web-Chaos-To-Order).

## Example Use Cases
The automated workflow for web information management with LLMs can significantly enhance learning, decision-making, and information retrieval. Here are some key use cases:

**Monitoring Changes in a Specific Domain**

Set the system to run regular searches with the same Time Horizon to track changes over time. For example, monthly searches on "AI advancements in healthcare" using a past month Time Horizon help monitor new developments and trends consistently.

**Identifying Reliable Sources for Specific Questions**

The workflow ranks resources based on the number of specific questions they answer, helping users find the most reliable and comprehensive sources quickly.

**Facilitating Structured Learning from General to Specific**

Organize learning by summarizing and addressing specific questions within each resource, allowing users to progress from broad concepts to detailed information. The search can be very wide, covering a broad range of topics and then narrowing down to specific details.

These use cases demonstrate the workflow’s ability to enhance information retrieval and learning efficiency.

## Conclusions

In the digital age, information overload is a significant challenge. This exploration highlights how Large Language Models (LLMs) can help manage this by filtering and organizing knowledge efficiently.

The brain's limited short-term memory and processing speed require structured, hierarchical learning. Clear goals and hierarchical organization reduce cognitive load and improve learning efficiency.

Setting clear, significant learning goals boosts motivation. Using the U-curve of dopamine and spaced repetition enhances long-term memory retention.

Addictive digital platforms and the rapid growth of content contribute to information overload. Effective filtering and prioritization are essential to manage this overload.

Automating information management with LLMs reduces cognitive burden and improves information quality. The developed workflow retrieves, filters, summarizes, and ranks information, providing a structured and transparent method.

The PoC shows LLMs can automate information management, ensuring relevant, high-quality resources. This structured approach offers stable and reliable outputs, enhancing decision-making and learning processes.

Leveraging LLMs helps individuals navigate the information overload, aligning with cognitive abilities and providing a scalable, efficient solution to the challenges of the digital age.

## References
1. Cognitive and neuroscientific perspectives of healthy ageing, Reuter-Lorenz, P. A., & Park, D. C. (2014). *Neuropsychology Review, 24*(3), 355-370. doi:10.1007/s11065-014-9270-9
    
2. Goal Striving, Need Satisfaction, and Longitudinal Well-Being: The Self-Concordance Model, Sheldon, K. M., & Elliot, A. J. (1999). *Journal of Personality and Social Psychology, 76*(3), 482-497.
    
3. The "What" and "Why" of Goal Pursuits: Human Needs and the Self-Determination of Behavior, Deci, E. L., & Ryan, R. M. (2000). *Psychological Inquiry, 11*(4), 227-268.
    
4. Choice Overload: A Conceptual Review and Meta-Analysis, Chernev, A., Bockenholt, U., & Goodman, J. (2015). *Journal of Consumer Psychology, 25*(2), 333-358. doi:10.1016/j.jcps.2014.08.002
    
5. Contextual Feature Extraction Hierarchies Converge in Large Language Models and the Brain, Schrimpf, M., Blank, I., Tuckute, G., Kauf, C., Hosseini, E. A., Kanwisher, N., Tenenbaum, J., & Fedorenko, E. (2021). *Proceedings of the National Academy of Sciences, 118*(45), e2021256118. doi:10.1073/pnas.2021256118
    
6. The Scrum Guide, Schwaber, K., & Sutherland, J. (2020). Scrum.org. Retrieved from https://www.scrum.org/resources/scrum-guide
    
7. The 12 Week Year: Get More Done in 12 Weeks than Others Do in 12 Months, Moran, B., & Lennington, M. (2013). Wiley.
    
8. Forgetting curve, Ebbinghaus, H. Teachers College, Columbia University. Retrieved from https://www.eng.auburn.edu/current-students/documents/forgetting-curve.pdf