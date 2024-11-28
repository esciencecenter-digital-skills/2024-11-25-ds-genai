![](https://i.imgur.com/iywjz8s.png)

# 2024-11-25 AI-assisted Coding with Codeium

Welcome to "AI-assisted Coding with Codeium" Collaborative Document.

This Document is synchronized as you type, so that everyone viewing this page sees the same text. This allows you to collaborate seamlessly on documents.

----------------------------------------------------------------------------

##  🫱🏽‍🫲🏻 Code of Conduct

Participants are expected to follow these guidelines:
* Use welcoming and inclusive language.
* Be respectful of different viewpoints and experiences.
* Gracefully accept constructive criticism.
* Focus on what is best for the community.
* Show courtesy and respect towards other community members.
 
## ⚖️ License

All content is publicly available under the Creative Commons Attribution License: [creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/).

## 🙋Getting help

To ask a question, just raise your hand.

If you need help from a helper, place a pink post-it note on your laptop lid. A helper will come to assist you as soon as possible.

## 🖥 Workshop website

[link](https://esciencecenter-digital-skills.github.io/2024-11-25-ds-genai/)

🛠 Setup

[link](https://olgaminaeva.github.io/gen-ai-coding/)

## 🗓️ Agenda
|  Time | Topic                                |
| -----:|:------------------------------------ |
| 11:00 | Welcome and icebreaker               |
| 11:15 | Introduction to AI coding assistants |
| 11:45 | Setup                                |
| 12:00 | Lunch break                          |
| 13:00 | Code generation and optimization     |
| 14:15 | Coffee break                         |
| 14:30 | Ethical and security considerations  |
| 15:00 | END                                  |

## 🏢 Location logistics
* Coffee and toilets are in the hallway, just outside of the classroom.
* If you leave the building, 
  be sure to be accompanied by someone from the escience center to let you back in through the groundfloor door
* For access to this floor you might need to ring the doorbell so someone can let you in
* In case of an emergency, you can exit our floor using the main staircase.
  Or follow green light signs at the ceiling to the emergency staircase.
* **Wifi**: Eduroam should work. Otherwise use the 'matrixbuilding' network, password should be printed out and available somewhere in the room.

## 🎓 Certificate of attendance
If you attend the full workshop you can request a certificate of attendance by emailing to training@esciencecenter.nl.
Please request your certificate within 8 months after the workshop, as we will delete all personal identifyable information after this period.

## 🔧 Exercises

## 🧠 Collaborative Notes

### Introduction to AI coding assistants 

#### What is GenAI?
- AI > Machine Learning > Deep Learning > Generative AI
- All of the above also have overlap with Natural Language Processing, especially coding assistants

#### AI Coding assissants
- Trained on public code and documentation to understand paterns/syntax/code logic
- Data collection -> Model architecture design -> Pre-training -> Fine tuning -> evaluation and iteration
- New genAIs can be trained from foundation models rather than having to be trained from scratch

#### Context Awareness: Retrieval-Augmented-Generation
- Pretrained model does not only rely on foundation model/training data, but also on external knowledge
- Useful in domain specific applications
- RAG can be fine-tuned without retraining

#### AI coding assisants rely on ML techniques:
- Trained on public code
- Context awareness (RAG)
- NLP to interpret natural language
- Learning from user interaction
- Code generation and refactoring
- Multilanguage support (programming languages)

#### Areas of application
- Intelligent code completion
- Real-time error detection
- Code refactoring suggestions
- Automated documentation generation
- Code and error explanation
- Collaboration enhancement

#### Challenges
- Balancing accuracy vs speed
- Adaptability to different coding styles
- Ensuring user privacy and security
- Limited context awareness
- Unclear AI behavior

#### AI coding assistant options
- Many choices, some well known ones:
    - GitHub Copilot
    - Codeium
    - Amazon Q Developer
    - Tabnine
    - Hugging Chat
    - Cline
- See table for details and differences (link will be added to resources below)

### Codeium AI introduction

#### Testing Codeium installation in VSCode
- Do you see the curly brackets symbol in your VS Code IDE?
- Can you interact with it?
- Do you see that the extension is enabled?

#### 3 Modes
- Command: generate new code/edit existing code
- Chat: ask a question, get an answer, ask for clarification, etc. Basically have a conversation with the AI
- Autocomplete: suggestions while you type

#### What can you do with this?
- Generate new code
- Optimize/refactor existing code
- Identify/fix bugs

#### Command mode
- Enter a prompt (using CMD/Crl + I): open a prompt box
    - you can select a specific piece of code so that codeium has some specific context about which piece of code
- No dialog possible, just accept or reject
- Code lenses: VS code shows gray text refactor/docstring/explain near a function/class/..., which you can click to produce that specific action
- Best practices:
    - advanced model running command
    - highlight a specific text
    - give clear and detailed prompts, dont expect the AI to read your mind. Machines cannot interpret it as well as humans
    - always review AI-generated code

#### Chat mode
- More conversational function
- mentiones: use `@` to refer to specific functions, files, etc.
    - Chat retains context of the files you have open, but you can add files to the context using mentions
- Best practices:
    - Dont exceed context length
    - There's no "counter", so don't ask to count "how often ..."
    - Don't assume up-to-date knowledge: models have been trained some time ago
    - Don't ask self-reflective questions: codeium is not aware of itself.

#### Autocomplete
- Simpler model than other two
- Goal is "boilerplate code", repetitive functions, code formatting/styling, etc.
- Fill-in-the-middle functionality: it will look above and below
    - e.g. it will also look at the code to auto-complete the docstring
- Best practices:
    - Use declarative code instead of giving instructions (instructions are more for other modes)
    - Use good variable/class/etc naming as well as type hints (in Python), this helps the autocomplete function understand what you want to do (also future developers)
    - Be explicit about what you want

### Using Codeium
- create a virtual environment

```bash=
pip install virtualenv
python3 -m venv .venv
pip install -r https://raw.githubusercontent.com/olgaminaeva/gen-ai-coding/refs/heads/main/learners/files/requirements.txt
```

### Ethical and security considerations

#### Ethical considerations
- AI-generated content is based on a biased input data set (e.g. US/Western Europe centric)
- Black-box results, there is no way to look under the hood to see how the result was generated and/or whether there is any malicious things
- Environental costs: GenAI costs A LOT of energy/CO2 and (cooling) water to support

#### Best practices of using GenAI
- Be vigilant of results
- Acknowledge/cite usage of genAI
- Check for your institute's/journal/EU regulations regarding genAI in research

#### Data security
- Don't put sensitive information on public AIs
- Local GenAIs also exist
- Be aware of malicious/mis-trained code that can be injected into models
- Don't assume all generated code is secure

#### Security measures
- Acces control/data encryption: avoid your data/code landing on some public server
- Continuous monitoring and updating: regular security fixes are published by providers as issues become flagged
- Collaborative oversight/code reviewing to have an extra set of eyes checking your code

## Exercises

#### Hands on 1 - Code Generation

Prompt codeium:

```
Load a [CO2 concentration dataset](https://datahub.io/core/co2-ppm/) from the file `co2-mm-mlo.csv` into a Pandas DataFrame, then generate descriptive statistics and visualize data distributions. Read the dataset using the following URL: https://edu.nl/k6v7x.

1.  Write a function that takes a DataFrame as input and calculates key descriptive statistics, including:

   - Number of rows and columns
   - Data types of each column
   - Summary statistics (e.g., mean, minimum, maximum)

   Compute the statistics only for the numeric columns.

2. Write a function that accepts a DataFrame and a specific column as inputs, and creates a new figure in which it plots its distribution. If the column is numeric (e.g., `int64`, `float64`), create a histogram to display its distribution; if categorical, create a bar plot to show category frequencies. Add the name of the column to the title.

3. Write a function that creates a new figure in which it plots the `Average` and `Interpolated` columns on a single graph, with `Date` on the x-axis, to visualize their distributions over time. 

4. In the main, print nicely the information computed in 1., run the function defined in 2. on all columns, and run the function defined in 3. Use the `show()` functionality to display the figures only at the end of the main. 
```

#### Exercise - Bug Fixing (5 min)

Look back at the code generated during the “Code Generation” section. If you look at the head of the DataFrame, what do you notice? Use the Chat feature to discuss the issue with Codeium and ask for suggestions on how to resolve it. Then run again the functions defined in the previous exercise to see if the issue has been resolved.

### Exercise - AI Coding Assistant Ethics Challenge (15 min)

You're leading a team that's considering adopting an AI coding assistant for a new project involving sensitive user data. Your task is to create a comprehensive plan that addresses the ethical and security concerns discussed in the lesson.

1. List at least two potential risks or vulnerabilities that could arise from using an AI coding assistant in this project.

2. For each risk identified, propose a specific mitigation strategy. Explain how this strategy addresses the risk and aligns with the best practices discussed in the lesson.

3. Draft a set of at least 5 ethical guidelines for your team to follow when using the AI coding assistant. These should cover areas such as bias prevention, code review processes, and data privacy.

4. Outline a security protocol that includes at least three specific measures to protect sensitive data and ensure the integrity of the AI-assisted development process.

5. Design a collaborative code review process that leverages the strengths of both human developers and the AI assistant while mitigating potential risks.

## 📚 Resources

- [Codeium documentation](https://help.codeium.com/hc/en-us)
- [Prompting guide 101: A quick-start handbook for effective prompts](https://services.google.com/fh/files/misc/gemini-for-google-workspace-prompting-guide-101.pdf)
