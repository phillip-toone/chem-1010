# CHEM 1010 --- Course Reconstruction Workflow

> **Purpose:** Provide a repeatable human + LLM workflow for
> reverse-engineering, documenting, and maintaining the inherited CHEM
> 1010 course.\
> **Scope:** Course reconstruction and documentation process, not
> chemistry content or semester policy.\
> **Primary use:** Resume this work consistently in a new LLM chat
> without depending on prior conversation history.\
> **Status:** Working process document; revise when the reconstruction
> method itself improves.

------------------------------------------------------------------------

## 1. Why This Document Exists

`COURSE-GUIDE.md` explains **how CHEM 1010 is designed to work as an
instructional system**.

This file explains something different:

> **How do we systematically reconstruct the inherited course from
> Canvas, Critical Chemistry, review materials, assessments, and related
> artifacts, then turn that evidence into useful instructor
> documentation?**

The reconstruction process should be reproducible. Important decisions
should not exist only in a long chat history or in one instructor's
memory.

The goal is to transform a collection of Canvas objects and external
resources into a documented hierarchy:

``` text
course architecture
        ↓
semester pacing
        ↓
unit conceptual roadmap
        ↓
section teaching roadmap
        ↓
source evidence
```

------------------------------------------------------------------------

## 2. Core Principle: Evidence Before Synthesis

Do not begin by writing what a generic introductory chemistry course
*should* contain.

Begin with what this inherited CHEM 1010 course actually contains.

The basic workflow is:

``` text
COLLECT
   ↓
COMPARE
   ↓
SYNTHESIZE
   ↓
REVIEW
   ↓
COMMIT
   ↓
MOVE TO NEXT SECTION
```

During collection, resist the temptation to prematurely impose a
narrative on the section.

The narrative should emerge from the evidence.

------------------------------------------------------------------------

## 3. Evidence Labels

Use the same evidence discipline throughout the reconstruction.

### DOCUMENTED

Directly established by supplied course evidence, such as:

-   Canvas learning outcomes;
-   assignment instructions;
-   quiz questions;
-   rubrics;
-   syllabus language;
-   calendar entries;
-   Critical Chemistry assignment descriptions;
-   supplied review PDFs;
-   other authoritative course artifacts.

### INFERRED

A conclusion strongly supported by relationships among multiple
artifacts but not explicitly stated as course policy or instructional
intent.

Example:

> The periodic-table lesson appears intended to prepare students to
> explain periodic patterns using electron configuration.

### INSTRUCTOR PRACTICE

A proposed implementation decision that may be pedagogically useful but
is not established by the inherited course.

Examples:

-   a proposed Tuesday/Thursday lecture sequence;
-   a particular classroom demonstration;
-   a recommended problem-solving routine;
-   a suggested conceptual question for organizing a lecture.

### KNOWN UNKNOWN

A question the collected evidence does not yet answer.

Examples:

-   which reference materials are provided on a particular assessment;
-   how strongly a unit's case-study context is used in face-to-face
    instruction;
-   whether a particular section has canonical demonstrations or
    face-to-face activities intended by the original course developer.

### Rule

> **Never silently turn generic chemistry knowledge, an inference, or an
> instructor preference into a documented course requirement.**

When evidence is incomplete, preserve the uncertainty.

------------------------------------------------------------------------

## 4. Source-of-Truth Discipline

When sources disagree, use the current course sources before
reconstructed documentation.

A useful working hierarchy is:

1.  current institutional requirements and official policies;
2.  current course syllabus;
3.  current Canvas modules, assignments, rubrics, quizzes, and
    instructor announcements;
4.  current semester Canvas calendar;
5.  supplied Critical Chemistry / review / linked course resources;
6.  reconstructed unit and section roadmaps;
7.  `COURSE-GUIDE.md`;
8.  prior-semester materials;
9.  LLM inference or generic chemistry knowledge.

The exact ordering can be revised when stronger evidence becomes
available.

The important principle is:

> **A reconstruction document must never become more authoritative than
> the evidence from which it was reconstructed.**

------------------------------------------------------------------------

## 5. Work One Section at a Time

Do not attempt to reconstruct an entire unit simultaneously.

For a unit such as Unit 2:

``` text
2.1 collect → synthesize → review → commit
2.2 collect → synthesize → review → commit
2.3 collect → synthesize → review → commit
2.4 collect → synthesize → review → commit
                         ↓
                 create Unit 2 README
```

This makes errors easier to detect and prevents later evidence from
being mixed into an unfinished section.

------------------------------------------------------------------------

## 6. Collection Mode

When beginning a section, the human instructor works through Canvas and
supplies artifacts in the order encountered.

The LLM should remain primarily in **collection mode**.

### Human role

Provide relevant artifacts such as:

-   section Recall, Reflect, and Verify;
-   Begin Unit page and unit outcomes, when encountered;
-   Pre-Reading metadata;
-   Pre-Reading learning outcomes;
-   Read / Watch / Review tabs;
-   review PDFs;
-   actual Pre-Reading quiz questions;
-   Critical Chemistry Guided Reading learning outcomes;
-   Critical Chemistry Case Study learning outcomes;
-   Critical Chemistry Problem Set learning outcomes;
-   Critical Chemistry instructions;
-   simulations or linked activities;
-   Section Quiz metadata;
-   Section Quiz learning outcomes;
-   Section Quiz instructions;
-   actual Section Quiz questions;
-   Consolidation Practice instructions;
-   Consolidation learning outcomes;
-   Deliberate Practice instructions;
-   Deliberate Practice learning outcomes;
-   rubrics;
-   unusual Canvas labels, typos, grade values, or accessibility
    warnings;
-   any other artifact that appears relevant.

Do not worry about deciding in advance whether an artifact is important.
Part of the reconstruction process is determining its role.

### LLM role during collection

For each artifact:

1.  identify what it is;
2.  record its role and major content;
3.  note useful connections to prior evidence;
4.  flag obvious inconsistencies or maintenance issues;
5.  distinguish documented facts from early inference;
6.  avoid producing the final section narrative prematurely;
7.  invite the next artifact.

Responses during collection should generally be concise.

------------------------------------------------------------------------

## 7. Do Not Over-Interpret Duplicates

Canvas often exposes the same assignment through multiple tabs or
repeated views.

Examples include:

-   metadata followed by the same learning outcomes;
-   a Review tab containing a PDF already supplied;
-   assignment instructions repeated after learning outcomes;
-   duplicate quiz metadata.

When a duplicate appears:

-   acknowledge it;
-   treat it as confirmation;
-   do not count it as a new activity;
-   do not duplicate it in the eventual roadmap.

------------------------------------------------------------------------

## 8. Preserve Course Errors as Maintenance Evidence

Do not silently "fix" inherited course errors while reconstructing the
course.

Examples already encountered include:

-   incorrect section numbers in Canvas headings;
-   inconsistent quiz titles;
-   outcome lists that omit material actually assessed;
-   typographical errors;
-   formatting artifacts in quiz choices;
-   ambiguous gradebook categories;
-   accessibility warnings;
-   questionable scientific wording.

Record these under **Maintenance Notes**.

When necessary, distinguish:

``` text
What students currently see
        vs.
What should probably be corrected
```

Do not assume a correction is authorized merely because an error seems
obvious.

------------------------------------------------------------------------

## 9. PDFs and Review Materials

When a review PDF is available, inspect both:

-   parsed text;
-   diagrams, tables, figures, and visual examples.

The PDF may reveal instructional depth that the Canvas learning-outcome
list does not.

Useful questions include:

-   What conceptual sequence does the PDF use?
-   What representations are emphasized?
-   What examples recur?
-   Does it introduce terminology absent from the Canvas outcomes?
-   Does it reveal a model or explanation that should shape face-to-face
    teaching?
-   Does it overlap with a later section?

Do not assume the OpenStax or source-textbook numbering is the primary
organizational structure. CHEM 1010 section numbering should remain the
student-facing organization unless current course materials establish
otherwise.

------------------------------------------------------------------------

## 10. Actual Quiz Questions Are High-Value Evidence

Whenever possible, collect the actual Pre-Reading and Section Quiz
questions.

Learning-outcome lists describe intended scope.

Actual questions reveal what students are actually expected to do.

Compare:

``` text
STATED OUTCOMES
       ↕
ACTUAL ASSESSMENT BEHAVIOR
```

Look for:

-   recognition versus application;
-   calculations versus definitions;
-   representation changes;
-   problem complexity;
-   hidden prerequisite skills;
-   material assessed but missing from the stated outcomes;
-   outcomes listed but not visibly assessed;
-   recurring distractors that reveal likely misconceptions.

Do not reproduce answer keys in reconstruction documents unless there is
a specific instructional reason to do so.

------------------------------------------------------------------------

## 11. Section Evidence Crosswalk

Before synthesizing a section, mentally or explicitly compare evidence
across this structure:

``` text
Unit outcomes
      ↓
Recall prompts
      ↓
Pre-Reading outcomes
      ↓
review PDFs / linked resources
      ↓
actual Pre-Reading questions
      ↓
Critical Chemistry outcomes + instructions
      ↓
Problem Sets / simulations / other practice
      ↓
Consolidation outcomes
      ↓
Deliberate Practice outcomes
      ↓
Section Quiz outcomes
      ↓
actual Section Quiz questions
```

Not every section will contain every artifact.

Absence should remain visible rather than being filled with an assumed
equivalent.

------------------------------------------------------------------------

## 12. What to Look for During Comparison

### Alignment

Ask whether the same learning outcomes appear across:

-   Pre-Reading;
-   Critical Chemistry;
-   Consolidation;
-   Deliberate Practice;
-   Section Quiz.

Strong alignment is worth documenting.

Misalignment is also worth documenting.

### Progression

Ask whether activities move students from:

``` text
exposure
   ↓
concept development
   ↓
application
   ↓
retrieval
   ↓
integration
   ↓
targeted practice
   ↓
assessment
```

Do not assume this sequence is perfectly linear.

### Dependencies

Identify what the section reactivates from earlier sections.

### Forward connections

Identify what later sections will depend on this material.

### Representations

Note whether students move among:

-   macroscopic observations;
-   particle/submicroscopic models;
-   symbolic chemistry;
-   equations;
-   diagrams;
-   tables;
-   verbal explanations.

### Conceptual spine

Look for the smallest set of relationships that makes the section
coherent.

------------------------------------------------------------------------

## 13. Pre-Reading Exposure Is Not Mastery

Do not treat a Pre-Reading quiz score or completion as proof that
students have mastered the section.

Pre-Reading activities often establish:

-   vocabulary;
-   representations;
-   prerequisite concepts;
-   basic recognition;
-   first exposure.

Later Critical Chemistry activities, practice, Consolidation, Deliberate
Practice, and Section Quizzes may require substantially deeper
application.

When planning face-to-face instruction:

> **Distinguish what students should already have encountered from what
> they can reliably do independently.**

------------------------------------------------------------------------

## 14. Critical Chemistry

Critical Chemistry is substantive courseware, not merely a link
repository.

Canvas may use labels such as:

-   Guided Reading;
-   Case Study;
-   Problem Set;
-   simulation-linked activity.

The Canvas page often provides:

-   learning outcomes;
-   pacing;
-   completion instructions;

while the interactive Critical Chemistry environment contains the actual
lesson sequence.

### Collection limitation

The interactive slide/page structure may be difficult to copy into an
LLM chat.

When detailed Critical Chemistry content is unavailable:

-   preserve the Canvas learning outcomes and instructions;
-   do not invent the internal lesson sequence;
-   list the internal sequence as a known unknown if it matters.

### Completion workflow observed

Typical instructions require students to:

1.  enter Critical Chemistry;
2.  complete the named lesson;
3.  work through each page;
4.  reach the "Congratulations! ✓" banner;
5.  close the banner to receive completion credit.

### Documented Canvas gradebook behavior

The course developer has clarified that Canvas contains two Critical
Chemistry assignment groups with different purposes:

-   **Critical Chemistry** --- created by the Critical Chemistry setup
    and weighted **20%** of the course grade. Scores should populate
    here as students complete their Critical Chemistry assignments.
-   **Critical Chemistry Assignments** --- **0%** assignment group
    containing ungraded Canvas pointer assignments. These exist so
    Critical Chemistry activities appear in Canvas and on the Canvas
    calendar.

A **hyphen** in the graded Critical Chemistry entries indicates that the
student has not completed the corresponding assignment.

For instructor follow-up, the CHEM 1010 Teams channel contains the
course developer's strategies for identifying students who have not been
completing Critical Chemistry work and messaging them through Canvas
Gradebook tools.

------------------------------------------------------------------------

## 15. Retrieval Is Longitudinal

Recall, Reflect, and Verify should not be treated merely as the final
activity in a section.

The course deliberately uses spaced retrieval across prior sections.

A Section 2.1 recall activity, for example, may retrieve material from
Sections 1.1 and 1.2 while adding Section 2.1.

Therefore:

``` text
new learning
     +
earlier retrieval
     ↓
cumulative knowledge
```

When reconstructing a section, Recall prompts are valuable evidence
about which prior ideas the course expects students to keep active.

------------------------------------------------------------------------

## 16. Synthesis Trigger

The human instructor explicitly signals when collection is complete,
typically with language such as:

> **"We've reached the end."**

or

> **"That's everything for Section X.X."**

Do not create the final section roadmap before that signal unless
explicitly requested.

At that point, move from collection mode to synthesis mode.

------------------------------------------------------------------------

## 17. Section Roadmap Output

Create:

``` text
units/unit-N/section-N.N-topic.md
```

The exact structure can vary with the evidence, but a strong roadmap
usually includes:

1.  section title and purpose;
2.  why the section exists;
3.  unit context;
4.  documented learning outcomes;
5.  prerequisite knowledge;
6.  learning architecture / activity sequence;
7.  major conceptual strands;
8.  source/review-material crosswalk;
9.  Critical Chemistry role;
10. what Pre-Reading actually assesses;
11. what the Section Quiz actually assesses;
12. assessment alignment;
13. proposed role of face-to-face instruction;
14. proposed Tuesday/Thursday rhythm where appropriate;
15. suggested student practice;
16. common-confusion candidates;
17. Chemistry Triplet opportunities where useful;
18. connection forward to the next section;
19. maintenance notes;
20. known unknowns;
21. instructor quick reference;
22. evidence base.

The roadmap should be detailed enough to support future lecture planning
without requiring the instructor to reopen every Canvas object.

------------------------------------------------------------------------

## 18. Face-to-Face Teaching Recommendations

Face-to-face recommendations are usually **INFERRED / INSTRUCTOR
PRACTICE**, not inherited requirements.

The roadmap should ask:

> What can class time add that the asynchronous resources do not already
> provide efficiently?

High-value possibilities include:

-   establish the conceptual story;
-   connect multiple course resources;
-   retrieve prerequisites;
-   model expert decisions;
-   work examples that expose reasoning;
-   surface misconceptions;
-   ask students to predict;
-   give students short independent attempts;
-   connect representations;
-   diagnose errors;
-   synthesize the section;
-   prepare students for the next stage.

Do not automatically recommend re-lecturing the review PDF from
beginning to end.

------------------------------------------------------------------------

## 19. Tuesday/Thursday Rhythm

Use a two-meeting rhythm only when the calendar and section structure
support it.

Do not force every section into:

``` text
Tuesday = Topic A
Thursday = Topic B
```

Section 1.0 demonstrated that some sections span multiple quantitative
strands and may require a different rhythm.

When a section roadmap exists, it should become the preferred
reconstructed guide for that section's lecture sequence.

------------------------------------------------------------------------

## 20. Common-Confusion Candidates

These should be grounded in evidence when possible.

Useful sources include:

-   quiz distractors;
-   repeated comparison tasks;
-   terminology emphasized across multiple resources;
-   representational transitions;
-   procedures that invite algorithmic misuse;
-   concepts repeatedly retrieved in Recall activities.

Label these as **INFERRED** unless explicitly documented as
misconceptions.

------------------------------------------------------------------------

## 21. Maintenance Notes

Each section roadmap should preserve course-maintenance findings such
as:

-   incorrect section labels;
-   broken links;
-   inconsistent outcomes;
-   accessibility warnings;
-   formatting problems;
-   scientific wording that needs review;
-   unclear memorization/reference expectations;
-   gradebook inconsistencies;
-   resource duplication;
-   ambiguous instructions.

This reconstruction project is both a teaching-roadmap project and a
course-maintenance audit.

------------------------------------------------------------------------

## 22. Commit After Each Section

After the section roadmap is reviewed:

``` bash
git add units/unit-N/section-N.N-topic.md
git status
git commit -m "Add Section N.N teaching roadmap"
git push origin main
git status
```

Use the actual repository path and filename.

A clean working tree is the preferred checkpoint before beginning the
next section.

### Line-ending warning

On Windows/Git Bash, Git may report:

``` text
LF will be replaced by CRLF the next time Git touches it
```

This is generally a line-ending configuration warning, not evidence that
the Markdown content is corrupt.

### Strange untracked files

If copying Canvas text accidentally creates an unexpected file, inspect
it before deleting it.

Useful commands:

``` bash
ls -lab
git status --short
```

Do not blindly `git add .` when unexplained files are present.

------------------------------------------------------------------------

## 23. Do Not Create the Unit README Too Early

Wait until **all sections in the unit** have been reconstructed.

Then create:

``` text
units/unit-N/README.md
```

The unit README should answer:

> **Why do these sections belong together, and what should students be
> capable of by the end of the unit?**

It should synthesize rather than duplicate the section roadmaps.

Useful unit-level content includes:

-   unit conceptual progression;
-   documented unit outcomes;
-   section dependencies;
-   recurring learning architecture;
-   what students should carry into the Unit Test;
-   what students should carry forward;
-   bridge to the next unit;
-   unit-level assessment/alignment observations;
-   maintenance themes;
-   links to section roadmaps.

------------------------------------------------------------------------

## 24. Higher-Level Documentation Feedback Loop

After completing a unit:

``` text
finish all section roadmaps
          ↓
create unit README
          ↓
ask what the new evidence changes
          ↓
audit COURSE-GUIDE.md
          ↓
audit semester lecture/study guide
          ↓
audit root README/navigation
```

Do not automatically rewrite every higher-level file after every unit.

Instead ask:

-   Did the unit reveal a new course-wide pattern?
-   Did it resolve a known unknown?
-   Did it contradict an earlier inference?
-   Did it change the semester lecture plan?
-   Did it create new documentation that should be linked?

If not, leave the higher-level document alone.

------------------------------------------------------------------------

## 25. Repository Documentation Architecture

The working hierarchy is:

``` text
README.md
    repository front door
        ↓
COURSE-GUIDE.md
    semester-independent course architecture
        ↓
COURSE-RECONSTRUCTION-WORKFLOW.md
    how to continue this reconstruction process
        ↓
docs/
    semester-specific pacing and lecture documentation
        ↓
units/unit-N/README.md
    unit conceptual roadmap
        ↓
units/unit-N/section-N.N-topic.md
    detailed section teaching roadmap
```

These documents serve different purposes and should not become copies of
one another.

------------------------------------------------------------------------

## 26. New-Chat Startup Procedure

When continuing this work in a new LLM conversation, provide the
smallest set of documents needed to restore context.

Recommended order:

1.  `COURSE-GUIDE.md`
2.  `COURSE-RECONSTRUCTION-WORKFLOW.md`
3.  current semester lecture/study guide
4.  current unit README, if it exists
5.  completed section roadmaps for the current unit
6.  any unresolved source material relevant to the next section

Then state clearly:

-   which unit is being reconstructed;
-   which section is next;
-   which sections are already complete;
-   that the LLM should remain in collection mode until told the section
    is complete.

------------------------------------------------------------------------

## 27. Ready-to-Copy New-Chat Prompt

Use or adapt the following:

> You are assisting me with reconstructing and teaching CHEM 1010. Read
> `COURSE-GUIDE.md` for the course-wide instructional framework and
> `COURSE-RECONSTRUCTION-WORKFLOW.md` for the reconstruction process.
> Use the current semester guide for pacing. Use any completed unit and
> section roadmaps as reconstructed context, but treat current
> Canvas/source materials as more authoritative when they conflict.
>
> We are currently reconstructing **\[Unit N, Section N.N --- title\]**.
> Sections **\[list completed sections\]** are already documented.
>
> I will copy/paste Canvas artifacts and upload relevant PDFs one item
> at a time. Stay primarily in **collection mode**: identify each
> artifact, record what it contributes, note connections or maintenance
> issues, and avoid prematurely writing the final section narrative.
>
> Distinguish **DOCUMENTED**, **INFERRED**, **INSTRUCTOR PRACTICE**, and
> **KNOWN UNKNOWN**. Do not silently fill gaps with generic
> chemistry-course assumptions.
>
> When I say **"We've reached the end"** or **"That's everything for
> Section N.N,"** synthesize the evidence into
> `units/unit-N/section-N.N-topic.md`, following the established
> section-roadmap style. We will review and commit that file before
> moving to the next section.

------------------------------------------------------------------------

## 28. Current Reconstruction Status

At the time this workflow document was created:

### Unit 1 --- complete

-   `units/unit-1/README.md`
-   `units/unit-1/section-1.0-growing-your-math-skills.md`
-   `units/unit-1/section-1.1-the-atom.md`
-   `units/unit-1/section-1.2-the-elements.md`

### Unit 2 --- in progress

Completed:

-   `units/unit-2/section-2.1-chemical-bonds.md`

Next:

-   **Section 2.2 --- Molecular Structure**

Still to reconstruct:

-   Section 2.2 --- Molecular Structure
-   Section 2.3 --- Intermolecular Forces
-   Section 2.4 --- Chemical Nomenclature
-   `units/unit-2/README.md` after Sections 2.1--2.4 are complete

### Units 3--4

Semester-guide content remains provisional until those sections are
reconstructed in detail.

------------------------------------------------------------------------

## 29. Current Important Known Unknowns

Preserve these across chat sessions until resolved:

-   explicit role of the Unit 2 "Opioid Crisis" context within
    individual sections;
-   assessment/reference-sheet expectations for memorized items such as
    polyatomic ions;
-   canonical face-to-face demonstrations or activities intended by the
    original course developer;
-   Unit Test weighting of individual section outcomes unless actual
    tests/blueprints establish it.

Add or remove items as evidence resolves them.

------------------------------------------------------------------------

## 30. Working Summary

The reconstruction method is:

``` text
ONE SECTION AT A TIME

collect source evidence
        ↓
compare outcomes, resources, and assessments
        ↓
identify conceptual spine and dependencies
        ↓
preserve inconsistencies and unknowns
        ↓
propose face-to-face teaching role
        ↓
write section roadmap
        ↓
review
        ↓
commit
        ↓
next section
```

After all sections in a unit:

``` text
section roadmaps
       ↓
unit synthesis
       ↓
unit README
       ↓
higher-level documentation audit
```

The governing principle is simple:

> **Reconstruct the course that actually exists before deciding how to
> improve or teach it.**
