##                **Daily Reflection Tree — Design Write-up**

                                                                                        Author name : Nisha Manuskare

## **1\. Overview**

This assignment focuses on designing a deterministic reflection system that helps an employee review their day in a structured and meaningful way. Instead of using an LLM at runtime, I built a decision-tree-based system that ensures consistency, clarity, and auditability.

The goal of the system is not to judge the employee, but to guide them toward self-awareness across three psychological axes:

* **Locus (Victim vs Victor)**  
* **Orientation (Entitlement vs Contribution)**  
* **Radius (Self vs Others)**

The tree acts as a structured conversation that helps users recognize patterns in how they think, act, and respond.

---

## **2\. Design Approach**

I approached this problem by thinking of the experience as a **guided evening reflection**, not a survey.

Each axis follows a similar structure:

1. A broad opening question to anchor the user in their day  
2. A decision node to split paths based on responses  
3. A deeper follow-up question  
4. A reflection that reframes their behavior  
5. A final question to reinforce awareness  
6. A bridge to the next axis

This creates a **natural conversational flow**, where each step builds on the previous one.

---

## **3\. Question Design**

The most important part of the system is the **questions and answer options**.

I focused on:

* Making options **realistic and relatable** (how people actually think at the end of a workday)  
* Avoiding obvious “good vs bad” answers  
* Ensuring each option clearly maps to a psychological signal

For example:

* Instead of asking “Did you take responsibility?”, I asked:  
   *“When something didn’t go as planned, what did you do first?”*

This makes the reflection feel natural rather than evaluative.

---

## **4\. Branching Logic**

The tree uses **decision nodes** to route the user into different paths.

Each decision:

* Maps answers to a specific branch  
* Ensures deterministic behavior (same input → same output)  
* Avoids ambiguity or interpretation

For example:

* Internal locus responses → reflection reinforcing agency  
* External locus responses → reflection gently reintroducing choice

This allows the system to adapt without using any AI at runtime.

---

## **5\. Psychological Foundations**

The tree is grounded in established psychological concepts:

* **Locus of Control (Julian Rotter)**  
   Used to identify whether the user attributes outcomes to themselves or external factors.  
* **Growth Mindset (Carol Dweck)**  
   Reflected in questions that emphasize adaptability and learning.  
* **Psychological Entitlement vs Contribution**  
   Captured through how users interpret effort, recognition, and responsibility.  
* **Self-Transcendence (Maslow)**  
   Used in Axis 3 to expand the user’s focus beyond themselves toward team and impact.

These frameworks guided both the structure and tone of the reflection.

---

## **6\. Tone and Reflection Design**

A key design goal was to **avoid moralizing**.

Reflections are written to:

* Acknowledge the user’s experience  
* Introduce a broader perspective  
* Encourage awareness without judgment

For example:  
 Instead of saying *“You should take more responsibility”*,  
 the system says:  
 *“There were moments where your response still mattered.”*

This keeps the tone supportive and realistic.

---

## **7\. Trade-offs**

Some trade-offs I made:

* **Simplicity vs Depth**  
   I limited the number of questions per axis to keep the experience short and usable daily.  
* **Determinism vs Personalization**  
   Without LLMs, personalization is limited, so I used branching and interpolation instead.  
* **Clarity vs Coverage**  
   I prioritized clear, understandable options over covering every possible scenario.

---

## **8\. What I Would Improve**

With more time, I would:

* Add **dynamic summary interpolation** using stored answers  
* Introduce **signal-based summaries** (e.g., dominant axis detection)  
* Expand each axis with additional nuanced branches  
* Build a **simple UI or CLI agent** to demonstrate the flow

---

## **9\. Conclusion**

This exercise demonstrates how psychological frameworks can be translated into a **deterministic, structured system**.

The final tree is:

* Predictable and auditable  
* Human-centered in tone  
* Structured for consistent daily use

It reflects the idea that meaningful insights can be delivered not through AI generation, but through well-designed decision structures.

