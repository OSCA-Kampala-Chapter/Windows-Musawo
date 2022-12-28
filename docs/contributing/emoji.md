# Contributor Guide

## Emoji

GitHub provides several emoji which can be included in many areas of the site, especially including comments on issues
and pull requests. To reduce confusion during evaluation of a pull request, the following emoji convey special intent.

* :question: (`:question:`) Indicates a question. This emoji comes with **no strings attached**, which means it's fine
  to simply answer the question in another comment without making any changes to code.

  In general, pull requests with an unanswered question will not be merged until *someone* addresses it. This could be
  the original creator of the issue or pull request, another contributor to the project, or even the person who asked
  the question.

* :exclamation: (`:exclamation:`) Indicates a problem with the code which will need to be addressed before changes can
  be merged into `master`. This *may* be accompanied by a specific suggestion for how to change the code. Any
  contributor is completely welcome to open a discussion regarding alternative solutions, even if the originally
  proposed change has already been made.

  Every active contributor to a project is likely to use the :exclamation: emoji (or similar) due to a simple
  misunderstanding or oversight in their evaluation. **This is absolutely fine.** If you notice a case like this, simply
  add a comment to clarify the intent and the exclamation can be considered resolved.

  Pull requests with an unresolved exclamation will not be merged until they are addressed by either a change in the
  code or a detailed explanation. While it is possible for code with an exclamation to be merged, this will usually only
  occur if *all* of the following conditions hold:

    * The rationale is fully and clearly explained
    * The code corrects an issue that is likely to affect users
    * All other proposed solutions are either too time-consuming to implement or are equally (or more) problematic

* :bulb: (`:bulb:`) Indicates an idea or suggestion regarding a potential change in the code. These items will not
  necessarily block the inclusion of code into the `master` branch, especially in cases where suggestions are trivial
  and no other issues were found during code review.

  In certain trivial cases (e.g. a simple formatting change), a core contributor on the project may make the suggested
  change themselves in the process of merging a pull request. Like the :exclamation: emoji, :bulb: suggestions invite
  open discussion about alternative solutions from any contributor.