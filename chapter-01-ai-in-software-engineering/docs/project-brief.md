# EngCoach — Project Brief

**Status:** Approved

## Problem Hypothesis

TOEIC self-learners (both beginners and those who already have a foundation and want to improve their scores quickly) lack a focused practice tool that provides immediate scoring and clear explanations of mistakes, so they can self-assess and track their progress without needing classes or teachers.

## Primary User

General TOEIC self-learners — regardless of whether they are beginners or already have a foundation. (Assumption: both groups use the same experience flow in the MVP, without personalization based on proficiency level.)

## Desired Outcome

Users practice regularly, clearly see where they made mistakes and why, and see their scores/progress improve over time.

## In-Scope Behavior (MVP)

* Register / log in to an account (store data separately for each user).
* Practice 2 skills: Reading and Listening.
* Two practice formats:

  * Practice by individual question types (according to each TOEIC Part).
  * Take a full mock test (200 questions, with a time limit).
* Submit the test → grading:

  * Automatically compare answers (multiple-choice).
  * AI provides detailed explanations for each incorrect answer.
* View progress: score history + progress chart over time.

## Exclusions (not included in the first version)

* Speaking, Writing practice.
* Group classes, manual grading by teachers.
* Payment / paid packages.
* Separate mobile application (web only).
* AI-personalized learning path (adaptive learning) — for a later version.

## Constraints

* Academic project, team of 2–3 people, developed according to the weekly/chapter-based progress of the course.
* No specific technology is required — a suitable stack will be proposed in Chapter 5 (Architecture).
* Timeline: according to the course schedule.

## AI Working Rules

* AI supports each stage (requirements, design, coding, testing, docs) according to the course's required prompt templates.
* All scope/product decisions must be explicitly approved by the team before being saved as official documentation.
* Do not independently add features outside the approved scope.

## Decision Log

| Decision          | Selected                                                     |
| ----------------- | ------------------------------------------------------------ |
| Target Exam       | TOEIC                                                        |
| MVP Skills        | Reading & Listening                                          |
| Scoring Method    | Automatic + AI explanations                                  |
| Primary User      | General for beginners & learners with an existing foundation |
| Practice Format   | Both individual section practice + full mock tests           |
| Progress Tracking | Yes (history + chart)                                        |
| Account           | Registration/login required                                  |
| Stack             | Not finalized, to be proposed in Chapter 5                   |
| Team Size         | 2–3 people                                                   |

## Open Assumptions (require further team confirmation)

* Where will the TOEIC question bank come from (self-created, existing dataset, or AI-generated questions)?
* Is there a limit on the number of times one test can be taken?
* Is a feature for sharing scores/results with others required?
