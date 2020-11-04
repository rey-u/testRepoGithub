---
title: The writing phase for contributing to customer facing content
description: This article describes the writing phase of creating customer facing content
author: rey-u
ms.author: v-rurias
ms.date: 11/03/2020
ms.prod: non-product-specific
ms.topic: contributor-guide
ms.custom: internal-contributor-guide
# customer intent: As a new part-time contributor who is unfamiliar with the publishing phase of content develop I need to know how to get my draft reviewed and published.
---

# Publishing your content

This article identifies and defines the tasks that comprise content publishing. It is one of a set of articles that are designed to help you develop and maintain quality content.

The purpose of this phase is to provide content contributors of the last steps to reviewing and publishing contributions.

![Article creation process - Publish](./media/content-dev/4-publish.svg)
<!--- this image should be 3 to 5 process buckets that reflect the work of planning --->

Once the content is drafted, contributors should open a pull request. The allows for build validation to occur, which checks for technical errors such as broken links, as well as stylistic suggestions.
Reviewers should be tagged in the pull request so they can review and provide feedback. Once feedback has been addressed, the pull request can be signed off and merged with the main branch.

## Content publishing tasks

> [!NOTE]
> Links in the task column below go to detailed task documentation for that entry.

|  | Task | Description |
|-|-|-|
|  | [Submit pull request to stage content]() | **Begins with:** Content being added to the local branch and ready to be pushed to the upstream repo <br>**Ends when:** A pull request has been opened|
|  | [Address validation errors]() | **Begins with:** A pull request kicking off OPS build validation<br>**Ends when:** Pull request successfully builds without warnings, suggestions, or errors|
|  | [Distribute doc for review]() | **Begins with:** A pull request of the draft content is opened and reviewers are tagged or mentioned<br>**Ends when:** Reviewer feedback has been addressed and the PR is signed-off|
|  | [Merge content]() | **Begins with:** The contributor or repo owner typing #sign-off as a comment in the content pull request <br>**Ends when:** The pull request is merged into the main branch|



## Next steps

> [!div class="nextstepaction"]
> [Design your content](./content-dev-design.md)
