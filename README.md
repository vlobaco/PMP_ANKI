This project aims at transforming the OCR questions at the end of each chapter of `PMP ExamPrep Simplified`, Andrew Ramdayal, into a csv file that can be imported into [Anki](ttps://apps.ankiweb.net/).

The data is split into two files:
- **data/answers_<chapter>.txt**. The answers are represented with one letter, using upper case, without any spaces between them.

```text
AABACDBABAAAACBDACADD
````

- **data/question_<chaper>.txt**. Each question is identified by a question number followed by a point. Each question is followed by 4 possible options. Each option marked with a letter (A-D), followed by a point.

```text
3.	You are a project manager overseeing a web-based automation project in a weak matrix organization. You are playing the role of a communication coordinator with little power to make decisions and sometimes report to a high-level manager. Your role can be defined as a:
A.	Team lead
B.	Project coordinator
C.	Lead coordinator
D.	Project expeditor
````
Because the questions have been OCR, special care should be placed into checking the format is correct. These restrictions involves:
- **R1**: checking that the number of questions and answers are the same
- **R2**: the sequence of the questions (1, 2, 3, ...) is maintained
- **R3**: the sequence of the answers (A, B, C, D) is maintained
- **R4**: each question has four options, and just four

It should be remembered that each component takes exactly a line. Each question is separated from the next by an blank line. 