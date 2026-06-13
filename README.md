# AI Job Application Optimizer

> An AI-powered career assistant built with Amazon PartyRock that transforms a Job Description and Candidate Profile into an ATS-optimized Resume, Personalized Cover Letter, Skill Gap Analysis, and Interview Preparation Plan.

---

## The Motivation

Every job application is unique, but the process of tailoring resumes, writing cover letters, identifying skill gaps, and preparing for interviews is often repetitive and time-consuming.

Students and early-career professionals frequently apply to dozens of opportunities using generic resumes and cover letters. Despite possessing relevant skills and projects, many applications fail to effectively communicate the candidate's strengths or pass Applicant Tracking Systems (ATS).

I wanted to explore how Generative AI could make this process smarter, more personalized, and significantly faster—not by replacing human effort, but by augmenting it with structured AI workflows.

This led to the creation of **AI Job Application Optimizer**, an end-to-end AI-powered career assistant built using Amazon PartyRock.

---

## What the Application Does

The application accepts two simple inputs:

- **Job Description**
- **Candidate Profile**

Using these inputs, it generates four recruiter-ready outputs:

### ATS-Optimized Resume

Generates a resume tailored specifically to the provided job description by:

- Aligning with ATS keywords
- Improving structure and readability
- Highlighting relevant experiences and projects
- Preserving factual accuracy by using only user-provided information

---

### Skill Match & Gap Analysis

Provides a structured comparison between the candidate profile and the target role.

The analysis includes:

- Matching skills
- Missing skills
- Priority skills to learn
- Improvement recommendations
- Suggested projects to bridge skill gaps

---

### Personalized Cover Letter

Creates a professional cover letter that:

- Aligns with the target role
- Highlights relevant strengths
- Demonstrates role-candidate fit
- Maintains a confident and recruiter-friendly tone

---

### Interview Preparation Plan

Generates a structured preparation roadmap including:

- Technical interview questions
- HR interview questions
- Important topics to study
- A practical 7-day preparation plan

---

## System Design

```text
                     ┌────────────────────┐
                     │ Job Description    │
                     └─────────┬──────────┘
                               │
                               │
                     ┌─────────▼──────────┐
                     │ Candidate Profile  │
                     └─────────┬──────────┘
                               │
         ┌─────────────────────┼─────────────────────┐
         │                     │                     │
         ▼                     ▼                     ▼
┌────────────────┐   ┌────────────────┐   ┌────────────────┐
│ ATS Resume     │   │ Skill Match &  │   │ Cover Letter   │
│ Generator      │   │ Gap Analysis   │   │ Generator      │
└────────────────┘   └────────────────┘   └────────────────┘
                               │
                               ▼
                    ┌───────────────────┐
                    │ Interview Prep    │
                    │ Planner           │
                    └───────────────────┘
```

---

## Prompt Engineering Principles

A major focus of this project was designing prompts that produce:

- Structured and reusable outputs
- ATS-friendly formatting
- Grounded responses without hallucinations
- Role-specific personalization
- Professional and recruiter-friendly tone

Each AI workflow is backed by dedicated prompts that are documented in the `prompts/` directory.

---

## About Amazon PartyRock

Amazon PartyRock is a no-code generative AI platform built on Amazon Bedrock that allows users to build AI applications using prompts and widgets without writing code.

In this project, PartyRock is used to design structured prompt workflows that generate ATS resumes, cover letters, skill-gap analysis, and interview preparation plans from job descriptions and candidate profiles.

---

## Technologies Used

- Amazon PartyRock
- Amazon Bedrock
- Generative AI
- Prompt Engineering

---

## Outcomes

This project demonstrates how Generative AI can be integrated into real-world career workflows to create meaningful user experiences.

The final application is capable of:

- Producing ATS-optimized resumes in seconds
- Generating personalized cover letters for different roles
- Automatically identifying strengths and skill gaps
- Creating structured interview preparation plans
- Delivering consistent, professional outputs through reusable AI workflows

More importantly, it showcases practical experience in:

- Prompt Engineering
- AI Workflow Design
- Human-AI Collaboration
- Career-focused AI Applications
- Building products with Amazon PartyRock

---

## Live Demo

**PartyRock App**

https://partyrock.aws/u/nataraj-el/AYm8pF8To/AI-Job-Application-Optimizer

---

## Repository Structure

```text
partyrock-ai-job-application-assistant
│
├── README.md
│
├── screenshots/
│   ├── app-overview.png
│   ├── ats-resume-output.png
│   ├── skill-match-report.png
│   ├── cover-letter-output.png
│   └── interview-prep-plan.png
│
├── prompts/
│   ├── ats_resume_prompt.md
│   ├── skill_match_prompt.md
│   ├── cover_letter_prompt.md
│   └── interview_prep_prompt.md
│
└── assets/
    └── architecture.png
```

---

## Reflections

Building this project reinforced an important idea: AI becomes significantly more valuable when it is designed around real user workflows rather than isolated prompts.

By grounding the model on user-provided information and structuring outputs around practical career needs, the application delivers trustworthy, repeatable, and highly personalized results—demonstrating how Generative AI can meaningfully enhance everyday decision-making and productivity.
