# How to use WAVE

## What is it?

WAVE, the Web Accessibility Evaluator Tool, is a free tool designed by [WebAIM](www.webaim.org) to evaluate certain baseline accessibility features of websites and web-based content.  

Websites can be evaluated on a per-page basis using WAVE.  Recently, the makers of WAVE have started to expose WAVE APIs to do larger scans, however this README will focus on how to use the web-based WAVE tool.  

## Tutorial: Using WAVE on the web

### Requirements
* Webpage(s) containing content to be tested
* WAVE website
* Testing developer (hereafter referred to as the tester)
* [The WAVE icon key](icon_key.md) (optional, recommended)

### Steps
For each webpage to be tested, complete the following steps:
1. Bring up [WAVE](http://wave.webaim.org/) in a browser.  
2. Copy the URL of the page to be evaluated and paste it into the `Web page address...` searchbar in WAVE, then press Enter or click on the submit button (the arrow to the right of the searchbar).
3. On the resulting page, evaluate the results.  The dashboard on the left can be used as follows:
  * The `Summary` tab: provides a high-level view of the status of the page.  
    * Items marked `Errors` should be reviewed for remediation.  Errors are occasionally falsely reported, however they should always be investigated to determine whether they need to be addressed.  
    * `Alerts` are items that may need to be improved for accessibility but that cannot be definitely, programmatically identified as problems.  These should evaluated with the same attention as Errors.
    * `Features` are items present on the page reported as beneficial for accessibility, such as the presence of alt text on images, semantically-correct HTML form markup, and so on.
    * `Structural Elements` identify semantically-correct HTML structural elements such as headings, lists, and frames in use on the page.  This overview can be used by the tester to evaluate generally how well the page is structured.
    * `HTML5 and ARIA` identifies HTML5 elements and ARIA attributes in use on the page.  These can be used in ways similar to the `Structural Elements` report, to evaluate how these technologies are being used for accessibility, and if their use can/must be improved.
    * `Contrast Errors` items are items identified as being too low contrast to be accessible.  These items need to be reviewed and remediated as needed by a human.  More information about these errors can be found in the `Contrast` tab in WAVE.  A color contrast checker is also available in the `Contrast` tab to help produce contrasting hex color combinations to satisfy accessibility criteria.
* The `Details` tab returns a detailed list of all of the WAVE items reported in the summary for the page.  This list can be filtered to return items risking compliance against [Section 508](https://www.access-board.gov/guidelines-and-standards/communications-and-it/about-the-section-508-standards/section-508-standards), [WCAG 2.0 Level A or AA](https://www.w3.org/TR/UNDERSTANDING-WCAG20/conformance.html#uc-levels-head), or all three sets of guidelines.
* The `Documentation` tab returns explanatory documentation about the meanings of the items detected by WAVE, with suggested remediation techniques.
* The `Outline` tab returns the heading structure of the page.  This can be used for a high-level evaluation of the accessibility of the heading structure of the page, and the effectiveness of the use of headings on the page in general.
4. For remediation, consult the tools available in the WAVE dashboard as described above, and optionally the [WAVE icon key](icon_key.md) and related code samples as needed.  For additional support, consider reaching out to the Best Practices Group on Accessibility.

### Caution(s)
* While WAVE is an excellent tool for evaluating pages for web accessibility, it should used as a first step rather than the only step to making sites accessible.  As indicated above, it is able to programmatically determine accessibility issues that are easy to detect from code alone, such as missing alt text on images, semantically-incorrect HTML elements, and broken HTML form markup.  However, the tester should use this tool to guide remediation efforts while using other tools and techniques for additional review for potential issues such as color contrast issues, accuracy/appropriateness of alt text, and so on.
* WAVE will report items on all content on the page.  If evaluating content within a template such as a Wordpress site, this may result in "noise" in reports, or items in the summary that may be a) falsely identified as issues, b) not addressable for remediation by the tester, and/or c) occur multiple times on the page and bloat the report.  The tester should be aware of this issue and parse out meaningful items accordingly.  Where accessibility issues are detected in templates that the tester cannot remediate such as in the case of vendor platforms, the tester should report the issue to the vendor/party that can address remediation with these findings.
