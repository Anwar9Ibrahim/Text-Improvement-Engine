# Text-Improvement-Engine
Develop a tool that analyses a given text and suggests improvements based on the similarity to a list of "standardised" phrases. These standardised phrases represent the ideal way certain concepts should be articulated, and the tool should recommend changes to align the input text closer to these standards.
Requirements:
Data Input: Create a method for the user to input the text they wish to analyse. This could be through a simple UI or via a text file in CLI. The result should be shared as a link to GitHub project.

Standardised Phrases: Pre-load the tool with a list of standardised phrases (e.g., business jargon, scientific terminology, etc.).

Text Analysis: Use a pre-trained language model to find phrases in the input text that are semantically similar to any of the standardised phrases. Consider using techniques like cosine similarity with word embeddings. 

Suggestions: Provide a list of suggestions to replace phrases in the input text with their more "standard" versions. Each suggestion should show the original phrase, the recommended replacement, and the similarity score.

Documentation: Provide a README file detailing the setup process, technologies used, and rationale behind your design decisions.
This project should give you an opportunity to demonstrate a range of skills including text analysis, semantic similarity, and code quality, this should be doable within 4 hours.

Additional requirement: As part of the trial task, candidates will be required to submit a screen recording where they explain their code and the results achieved, along with the code itself. The recording can be shared via Loom, Google Drive or any other applicable method.

Sample “standardised phrases”:
1 Optimal performance
2 Utilise resources
3 Enhance productivity
4 Conduct an analysis
5 Maintain a high standard
6 Implement best practices
7 Ensure compliance
8 Streamline operations
9 Foster innovation
10 Drive growth
11 Leverage synergies
12 Demonstrate leadership
13 Exercise due diligence
14 Maximize stakeholder value
15 Prioritise tasks
16 Facilitate collaboration
17 Monitor performance metrics
18 Execute strategies
19 Gauge effectiveness
20 Champion change
Sample text to analyse:
In today's meeting, we discussed a variety of issues affecting our department. The weather was unusually sunny, a pleasant backdrop to our serious discussions. We came to the consensus that we need to do better in terms of performance. Sally brought doughnuts, which lightened the mood. It's important to make good use of what we have at our disposal. During the coffee break, we talked about the upcoming company picnic. We should aim to be more efficient and look for ways to be more creative in our daily tasks. Growth is essential for our future, but equally important is building strong relationships with our team members. As a reminder, the annual staff survey is due next Friday. Lastly, we agreed that we must take time to look over our plans carefully and consider all angles before moving forward. On a side note, David mentioned that his cat is recovering well from surgery."


