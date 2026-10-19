CrewAI Build Report

Name: Soumith Rao Amradi
Discuss how AI can be applied in the healthcare sector.Talk about the healthcare industry's uses of AI.

 1. What I Changed

This assignment entailed editing the backstory of the Technical Writer agent found in the `crewai-kit/main.py`. Starter program had 3 agents: Research Analyst, Technical Writer, Editor. I maintained this structure and adjusted the instructions that lead the Writer by his/her writing style.

The new backstory portrays the Writer as a friendly science teacher teaching 10-year-old students complicated matters. It requests the agent to speak in simple terms that do not include jargon, short sentences, real-life illustrations, and definitions of technical terms.

I selected this modification because it contains some terms that may not be easily understood to people who may not have a technical background. I wanted to see if it would be easier to understand to change the audience by using an agent's backstory.

I used the same topic and maintained the research/writing/editing process for both runs. This helped me to compare the final products and to see if the changes in instructions had an effect on the explanation.

 2. How CrewAI Works

CrewAI is an AI workflow that revolves around agents, tasks, and a crew. An agent has a role, goal and backstory that provides structure and context for how the agent is to interpret the assigned work. A task is a statement of what work is to be done and what is expected. This crew unites the agents and tasks.

The Research Analyst is responsible for creating information on artificial intelligence applications in healthcare in this project. This information is from the language model's current knowledge, as the starter kit does not have access to the web. The Technical Writer uses the research product to create an explanation. The Editor then reviews the draft for clarity, organization, and claims which require supporting sources.

The program employs a sequential approach and tasks are executed in order within the program. Later task outputs draw on earlier task outputs to provide context, enable explanation to grow through research, writing and editing.

The change in my modification was to change the instructions that are fed to the Writer while keeping the sequence the same. The new backstory gave the model the opportunity to communicate to a younger audience. The final outcome was, however, also influenced by task instructions, and revision by the Editor. This can account for why there wasn't a complete absence of technical terms in the output, despite a change in one of the backstories.

 3. Evidence

I executed the original program with the "Applications of Artificial Intelligence in Healthcare" and the output of the terminal was stored as run1_original.txt and the output of the explanation in the file as explainer_run1.md.

I ran the program again with the same topic with the Writer's backstory changed. I saved run 2 as run2_changed.txt and explainer_run2.md.

The initial interpretation included topics like healthcare cost savings, regulatory issues, and disparities in healthcare data. The revised explanation started with a more general introduction to AI and structured the talk around various use cases, including diagnostic imaging, predictive risk evaluation and clinical decision support.

I used the comparison tool in VS Code, and the SHA256 hashes, to compare the files. The fact that the files were different was confirmed by using a number of different hashes, and reading the text enabled me to assess their nature. Without using hashes, they couldn't determine which of the two explanations was easier to understand or better-fitting for children.

I had to deal with empty language-model responses, also with model identification errors, related to the Groq integration, in the course of the work. I checked the configuration, the available models and tried to fine-tune the settings until the workflow finished.

A few of the more sophisticated terms were kept in the altered output. It was a significant constraint however: a different result does not automatically mean that the desired audience requirement was met. The differences could also be due to normal variation among student's responses to the model.

 4. Choosing a Framework

I would prefer to use CrewAI for a project that has well-defined tasks and can be broken down into a series of specialized agents. The structure is well suited for the research, writing and editing components in this assignment. There are dedicated agents for each purpose, making it easier to understand the instructions and where they should go, and which part of the workflow needs to be adjusted.

For instance, in the development of an educational explanation, one agent might be assigned to gathering background information, another to drafting the explanation for a specific audience, and another to editing the explanation for clarity and consistency. CrewAI offers an agent and task definition to accomplish this division easily.

In the class there is another framework called LangGraph. It has a node + edge structure, giving you a clear control of the workflow's transitions between stages. This would be helpful in conditional paths, reviews that are repeated or when the Writer returns a draft that has not passed an audience review.

In this task, there was a very simple sequence of tasks, which is why CrewAI was used. I can get more control if there is a repetition process but that would require specifying more clearly transitions and conditions. My comparison is just on the concept of the framework itself, not on a specific LangGraph.

 5. Verification and AI Use

I did some terminal output checking and made Markdown files to verify that both runs ran and were done on the same topic. I took the explainers in VS Code and checked that there are differences in the contents of the explainers with their SHA256 hashes.

Next, I read through the revised explanation of evidence of the desired writing style. There was some progress towards accessibility in its introduction, although technical healthcare jargon was used. So I didn't think that the audience requirement was fully met.

I also looked at claims which are labelled as [source needed]. These markers are used to tag statements that need to be checked, but not to state that they are true. As the starter kit is not web accessible, I did not test the accuracy of each healthcare statement, but rather judged the integrity and ease with which they could be read.

I used ChatGPT to aid in understanding the assignment, debugging Python and Groq configuration problems, editing the Writer's backstory, and to organize and edit this report. I ran some suggested technical steps and observed the output of the commands to make sure of their correctness. It was a powerful experience to learn that AI can aid development, but generate code and explanations still need human oversight.