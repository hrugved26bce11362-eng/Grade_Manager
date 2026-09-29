# Project Statement: Student Grade Manager

**Course:** CSE1021  
**Student:** Hrugved Sharad Rathod (26BCE11362)  
**Faculty Mentor:** Dr. Poonkuntran S.  
**Institution:** VIT Bhopal University

---

## 1. Problem Statement

Recording student marks on paper or in an unstructured list makes it slow to calculate averages, find the best and weakest performers, or correct mistakes. Errors such as duplicate entries, blank input or non-numeric marks also go unnoticed.

This project provides a simple console application in Python that stores each student's marks under their name and offers the common grade-book operations through a numbered menu. It rejects invalid input with a clear message instead of crashing.

## 2. Scope of the Project

**In scope**

- A menu-driven command-line program written in Python 3 using only built-in features.
- Adding, viewing, updating and removing students and their marks.
- Calculating each student's average and identifying the topper and the lowest scorer.
- Input validation for empty names, duplicate names, empty marks, non-numeric marks and invalid menu choices.

**Out of scope**

- Permanent storage (data is kept in memory and lost when the program exits).
- Graphical or web interface.
- Subject-wise marks, letter grades and user accounts.

## 3. Target Users

- **Teachers and tutors** who need a quick way to track marks for a small class.
- **Students** who want to record and compare their own scores.
- **Beginners in Python** who want a small, readable example of functions, dictionaries, lists, loops and error handling.

## 4. High-Level Features

| # | Feature | Description |
|---|---------|-------------|
| 1 | Add student | Store a unique student name with one or more integer marks. |
| 2 | View all students | List every student with their marks and average (two decimal places). |
| 3 | Find topper | Show the student with the highest average. |
| 4 | Find lowest scorer | Show the student with the lowest average. |
| 5 | Update marks | Replace the marks of an existing student. |
| 6 | Remove student | Delete a student from the system. |
| 7 | Exit | Leave the program from the main menu. |

## 5. Technical Overview

- **Language:** Python 3 (no external libraries)
- **Interface:** Console, menu driven
- **Data structure:** a dictionary mapping each student name to a list of integer marks
- **Main file:** `student_grade_manager.py`

## 6. Expected Outcome

A reliable, easy-to-read program that lets a user manage a small set of student marks from the terminal, handles every kind of invalid input gracefully, and reports averages, the topper and the lowest scorer accurately.

## 7. How to Run

```bash
python student_grade_manager.py
```
