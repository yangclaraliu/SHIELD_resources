## Research Practice

Effective research collaboration across a multi-country consortium requires a degree of shared practice.
This document focuses on how we collaborate and operationalise research day to day, whereas the research protocol defines what research we are doing and why.
The tools and approaches outlined in this section reflect what has worked well in our experience, and while they are not mandated, we strongly encourage the consortium to find common ground on these where possible before much of the research activities start to roll out.

This document introduces a range of tools because different parts of the research workflow have different needs.
In practice, people may use different platforms for writing, analysis, version control, or storage.
However, at team level, SharePoint should remain the main entry point for navigation.
If work is happening elsewhere, there should still be a clear record on SharePoint showing where that content lives and how to access it.
Doing so will make it easier to share code and data, co-develop outputs, and maintain a coherent record of work across the life of the project.

Slide deck accompanying this document can be found [here](https://docs.google.com/presentation/d/1D-S5QjQgYzoJCubwAcGbyRjhBw0vXhi66ZI4ebnSg7k/edit?usp=sharing).

## Table of contents

1. [Writing and reporting](#writing-and-reporting)
2. [Reference manager](#reference-manager)
3. [Data analysis and visualisation](#data-analysis-and-visualisation)
4. [Version control](#version-control)
5. [Data storage and sharing](#data-storage-and-sharing)
6. [Dissemination](#dissemination)

## Writing and Reporting
This section covers tools for producing written outputs across the project — including research manuscripts, technical reports, press releases, and other communication materials.
Different outputs may call for different tools, and the consortium is encouraged to discuss and agree on preferred approaches for each type of output early in the project.

### Microsoft Word (OneDrive/SharePoint)
Word via OneDrive/SharePoint works well for routine collaborative writing, but performance degrades with large documents, heavy tracked changes, or many embedded citations.
On less powerful machines, this can cause freezes, crashes, and sync issues.
Reference manager integrations (e.g. Zotero, EndNote) are also prone to breaking in cloud-synced or collaborative workflows.
The browser-based version of Word is notably more limited than the desktop app.
Some partner organisations may also face institutional restrictions on accessing OneDrive/SharePoint, which is worth flagging early.

One further issue we have encountered with Microsoft Word is that tagging individuals across institutions has been difficult.
For instance, if the document is hosted on PATH's SharePoint, we cannot directly assign or tag individuals from MUBAS, AKU, or SEI Africa.
This appears to be a recurring limitation in our cross-institutional use of Microsoft Word and SharePoint.
For highly collaborative tasks, this needs to be planned carefully.

### Google Docs
Google Docs is well-suited for early-stage collaborative drafting — shared notes, scoping documents, and workshop outputs — where multiple people need to contribute quickly.
Access permissions are also generally easier to manage than in OneDrive/SharePoint.

That said, reference manager support is more limited, and formatting control is weak for longer or more structured documents.
Tracked changes and comment resolution are harder to manage cleanly through multiple review rounds.
In practice, Google Docs is often a good place to start writing, but documents typically need to move elsewhere once they become citation-heavy or publication-facing.

### LaTeX
LaTeX is well suited to publication-quality outputs, particularly technical writing involving equations, complex figures, tables, or appendices.
Unlike Word or Google Docs, it handles large documents exceptionally well — performance does not degrade as files grow.
Formatting is clean and consistent, reference management is robust, and as a plain-text format it integrates well with version control and agentic AI tools.
Note that chatbox-based AI tools (e.g. ChatGPT, CoPilot) tend to over-edit when working with LaTeX and are generally not recommended for this purpose.

The main downside is a steep learning curve.
Collaborative review workflows are less intuitive than in Word or Google Docs, and it works best in smaller, more technically confident teams.
If the consortium wishes to adopt LaTeX for shared outputs, we would recommend a dedicated orientation session to get everyone started.
In our experience, getting broader stakeholder groups — particularly non-technical collaborators — to adopt LaTeX for joint work has proven difficult, and we would not underestimate that challenge.

### Overleaf
Overleaf is a browser-based LaTeX editor that removes the need for local installation and provides a shared environment for drafting, commenting, and versioning.
It makes LaTeX more accessible, but meaningful collaboration features are behind a paywall — the free version is limited for multi-author workflows.
It works best for smaller teams already comfortable with LaTeX who have paid or institutional access.

### Markdown
Markdown is a lightweight plain-text format most useful for technical documentation, README files, and interim results rather than publications.
When combined with Quarto or R Markdown, text, code, and outputs can be integrated into a single reproducible document.
Compiling to HTML is particularly useful for packaging figures and descriptions into a shareable, self-contained file for discussion.

As plain text, it integrates naturally with version control and code-based workflows, and has a much lower learning curve than LaTeX.
It is less suited to complex formatting or publication-specific requirements, and less intuitive for collaborators more familiar with Word or Google Docs.

### TL;DR

| Tool | Strengths | Limitations |
|------|-----------|-------------|
| **Word** (OneDrive/SharePoint) | Familiar, good for tracked changes, strong reference manager support | Slow with large files; reference plugins break in collaborative/online mode; access issues for some organisations |
| **Google Docs** | Easy real-time collaboration, simple permissions, good for early drafts | Weak formatting control, limited reference manager support, not suited for publication-stage writing |
| **LaTeX** | Excellent for large/complex documents, consistent formatting, robust references, version control-friendly | Steep learning curve, less intuitive for review workflows, requires orientation for new users |
| **Overleaf** | Browser-based LaTeX, no local install needed, shared editing environment | Key collaboration features behind paywall, web-based limitations apply |
| **Markdown** | Lightweight, version-control-friendly, good for documentation and interim results; HTML export useful for sharing packaged outputs | Not suited for publications; less intuitive for non-technical collaborators |

### Suggested default
My first choice is LaTeX.
This setup links code, visualisation, and text seamlessly.
It also supports more integrated AI-assisted drafting, because code, results, and writing can be reviewed together in the same working environment.
This makes it easier to check whether interpretations are fair and to extract statistics directly when needed.
But I acknowledge the steep learning curve.
My second choice would be Google Docs (early-stage development) + Microsoft Word (late-stage development).
We generally use the end of ``first draft'' to mark the transition between these two stages.

[Back to ToC](#table-of-contents)

## Reference Manager
Beyond managing citations and bibliographies, reference managers can also serve as useful tools for shared literature organisation across the consortium.
The key consideration is how well a tool integrates with the team's writing workflow — citation integrations can be surprisingly fragile in collaborative, cloud-based, or heavily edited documents.

### Zotero
The strongest all-round option for cross-institution collaboration.
Mostly free, works across Word, Google Docs, and LaTeX/BibTeX, and the browser connector makes it easy to capture papers, reports, and PDFs from the web.
Group libraries support shared literature curation over time.
Metadata storage is unlimited on the free tier, though PDF storage is not.
Note that switching between Google Docs and Word mid-manuscript can break citation links, so it is worth settling on a writing environment early.

### EndNote
Widely used in traditional academic and institutional settings, and may be familiar to more senior collaborators.
In practice, it works best for individuals managing their own manuscript workflow — cross-institution library sharing and syncing are more cumbersome than in Zotero, and it does not integrate well with Google Docs or LaTeX.
Requires a paid or institutional licence.

### Paperpile
A good fit for teams working primarily in Google Docs — browser-first and integrates neatly with the Google ecosystem.
That said, as with Google Docs itself, it works better as a place to start than to finish: once a manuscript becomes citation-heavy or publication-facing, the limitations become more apparent.
Less flexible in mixed writing environments (Word, LaTeX), and subscription-based.

### TL;DR
| Tool | Best for | Limitations |
|------|----------|-------------|
| **Zotero** | Cross-institution collaboration, shared libraries, mixed writing environments | Shared libraries need discipline; PDF storage limited on free tier |
| **EndNote** | Solo manuscript management in Word | Poor cross-institution syncing; not suited to Google Docs or LaTeX; requires licence |
| **Paperpile** | Google Docs-centred workflows | Less flexible in mixed environments; subscription-based; not ideal for publication-stage writing |

### Suggested default
My first choice is Zotero.
It is free, powerful, and already widely used in academic work.
That makes it an easy recommendation for teams working across institutions and budgets.

[Back to ToC](#table-of-contents)

## Data analysis and visualisation

The most important question is not whether a tool is fashionable or technically impressive, but whether it fits the research purpose, supports reproducibility, can be realistically used by the people involved, and avoids creating unnecessary collaboration bottlenecks.
Where similar functionality exists, I would generally favour free and open-source tools, because they reduce licensing barriers and make it easier to work more equitably across institutions over the life of the consortium.
Wherever possible, analysis code should be made available — this supports transparency, handover, and longer-term reuse across the project and consortium.

### R / RStudio
R is usually our primary tool for statistical analysis and visualisation.
It is free and open source, and RStudio provides a user-friendly environment that lowers the barrier to entry for less technical users.
R's package ecosystem is particularly strong for epidemiology and applied data analysis, and it excels at producing publication-ready plots and exploratory graphics.
Reproducible reporting is well supported through R Markdown and Quarto.

The main caveats are that the package ecosystem is large and uneven in quality, and it is easy to introduce avoidable errors if workflows are not set up carefully.
R can also be slower than Python or Julia for computationally intensive tasks, and package installation in institutional settings can be frustrating — particularly where users need admin rights.

### Python
Python is a strong choice where the workflow goes beyond conventional statistics — for example, automation, data engineering, machine learning, or systems integration.
It is generally faster than R for many computational tasks and is highly interoperable with other tools and environments.

That said, installation and environment setup are less intuitive than R/RStudio for less technical users, and some applied statistical workflows are less convenient out of the box.
Visualisation is powerful but often less publication-ready by default than in R.
For teams whose needs are primarily conventional statistical analysis, Python can be more flexible than necessary.

### Stata
Stata is well-established in applied quantitative research and has a mature ecosystem for regression-based analysis, survey data, panel data, and standard epidemiological work.
It is relatively straightforward for these conventional workflows and handles moderately large structured datasets well.

However, it is license-based, slower and less flexible than R or Python for many modern workflows, and its visualisation capabilities are more limited.
It is less well suited to complex, unstructured, or non-tabular data, and does not fit as naturally into version-controlled or more open analytical workflows.

### ArcGIS / QGIS
Virtually all climate and health issues have a spatial dimension.
ArcGIS and QGIS are well-established tools for processing and visualising geographic data.
Full disclosure: this is how I first learned spatial epidemiology.
Their point-and-click interface makes them relatively accessible.

An issue we cannot ignore is that the file-handling layer can be quite rigid in this ``universe'' of tools.
To use ArcGIS or QGIS well, you need a decent grasp of projections, file formats, layer compatibility, joins, and related spatial data structures.
That can create a steeper practical learning curve than the interface initially suggests.

That said, for climate and health research, they are usually most useful for exploratory mapping or relatively superficial spatial tasks.
Once the workflow becomes more analytical, iterative, or complex, they are generally less flexible, less reproducible, and more labour-intensive than code-based approaches in R.
In my experience, they are therefore rarely the best option for production-stage analysis or figures.
ArcGIS also carries the usual licence-related access issues, while QGIS avoids this but still shares some of the workflow limitations of GUI-based analysis.

### Stan, Julia, and other specialist tools
Stan is used for Bayesian modelling; Julia and C++ are options for high-performance or computationally intensive work.
These tools are appropriate where there is a clear technical need.
The key principle is less about the specific language and more about whether the workflow is fit for purpose, version-controlled, transparent, reproducible, and accessible to the relevant users.

### NVivo
NVivo is one of the most established tools for qualitative coding and thematic analysis, and is useful for interview data, focus groups, document coding, and structured qualitative workflows.
There are relatively few widely adopted alternatives in this space.

The main limitations are that it is license-based, collaboration workflows are not especially smooth, and it can feel heavy or overly rigid depending on the style of qualitative work.
It is less useful where the project's qualitative component is relatively light-touch or interpretive rather than heavily code-based.

### Summary Comparison

| Tool | Best for | Limitations |
|------|----------|-------------|
| **R / RStudio** | Statistical analysis, epidemiology, publication-quality visualisation, spatial analysis and mapping | Slower for intensive computation; package environment can be frustrating in institutional settings |
| **Python** | Automation, data engineering, machine learning, scalable spatial pipelines | Less intuitive setup for non-technical users; visualisation less publication-ready by default |
| **Stata** | Conventional regression, survey, and panel data workflows | License-based; less flexible for modern or complex workflows; limited visualisation |
| **ArcGIS / QGIS** | Exploratory mapping, spatial data processing, accessible GUI-based spatial workflows | Rigid file handling; requires care with projections and layer compatibility; less flexible, reproducible, and efficient than code-based workflows for complex analysis |
| **Stan / Julia** | Bayesian modelling, high-performance computation | Specialist tools; steep learning curve |
| **NVivo** | Qualitative coding, thematic analysis | License-based; collaboration not smooth; can feel rigid for light-touch qualitative work |

### Suggested default
For visualisation, my suggested default is R.
In my experience, it offers the most flexibility and produces the best publication-quality plots.
For analysis, I would prefer us to use free and open-source tools as much as possible.
Stata and ArcGIS should be avoided where feasible, mainly because licences create access and reproducibility constraints.
NVivo is the main exception, as there are fewer clear alternatives for some qualitative workflows.

[Back to ToC](#table-of-contents)

## Version control
Version control is how we keep a clear, shared record of how our work evolves — who changed what, when, and why.
This matters especially when multiple people are contributing to the same project at different times.

### The conventional method
Most of us already practise some form of version control without calling it that.
Your desktop probably has files named something like `manuscript_20260124.docx`, `manuscript_v2_20260404.docx`, and `manuscript_final_revised_final.docx`.
This approach is intuitive and needs no setup, but it quickly becomes unwieldy: it is hard to know which file is the current one, what actually changed between versions, and whether anything important was lost or overwritten along the way.

### Git
Git is a version control system that handles all of this automatically.
It keeps a full history of every change made to a file — what changed, when, and who made the change — and makes it possible to go back to any earlier version if needed.
It also allows multiple people to work on the same project without overwriting each other’s contributions.

Git works best with plain-text files (scripts, Markdown, LaTeX).
For figures, Word documents, and PDFs, Git will store each version but cannot show you *what* changed — it just keeps a copy of the whole file each time.
Those files are backed up, but not truly tracked.

Git does have a learning curve.
It works best when the team agrees early on a simple shared workflow — when to save changes, how to name things, and how to handle parallel work.
I have a short introductory video [here](https://youtu.be/J6kL4QyBH2Q).

Version control also gives you a reliable audit trail for reproducibility.
If a reviewer or funder asks what your analysis looked like at the time of submission, you can point to the exact version of the code that generated your results.
This is increasingly expected in epidemiology and public health research, and is far more convincing than “we used version X of the script.”
For projects funded by Wellcome Trust, this is not just good practice — it is a requirement: Wellcome's data and software policy states that analysis code underpinning publications must be made publicly accessible. [[Wellcome](https://wellcome.org/research-funding/guidance/policies-grant-conditions/data-software-materials-management-and-sharing-policy)]
Treating code as a core research output from the start — through version control, clear documentation, and use of repositories that support public release — makes compliance with funder requirements much easier later on.

For Stata users: Git is compatible with Stata do-files, but the workflow is less smooth than with R or Python, and reproducibility requires a bit more care given Stata’s licence constraints.

### GitHub / GitLab
GitHub and GitLab build on Git by hosting your repository in the cloud, so the whole team can access, contribute to, and review work from anywhere.
Beyond storage, they add collaboration features: pull requests (a way to propose and discuss changes before they are merged), issue tracking, and project-level documentation.

This has been particularly useful for remote collaboration on code — far more efficient than screen-sharing or sending files back and forth.
It does require that everyone writes in a reproducible way: hardcoded file paths, for example, will not work on someone else's machine.

These platforms work well for:

- coordinating work across institutions
- maintaining a shared codebase
- documenting decisions and workflows
- enabling transparent review processes

GitHub and GitLab are designed to store **code and writing, not data**.
Avoid committing data files to these repositories.
GitHub will warn you about files over 50MB and block files over 100MB entirely — but the principle holds regardless of file size.
If your project involves proprietary code or specific institutional requirements, a private repository or self-hosted solution may be more appropriate.

A `.gitignore` file tells Git which files to ignore — data files, large outputs, or anything that should never be committed.
Setting this up at the start of a project is a simple safeguard that prevents accidental data uploads.

We do not include a detailed comparison here, as Git-based workflows are now the standard for version control in reproducible research and are generally the most practical option for shared code and technical documentation.

### Suggested default
For documents, live collaborative versions should be used wherever possible rather than manually maintaining multiple dated or version-labelled files.
People will sometimes do what they need to do, but versioning through file names should not be the default workflow.
For traceable plain-text outputs such as code, Markdown, and LaTeX, Git and GitHub are strongly recommended.

[Back to ToC](#table-of-contents)

## Data storage and sharing
Data storage and sharing should comply with the requirements of the relevant partner institutions, local ethics approvals, and any applicable requirements set by PATH.

As a general principle, identifiable individual-level data should remain in-country.
Cross-border transfer of such data is not currently assumed within the project’s ethical approvals and, if required, would likely need to be considered separately through amendment to the relevant institutional and/or national ethics processes.
Given the administrative and governance burden this may involve across multiple partners, cross-border transfer should be avoided unless there is a clear and necessary justification.

PATH can provide both SharePoint and Box storage if needed.
Both platforms can be used in a GDPR-compliant way when configured and governed appropriately, but this should not be taken to mean that all data should automatically be placed there.
In practice, data storage decisions should be driven by necessity, proportionality, institutional approval, and the sensitivity of the data involved.

Where data are stored or shared centrally, they should not be uploaded as standalone files without context.
At minimum, datasets should be accompanied by basic metadata and a simple data log or README describing what the file contains, where it came from, when it was created or updated, and whether it is raw, cleaned, linked, or analysis-ready.
Where relevant, a data dictionary should also be included to explain variable names, coding, units, and missing value conventions.

For analysis workflows, many reproducible research processes require code, data, and documentation to work together across local environments.
In practice, this means that collaborators involved in analysis will often need secure local access to relevant files and folders.
Browser-only or online-only access is unlikely to be sufficient for many analytical and computational workflows.

[Back to ToC](#table-of-contents)

## Dissemination
For most substantive outputs, we should write with **journal submission** in mind.
We have included budget for conference attendance, which should be planned around these journal submissions.

JGV and I will provide some guidance on writing style and formatting requirements to help keep outputs reasonably consistent across the project.
Most of these requirements can be found on PATH's public-facing [writing and style guide](https://www.path.org/writing-guide/).
We will aim to pull key information from this guide to a centrally accessible location for SHIELD, which likely would end up on SharePoint.
This centralised document may be fed to AI as a final screening step before a document is shared more broadly.
In general, writing should aim to be clear, concise, and suitable for external academic or professional audiences.

**Preprinting is not expected as standard.**
In most cases, there is no need to post a preprint unless there is a clear reason to disseminate findings quickly (for example, where results are especially time-sensitive or policy-relevant).

Where emerging policy questions warrant it, dissemination through policy briefs may also be considered.
This should be planned through our regular meetings and quarterly reports.

Outputs must be compliant with open access requirements.
As this work is funded by Wellcome, open access publication is required where applicable.
Associated publication fees should be covered through the relevant Wellcome mechanism and should not normally be taken from the project grant budget itself unless explicitly advised otherwise.

Where possible and appropriate, code and underlying data should be made publicly available in line with open research principles and Wellcome expectations.
Any sharing should remain consistent with ethical, legal, contractual, confidentiality, and data protection requirements.

If generative AI tools are used in preparing outputs, they should be used responsibly and transparently, and remain compliant with the requirements of the target journal, publisher, institution, and funder.
Two example declarations I have personally encountered are:

- Generative AI tools were used to assist with preparation of the manuscript text and as part of code review for both the baselinenowcast R package and the analysis applying it to the two case studies presented here. Coderabbitai https://github.com/apps/coderabbitai was used for automated code review. Claude Pro version 4 https://claude.ai/ was used for assistance with writing code and for revisions of text in the manuscript. Claude Sonnet 4 https://www.anthropic.com/claude/sonnet was used for writing and revising code. Opus https://www.anthropic.com/claude/opus was used for assistance with writing.

- Declaration of generative AI and AI-assisted technologies in the manuscript preparation process
During the preparation of this work the authors used ChatGPT (OpenAI, USA) and Perplexity Gemini Pro (Perplexity AI, Inc., USA) in order to rewrite text written by the authors in more appropriate and proper English. After using this tool/service, the authors reviewed and edited the content as needed and take full responsibility for the content of the publication.

As a project, we can discuss the best way to move forward and may have a more standardised statement across the project.

[Back to ToC](#table-of-contents)
