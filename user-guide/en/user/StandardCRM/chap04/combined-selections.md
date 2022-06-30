---
uid: help-en-combined-selections
title: Combined selections
description: Combined selections
author: SuperOffice RnD
so.date: 06.29.2022
keywords: CRM
so.topic: help
language: en
---

# Combined selections

A combined selection is a combination of two existing selections.

The combined selection can contain records that are common to the two existing selections, records that are different, records that are only in one of the selections or all records in the two selections.

There are however certain limitations on what can be combined:

* If you choose to create a combined selection consisting of companies, all types of selection are available.
* But if you choose to create a combined selection consisting of sales, projects, documents, follow-ups or products, only selections of the selected type are available.

The two selections to be combined can be static or dynamic. And once you have created a combined selection, you can choose to turn it into a static selection.

## How are the two selections combined?

You can select which entries you want to include in the combined selection. These are the available options:

| Icon | Option | Description |
|:-:|---|---|
| ![icon](../media/selection_comb_onlyin1.png) | Only in Selection 1 | Shows entries that are in selection 1, and excludes entries that are in both selection 1 and selection 2. |
| ![icon](../media/selection_comb_onlyin2.png) | Only in Selection 2 | Shows entries that are in selection 2, and excludes entries that are in both selection 1 and selection 2. |
| ![icon](../media/selection_comb_common.png) | Common | Shows only entries that are in both selection 1 and selection 2. |
| ![icon](../media/selection_comb_diff.png) | Difference | Shows only entries that are either in selection 1 or in selection 2. |
| ![icon](../media/selection_comb_all.png) | All | Shows only entries in selection 1 and selection 2. |

<!-- Fix reuse ID=a1 -->

In SuperOffice CRM you can create a selection of almost anything. The purpose of the examples below is to provide you with some ideas of how to use this functionality in the program.

Companies and sales

1. Create a combined selection of companies/contacts based on two existing selections: "Customers in Sweden" (selection 1) and "Sales made last year" (selection 2).
2. Select the combination type **Only in Selection 1**. The result will contain customers in Sweden to whom you sold nothing last year.
3. Save the result as a static selection under the name "Customers in Sweden with no sales", and give one of your sales staff responsibility for following up these customers.

Follow-ups

1. Create a combined selection of follow-ups based on two existing selections: "Follow-ups linked to my customers" (selection 1) and "Planned follow-ups next month" (selection 2).
2. Choose the combination type **Common**. The result will be a list of follow-ups you need to act on next month. You could then export this to a file using the **Export to file** task.

> [!NOTE]
> If you simply want to compare the companies linked to these two selections, check **Compare companies only**.

## What would you like to do now?

[Create combined selections](Creating-combined-selections.md)