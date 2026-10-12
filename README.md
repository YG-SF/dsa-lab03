# Lab 3

This assessment contains materials that may be subject to copyright and other intellectual property rights.

Modification, distribution, or reposting of this document is strictly prohibited. Learners found reposting this document or its solutions anywhere will be subject to the college's Academic Integrity policy.

## Due: Sunday, October 11, 2026, 11:59 PM

## Objectives

* Practice analyzing recursive functions.
* Practice implementing a non-sentinel doubly linked list.
* Continue using the DSA301 Classroom 50 / GitHub submission workflow.

## Before You Start

Lab 0 introduced the Classroom 50 / GitHub workflow used throughout this course.

If you are not comfortable accepting an assignment, using Codespaces, testing locally, committing/pushing with Git, or using the final `complete` tag, review Lab 0 before continuing.

## Setup

1. Open the **Lab 3** entry in `dsa301-main`.
2. Click the **Accept Lab 3 in Classroom 50** link.
3. Accept the assignment.
4. Classroom 50 will create a **private Lab 3 repository for your GitHub account**.
5. Work only in your own generated repository.

Your repository name will look similar to:

```text
dsa301-lab-03-your-github-username
```

You should see starter files including:

```text
README.md
.gitignore
lab3.md
lab3.py
test_lab3.py
```

Classroom 50 may also add control/workflow files such as `.classroom50.yaml` and files under `.github/`.

> **Important:** Do not work in `dsa301-main` or in `dsa301-lab-03-template`. Your work belongs in your personal private Lab 3 repository.

## Resources

You may find this course resource useful:

* [Analysis of recursive functions](https://seneca-ictoer.github.io/data-structures-and-algorithms/C-Recursion/analysis-of-recursive-functions)

## Part A - Recursive Analysis

Write all Part A answers in the provided `lab3.md` file.

Complete the analyses for **all three recursive functions** in `lab3.md` using the recursive-analysis process from the course notes.

## Part B - Programming

Implement the required functions for the **non-sentinel doubly linked list** in `lab3.py`.

Do not change the required public class or method names/signatures.

### `DoublyLinked.Node`

The `Node` class is declared inside `DoublyLinked`.

A node stores:

* a data value;
* a reference to the next node; and
* a reference to the previous node.

Its constructor is:

```python
def __init__(self, data, next=None, prev=None)
```

`data` is required. `next` and `prev` are optional and default to `None`.

Implement:

```python
def get_data(self)
```

Returns the data stored in the node.

```python
def get_next(self)
```

Returns the reference to the next node.

```python
def get_previous(self)
```

Returns the reference to the previous node.

### `DoublyLinked`

The constructor is:

```python
def __init__(self)
```

`DoublyLinked()` creates an empty list for which both `get_front()` and `get_back()` return `None`.

Implement the following methods.

#### `get_front`

```python
def get_front(self)
```

Returns a reference to the first data node in the list. If the list is empty, returns `None`.

#### `get_back`

```python
def get_back(self)
```

Returns a reference to the last data node in the list. If the list is empty, returns `None`.

#### `push_front`

```python
def push_front(self, data)
```

Adds `data` to the front of the list. Returns nothing.

#### `push_back`

```python
def push_back(self, data)
```

Adds `data` to the back of the list. Returns nothing.

#### `pop_front`

```python
def pop_front(self)
```

Removes the first data node and returns the value stored in that node.

If called on an empty list, raise:

```python
raise IndexError("pop_front() used on empty list")
```

#### `pop_back`

```python
def pop_back(self)
```

Removes the last data node and returns the value stored in that node.

If called on an empty list, raise:

```python
raise IndexError("pop_back() used on empty list")
```

## Part C - Reflection

Write your reflection answers in `lab3.md`.

The synchronized reflection includes:

1. your approach to writing recursive functions;
2. recursive-analysis vs. non-recursive-analysis; and
3. what you learned while implementing the doubly linked list, including difficult bugs/reference issues.

## Testing Your Lab

Before requesting Classroom 50 grading, test Part B **locally**.

### Codespaces / macOS / Linux

```bash
python3 test_lab3.py
```

### Windows

```bash
python test_lab3.py
```

If `python` is not recognized on Windows, try:

```bash
py test_lab3.py
```

Fix any errors or failed tests and run the tester again.

> The supplied tester checks the required linked-list behavior. Your instructor will still review Part A and Part C manually.

> **Grading note:** `test_lab3.py` is provided so you can test locally. Classroom 50 grades your submitted code using an **authoritative instructor-side copy of the same public linked-list tests**. Editing the tester in your repository does not change the Classroom 50 test used for grading.

## Saving Your Work to GitHub

Commit and push regularly.

For example:

```bash
git status
git add .
git commit -m "Work on Lab 3"
git push origin main
```

A normal push saves your work to GitHub but does **not** request Classroom 50 grading.

## Submitting Your Lab for Grading

Lab 3 uses a **tagged submission**.

### Optional preliminary check

Because the tester is available locally, use Classroom 50 grading sparingly.

If you have tested locally but still need to verify the Classroom 50 grading workflow, you may make **one optional preliminary attempt**:

```bash
git push origin main

git tag submit/check-1
git push origin submit/check-1
```

Do not delete, move, recreate, or force-update this tag.

### Final submission

When:

* all three Part A analyses are complete;
* Part B passes `test_lab3.py`;
* Part C is complete; and
* your latest work is committed and pushed to `main`;

submit your final commit using:

```text
complete
```

Recommended sequence:

```bash
git status
git add .
git commit -m "Complete Lab 3"
git push origin main

git tag complete
git push origin complete
```

If Git reports that there is nothing new to commit, that is fine. Make sure the commit you want graded is already pushed to `main`.

> **`complete` means final.** After pushing `complete`, do not push another grading tag unless your instructor explicitly asks you to resubmit.

If you accidentally push `complete` too early, do not delete or move the tag yourself. Contact your instructor.

## Checking Your Classroom 50 Submission

After pushing a grading tag:

1. Open your Lab 3 repository on GitHub.
2. Open the **Actions** tab.
3. Confirm that the Classroom 50 autograding workflow runs.
4. Review the automated result.
5. You may also see the result in Classroom 50 after scores synchronize.

For Lab 3, the Classroom 50 automated test is **all-or-nothing and worth 1 automated point**:

* all supplied linked-list tests pass → **1/1**;
* any required test fails → **0/1**.

The Classroom 50 score is **not automatically your final Lab 3 grade**. It verifies Part B behavior only. Your instructor will also assess the required analysis and reflection.

## Submitting the Repository Link on Blackboard

After the final `complete` submission has run, submit the URL of **your own Lab 3 repository** to the Lab 3 submission area on Blackboard.

The link should look similar to:

```text
https://github.com/seneca-dsa301-2026/dsa301-lab-03-your-github-username
```

Do **not** submit a link to:

* `dsa301-main`;
* the Lab 3 template repository; or
* another student's repository.

> Submitting the repository URL on Blackboard does **not** trigger Classroom 50 grading. The `complete` tag identifies your final submitted commit. Blackboard provides the official hand-in record and the direct repository link used by your instructor while marking.

## Repository Requirements

* Do not rename or remove the provided starter files.
* Do not create a separate public repository for your lab work.
* Do not modify `.classroom50.yaml` or files under `.github/`.
* Do not alter the supplied tester.
* Commit and push regularly.
* Do not force-update grading tags.

## Lab Rubric

| Criteria | Poor - 0 marks | Fair - 1 mark | Good - 2 marks |
|---|---|---|---|
| Lab Completion | Part A or Part B is incomplete | Coding is complete but analysis/reflection is missing or weak, OR coding is incomplete but the analysis/reflection portions are complete | Coding, all three analyses, and reflection are complete |
