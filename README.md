# Program Transfer Planner

## Description
This project is a web application that helps students plan transferring from one academic program to another.

It shows which completed courses can be matched with courses in a new program.

## Features
- Displays all courses and their status
- Dropdown to select target program
- Transfer button generates equivalency table

## Equivalency Algorithm

The program uses simple keyword matching:

- "Math" → Engineering Mathematics
- "Physics" → Applied Physics
- "Programming" → Intro to Programming
- "Data Structures" → Data Structures
- "AI / Machine Learning" → Same course

If no match is found, it returns "N/A".

## Improvement Plan (Future Work)

### Automatic Syllabus Comparison

In the future, AI can improve this system.

### Steps:
1. Load course syllabi of both programs
2. Convert text into vectors using NLP
3. Compare similarity between courses
4. Match courses with highest similarity

### AI Techniques:
- Natural Language Processing (NLP)
- Sentence embeddings
- Cosine similarity

This would make course matching accurate and automatic.