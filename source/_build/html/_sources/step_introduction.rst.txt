Step introductions in procedures
==================================

*Step introductions*, also known as *procedure headings* or *procedure platform statements*, are short sentence fragments that use a gerund or an imperative verb phrase. The step introduction precedes a list of steps for a procedure. Technical writers use them to set off a task or list of steps. Readers use them to quickly locate what they need to do in an article, document, white paper or tutorial.

The following are examples of step introductions:

- To change the display resolution, follow these steps

- To install a **.deb** file:

- To remove unnecessary fonts

Step introductions may end with a colon or without a colon depending on the style guide used by the writer. The *4th Edition of Microsoft Manual of Style* encourages the use of a colon as punctuation, as does the documentation style guide for **SUSE** and **OpenSUSE**. Most knowledgebase articles on the Internet also follow this rule. However, other writing guidelines and publications do not adhere to this practice strictly. Consult the technical editor or a company official style guide if you are not sure about punctuations on a step introduction.

Depending on the style guide, technical writers add the imperative phrases "perform the following the steps" or "follow these steps" or "do the following" after the sentence fragment describing the task. Other writing guidelines prefer a shorter step introduction.

Procedure headings and step introductions are immediately followed by a numbered list. However, if a task or procedure consists of only one step, the procedure heading can be used to introduce a single bullet point.

.. topic:: Single step procedure example

   To launch YaST2 Expert Partitioner:

    - From the KDE desktop, press **ALT+F2** then search for **Partitioner**.


When writing in a **DITA** environment, a step introduction can be placed within the ``<context>`` tag. *DITA Best Practices* from IBM Press recommends that the step introduction should not be found within the ``<shortdesc>`` tag, which focuses on the overview of the procedure or benefits and limitations of a task. **DITA 1.2** uses the ``<stepsection>`` element to mark the step introduction.

The following is an example of <stepsection> used with a step introduction:

::

    <task>
     <title>Syncing files between hard drives using Grsync</title>
     <shortdesc>Grsync can be used to sync files and folders between storage devices and across networks.</shortdesc>
    <taskbody>
      <steps>
        <stepsection>To sync files using Grsync:</stepsection>
            <step><cmd>Launch Grsync from the KDE Kickoff menu.</cmd></step>
      </steps>
    ...

The step introduction is disregarded in some style guides if the task is simple or the title already describes the procedure perfectly. In some authoring software such as **Adobe FrameMaker**, the default XSL stylesheet automatically adds a label or section heading before the steps. The label or section would add text such as "Procedure", "Tasks" or "Steps" just before the procedure list and makes a step introduction unnecessary.

A non-technical audience may find the step introduction annoying and repetitive particularly if the title of the article or tutorial uses the same words as the step introduction.

.. topic:: Step introduction with the same title as section or tutorial

    **Launching LXTerminal in LXDE**

    To launch LXTerminal in LXDE:

    1. Click **ALT+F2** and type ``LXTerminal``. Press **Enter**.

    …


The step introduction should be used consistently across documentation. Always consult the section on writing procedures in an official and approved style guide before using a step introduction in tasks or procedures.
