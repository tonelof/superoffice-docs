---
uid: help-en-project-guide-working-with
title: Work with project guide
description: Work with project guide
author: SuperOffice RnD
so.date: 07.04.2022
keywords: project, guide
so.topic: howto
language: en
---

# Work with project guides

If a project guide has been defined for a project type that you specify for a project, the following happens:

* The first status in the project guide is selected in the **Status** field on the main **Project** card.
* Follow-ups and/or documents for the status are listed on the **Project guide** section tab.

## The process

1. Click the **Create** button in front of the follow-up/document name.

2. In the dialog which appears, you create the follow-up/document in the usual way. Many of the fields are prefilled, but you can change the information, or add more information. See [The Document dialog][1] or [The dialog for follow-ups][2].

    You can delegate the follow-up to your colleagues by setting them as the owner of the follow-up. If defined in SuperOffice Settings and maintenance for a specific follow-up, the **Assign task to project member** dialog appears, where you can select a colleague as the owner of the follow-up.

3. When you have completed the follow-up, check **Completed** in the relevant dialog, or in the checkbox in front of the follow-up name on the **Project guide** section tab. By default, documents are marked as completed.

    > [!TIP]
    > If you want to create several follow-ups of the same type, right-click the activity and select **Create another**. The [follow-ups dialog][2] then opens.

4. Once all the required follow-ups and documents for a project status have been completed, you move on to the next status.

    > [!NOTE]
    > If you wish, you can go to the next status without creating or performing all the follow-ups/documents in a status.

5. Repeat the above procedure for all follow-ups/documents in each status of the project guide.

## Move to next status

You can move the project to the next status in two ways:

* To move the project to the next status automatically:

    It can be defined in SuperOffice Settings and maintenance that the project guide should propose moving the project on to the next status when the last follow-up in a status is marked as complete. The **Project guide - move the project to the next status** dialog then opens.

    Click **Yes** to move the project to the next status, or click **No** if you want to continue working on the project within the same status.

* To move the project to the next status manually:

    Right-click the button for the next status in the **Project guide** section tab and select **Move to this status**.

    Or do one of the following on the main **Project** card:

    1. Click **Edit** on the main **Project** card.
    2. Click the arrow next to the **Status** field.
    3. Select the required status from the list that appears. The available options are defined in SuperOffice Settings and maintenance.
    4. Click **Save**.

## Example

Which project types are assigned a project guide and which statuses and activities the project guides are to contain is set up in SuperOffice Settings and maintenance. What a project guide looks like can therefore vary, but below is an example of how a project using a project guide may proceed.

## Enter a new project and select a project type

You record a new project and select the **Conference** project type, which is linked to a project guide. The project guide contains the following statuses, follow-ups and documents.

| Statuses | Follow-ups | Documents |
|---|---|---|
| Planned | Planning meeting (Meeting (Internal)) | Conference programme (Memo) |
| In progress | Create list of project members (Follow-up) | erence (Meeting (External)) |
| Closing | Evaluation meeting (Meeting (Internal)) |
| Evaluation report (Memo) |

## The Planned status

1. You have agreed a meeting time and want to create the **Planning meeting** appointment in the Diary and invite participants.

    1. In the project guide, you click **Create** next to the **Planning meeting** follow-up.
        The **Appointment** dialog opens, with **Meeting (Internal)** specified as the appointment type and the name of the project prefilled.
    2. [Complete the information and invite participants][2].
    3. Click **Save**.

2. At the meeting you decide on the conference programme (agenda) and you want to create a memo containing this information.

    1. Click **Create** next to **Conference programme**.
        The **Document** dialog opens with **Memo** already selected as the document template, and the name of the project prefilled.
    2. Complete the rest of the information in the fields in the **Document** dialog.
    3. Click the **Create** button to create and save the memo.

3. Once the meeting has taken place and the conference programme has been decided on, you want to confirm this in the project guide and move on to the next project status.

    In the project guide, check the box next to the **Planning meeting** follow-up.

    > [!TIP]
    > You can also do this from the activities list in, for example, the **Diary** and the **Company** screens.

    1. The **Project guide - move the project to the next status** dialog opens.
    2. In this dialog, you are asked if you want to move the project to the next status, which is **In progress**.
    3. Click **Yes** to move the project to the next status.

    > [!NOTE]
    > The **Project guide - move the project to the next status** dialog opens because that is what is defined for the project type. This is done in SuperOffice Settings and maintenance.

## The In progress status

1. All the follow-ups and documents in the **Planned** status have been completed, and you have moved the project on using the **Project guide - move the project to the next status** dialog. This dialog is displayed when you set the last follow-up to completed. The follow-ups and documents for this new status are now displayed in the **Project guide** section tab.

    [!NOTE]
    > The **Project guide - move the project to the next status** dialog only comes up if this behaviour is defined for the project type. If it is not defined, you need to [move the project to the next status](#move-to-next-status).

2. At the planning meeting, you agree that your colleague should set up a list of conference delegates. You want to create a task in his diary to remind him about this.

    1. Click **Create** next to the **Create list of project members** follow-up.
        The **Assign task to project member** dialog opens.

    2. In the list of project members, select the person you want to assign the task, and click **OK**. The **Appointment** dialog opens.

    3. Enter the required information and click **Save**. (In the **Details** tab, you can see that your colleague is already defined as the owner.)

    4. The follow-up is displayed in your colleague's diary, and once he has finished setting up the list, he will mark the follow-up as **Completed**.

        > [!NOTE]
        > The **Assign task to project member** dialog opens because that is what is defined in SuperOffice Settings and maintenance.

3. You now want to produce an invitation letter.

    Click **Create** next to the **Conference invitation** document and [create the document][3].

4. Finally, the conference itself is held. You create the **Conference** meeting.

    1. Click **Create** next to the **Conference** follow-up.
        The **Appointment** dialog opens, with **Meeting (External)** specified as the appointment type and the name of the project prefilled.
    2. Complete the information and invite the conference participants in the usual way.
    3. Click **Save**.

## The Closing status

1. Once the conference has been held and all relevant follow-ups and documents in the **In progress** status have been completed, you go to the last status in the project guide, which is **Closing**.

    * Click **Yes** in the **Project guide - move the project to the next status** dialog.
        or
    * Click **Edit** on the main **Project** card, click the arrow to the right of the **Status** field and select **Closing** from the list, and then click **OK**.

2. You want to hold an internal meeting to summarise the conference.

    1. Click **Create** next to the **Evaluation meeting** appointment and create the appointment in the usual way.
    2. When the appointment has been completed, check the box.

3. Then you want to produce an evaluation report which summarises the evaluation meeting and the conference.

    Click **Create** next to the **Evaluation report** document to create the document.

Once all the required follow-ups and documents for the project have been completed, you can set the project status to completed.

<!-- Referenced links -->
[1]: ../../document/screen/index.md
[2]: ../../diary/screen/dialog-for-followups.md
[3]: ../../document/edit.md
<!-- Referenced images -->