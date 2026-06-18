---
title: Accessibility Audit
---

# sample accessibility audit

After I finished my class in 2026, I wanted to keep my digital accessibility skills fresh. I asked a website developer if I could review their site and perform a sample audit.

This audit did not cover the entire website. It covered five to six pages and listed issues from highest to lowest priority so the developer would know what to focus on first.

One of my goals was to practice avoiding “fix it” language. I wanted to explain the accessibility barriers and recommendations clearly without telling the developer how to do their job. I also wanted to practice my documentation skills and improve my use of Google Sheets, so I researched pivot tables and formulas and used what I learned to create a structured set of spreadsheets and supporting documents.

What follows is an explanation of the documents' structure as well as sanitized excerpts from that audit and its supporting documentation.

## The Method

When I first launched the website, I created a rough outline document comparing several sample pages on the site. this aided me in understanding the website's structure and  helped me decide what needed  deeper review verses what parts needed a cursory glance.  I then listed those pages on a Pages tab in a Google Sheet, which was used to create the validation lists for the main audit log. After that, I decided which tools to use. Because the sample audit was conducted independently,  both the scope  and WCAG review areas were tailored to a workflow I could use reliably. This workflow involved keyboard and screen reader use. 

## Document and Over All Structure
After reviewing the document, I  structured a google sheet around the website using the following tabs
### Tabs and What they Represented
* Index: table of contents for the sheet
* Pages and Scope: what pages were to be reviewed, what was in and out of scope and was the page filled in the audit log or deferred.
* Reference Lists: this sheet held most of the  validation rules for the audit log and pages tab.
* NVDA Log: listed the issues found on the site along with proposed solutions and notes where applicable
* WCAG Reference: A  reference for the website developer to quickly look up criteria. It was written in  easy-to-understand language and designed for quick skimming. Trippel A criteria were included for future testing purposes.
* Executive Summary: this listed simple  tables designed for a quick skim of issues and to list priorities. It was used as  a supplement  in conjunction with the pivot tables tab.
* Pivot Tables: this was the final report for both me and the website developers. The pivot tables could be expanded and collapsed where applicable. Priorities of issues are listed along with breakdowns in percentages of affected website areas.


## Executive summary structure

When it came time to create the executive summary I used the following sections.
### Structure of summary
* Title: lists name of the site and evaluator's name
* Introduction: purpose of the  summary
 * Pages and areas reviewed: lists the pages in scope which were reviewed during the audit.
* Out of scope and or limitations: listed pages and browsers and methods not used during the audit due to time and limitations For this audit. The section is divided into:
     * Screen readers:
     * Browsers:
     * Criteria:
     * Deferred and out-of-scope pages:
* Overall Findings: an overview of findings on the website. The findings are in table form.
* Accessibility priorities: a table showing priorities  listed by WCAG criteria from highest to lowest.
* Findings by Severity: a section dedicated to findings listed by severity criteria used in this audit
* Severity Overview: a table listing the scale used in this audit
* Recommended Priority Areas: a recommendation of what should be investigated in this audit. It is listed from most severe to lower  severity.  In the case of the website in question, it is divided into: 
    * Non-text Content
    * Info and Relationships
    * Name, Role, Value
    * Link Purpose
    * Status Messages
    * Headings and Labels
    * Sensory Characteristics

  Each section has a pages affected section listing the pages and total number of findings in a table.

* Conclusion: summarizes overall findings.

## Step One: Initial Review
My first task was to go through the site for orientation purposes. I listed key features I thought would be important to address during the audit and placed them in a google Doc. I repeated this task for every page with all findings in the same document for later reference when needed.

### Sanitized Excerpt

Observed so far: Skip to content link is present. Contact information appears in the footer. Product links are present.
Possible issues to verify: Skip link target and keyboard behavior. Navigation order. Link length and link purpose. Role and behavior of a particular control.


## Step Two: Create the Sheet

Next, I created the Google Sheet needed for the audit (see the tab list from above). I listed the  pages I wanted to audit, such as a landing page, a product page and a status page. I then created the reference lists and validation rules  needed to continue the audit.

## Step Three: Auditing  the site

Next, I spent time looking at each page and logging issues I noticed in the "NVDA" tab of the audit log. Here is a sample of some of the columns I included in the sheet. 
* Page name
* Component or area
* WCAG criterion
* Severity
* summary
* steps
* impact
* Recommendation
* Notes

I chose these columns so that the  developer could easily read and skim the log in conjunction with the executive summary.

## Step Three A: log the issues
When it came time to enter issues into the audit log I did the following. I first compared what NVDA exposed and what happened during keyboard testing against the relevant WCAG criteria. I then used the audit log to record confirmed issues, possible causes, impact, recommendations, and notes for the developer.
Examples of issues I looked for included missing image text alternatives, missing form labels, unexpected focus changes in controls, unclear link text, and heading levels that did not follow a logical order.
Each issue usually received its own row. If an issue appeared to come from a shared template, I noted that in the log so the developer could investigate the source rather than treating each occurrence as an unrelated issue.
### Sanitized excerpt
Following is a sample of what issues came up during this audit. They have been sanitized  for identity and privacy reasons.
### Finding One
* Page: emergency alerts
* Issue type: heading structure
* WCAG issue: 1.3.1 Info and Relationships
* Severity: Medium
* Summary: 

  this page’s heading structure does not create a clear content outline. It begins with the generic page title  followed by the repeated heading level six slogan,  then transitions to heading levels two, three, and four for page content and linked items. Several heading level four items appear to function as links rather than section headings.
* steps: 
   * Open the indicated page.
   * Using NVDA, navigate by headings.
  * Observe that the page begins with heading level one  followed by heading level six.”
   * Continue through the heading list and observe that the page uses heading level two   heading level three  and multiple heading level four items for several categories of links.
* Impact: Screen reader users may rely on headings to understand the structure of a page and move between sections. When heading levels skip unexpectedly or individual links are exposed as headings, the heading list becomes harder to interpret and less useful for navigation.
* Recommendation: 
  Review the page heading structure so headings identify meaningful sections in a logical hierarchy. Use headings for page and section organization, not only for visual styling or emphasis. Present individual links and link categories  within appropriately labeled sections or lists.
* Tested using : NVDA with Chrome on Windows plus  keyboard navigation
* Notes:
  The repeated heading level six issue is already tracked a separate audit row as a shared header or template pattern. This row focuses on the current page’s main content structure, especially the use of heading level four for linked categories. Confirm whether heading levels are controlled by page content, a CMS template, theme, plugin, or vendor component.

### Finding Two
* Page: scheduling page
* Issue type: control role and state
* WCAG issue: 4.1.2 Name, Role, Value
* Severity: Medium
* Summary:

  The branding logo control is announced by NVDA as “toggle button, not pressed,” however, activating the control leads to an external branding webpage. The exposed role and state do not communicate the control’s link behavior.

* Steps:
  * Open the scheduling page.
  * Using NVDA and the keyboard, navigate into the schedule table.
  * Navigate to the control announcing the name of the brand.
  * Activate the control.
  * Observe that activation leads to an external branding page rather than toggling a schedule table.
* Impact:

  Screen reader users may expect a control announced as a toggle button to enable, disable, or change a setting. When the control instead navigates to an external webpage, users receive incorrect information about the control’s behavior and destination.
* Recommendation:

  Expose the control with link semantics and an accessible name that communicates its destination, such as a link to the branding page, rather than exposing it as a toggle button with an irrelevant pressed state.
* Tested using: NVDA with Chrome on Windows, plus keyboard navigation
* Notes:

  Activation of the control appears to lead to a separate branding page rather than toggling a state. Confirm whether the incorrect control role and state can be corrected through widget configuration, requires a vendor fix, or requires an alternate accessible implementation.

