
API documentation guidelines
===================================

.. contents:: Table of Contents
   :depth: 4

Writing guide
----------------

The following sections focus on style and approaches to documenting API.

Documentation methods
~~~~~~~~~~~~~~~~~~~~~~~~

API documentation can be written using either of the methods:

- Tell don't teach method
- Teach don't tell method
- Hybrid method

The following table describes the characteristics of the three methods.

.. list-table::
   :widths: 10, 10, 80
   :header-rows: 1

   * - Documentation method
     - Sample components
     - Characteristics
   * - *Tell don't teach*
     -  List of API error codes

        List of message body schemas

        List of interfaces

        List of references

        Practical use cases with minimal text
     -  Fact-based.

        Minimal writing and prose.

        Easy to navigate and find specific information.

        Easy to design, write, and maintain.

        Developer, architect, and user focused. Minimal influence from management and technical writer.

        Assumes user/audience has a level of technical skill or basic understanding of API usage.

        Composed of bullet points and tables.

        Selective documentation (does not document everything and does not include frameworks and models).

        Focuses on just using the API, not on concepts or principles.

        Includes advanced functionality and complex troubleshooting.
   * -  *Teach don't tell*
     -  Tutorials and Quick Start sections

        Step-by-step lists for specific activities

        Models, diagrams, and process flows

        Detailed API descriptions

        Use cases with use case descriptions
     -  Tailored learning experience for users of all levels.

        Includes non-technical audience.

        Comprehensive documentation.

        Requires significant editorial review and feedback.

        Focuses on basic tasks with minimum level of effort.

        Prescriptive and easy to follow.

        May contain unnecessary or redundant information.
   * -  *Hybrid method*
     -
     -  Combination of Tell don't teach/Teach don't tell methods.

        Requires significant reviews from technical and non-technical users.

        Difficult to maintain.

        Product Owner, Technical Writer, testers and quality staff play a bigger part.

Conceptual + Procedural + Reference information
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

API documentation is generally composed of *15% conceptual text* + *15% procedural content* + *70% reference information*.

Conceptual text and procedural content can be omitted in some types of API documentation. For example, conceptual text is unnecessary if the API is self-explanatory. Procedural content can be skipped if existing documentation already covers the necessary tasks related to the API, or the tasks are generic.

The following table describes the characteristics of conceptual, procedural, and reference content.

.. list-table::
   :widths: 25, 25, 25, 25
   :header-rows: 1

   * -
     - Conceptual (15% or lower)
     - Procedural (15% or lower)
     - Reference (70% or higher)
   * - Content
     - Ideas and principles, models, diagrams
     - Simple, instructional language; screen captures if necessary
     - Useful, referential content only
   * - Writing style
     - Descriptive, explanatory
     - Task-based

       Imperative
     - No prose, straightforward

       Minimal explanation
   * - Formatting and language
     - Technical and/or simple prose
     - Numbered lists broken into headings/sections
     - Cross-reference links, tables, unordered lists
   * - Length
     - Any length, depending on the audience
     - Short, can include options and alternate steps
     - Lengthy but easy to navigate
   * - Example API sections
     - Overview

       Basic concepts (architecture)

       Use cases
     - Deployment and configuration

       Instructions for implementing API

       Environment setup
     - Prerequisites

       API reference (methods, parameters)

       Version log
   * - Notes
     - If conceptual sections are too long, move them to a different page or site from the API documentation.
     - If the tasks or operations are repetitive, unnecessary, trivial, or lengthy, move procedural content to a different section or page such as *Appendix, References, FAQS,* or *Support*.
     - Reference information is the primary content of API documentation since it is what developers and users need to use the API, regardless of skill level.

Documentation structure
----------------------------------------

The following sections discuss the typical documentation structure for API, as well as the basic minimum parts required.

Information map for API documentation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following diagram describes a sample outline/information map for API documentation.

.. note::

	The first two levels are recommended as per standard API documentation. However, the child headings are a guide and can be moved around as needed. The following table of API sections provide an overview of whether some parts are required or optional.

.. figure:: images/information_map.png
   :align: center

   Basic information map for API documentation

For an editable version of the information map, click `here <https://www.gloomaps.com/KwndvNWijQ>`_.

List of API documentation sections
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following is a list of sections applicable for general API documentation.

.. note::

	All sections are optional unless otherwise noted.

Introduction
  An *Introduction* section is only required if the API is independent of a group or family of products and related APIs. Add an *Introduction* only if necessary since the *Overview* section should provide most, if not everything, the reader needs.

API name
  The *API name* should feature prominently at the top of the page and in the navigation panel.

  If it's a short API document, the base URL can be included with the *API name*.

Overview
  The *Overview* should briefly describe the purpose of the API. To reduce the length of the documentation, the writer can place the most important points in Overview as a bullet point list. In most cases, the *Overview* supplements the *API name*, especially if the API is not self-explanatory.

  Avoid using the heading Description since the whole document represents a collection of descriptions. The same applies to Context since the document should clearly explain when to use and what the API is used for.

  Alternative heading names: *Description, Features, About*

Audience
  The *Audience* section is often unnecessary. The *Audience* section, similar to the *Introduction* section, is only added for a group or family of products or related APIs.

Basic concepts/Context/Functional overview
  The *Basic concepts* section is included if the API reference documentation is aimed at new users to the product, or to a non-technical audience. It can be placed in a separate document if necessary, or in the *Appendix*.

  If *Basic concepts* is added to the document, ensure that it doesn't distract the user and it only includes items that are necessary for using or understanding the API.

  *Basic concepts* should not include any content already described under *Overview*.

  *Context* - A system content diagram plus narrative text to "set the scene".

  *Functional overview* - An overview of the software system which may include wireframes, UI mockups, screenshots, workflow diagrams, and business process diagrams.

  Project management/Developer perspective: *Principles* - A list of the development and architecture principles (e.g. coding conventions, patterns).

  Project management/Developer perspective: *Software architecture* - A description of the software architecture involved such as containers, components, and dynamic runtime behavior.

  This section may include a discussion on the relationship between the other APIs, and if appropriate, the API's relationship with other API's running on other BUs.

  Components: Term definitions, data/domain models, data flow and sequence diagrams, context, functional overview, principles

Quality attributes
  *Quality attributes* refer to a list of non-functional requirements such as performance, scalability, and security.

  This is not required for customers. If needed, set Quality attributes in a separate page.

Prerequisites/Constraints/Assumptions
  The *Prerequisites* section is added if there are specific steps required in order for the reader to use or access the API.

  Obvious software requirements, such as Java or Python dependencies, shouldn't be added here and should be placed in the *Appendix* if necessary. Include software requirements in Deployment and configuration if it's absolutely necessary.

  Project Management perspective: *Constraints* refers to a list of environmental constraints such as timescale, budget, technology, team size/skills, etc. This isn't necessary for API documentation. If the target audience requires Project Management information, set a separate page instead.

  Alternative heading: *Constraints and Assumptions*

  Components: software requirements, constraints and assumptions, access privileges, dependencies, and development environment configuration, development environment description

Deployment and configuration
  *Deployment and configuration* can be placed under *Prerequisites* if it's not too long. However, if the *Deployment and configuration* steps are composed of several detailed sections, consider moving the section to a different location separate from the main API reference page.

  This section can also include a map of the software infrastructure.

  Alternative headings: *Setting up, Administrator guide, Data management*

  Components: Sections dedicated to configuring web services, AWS, Azure, Docker, Kubernetes, and testing environments, data models, entity relationship diagrams, data volumes, archiving and backup strategies

Code sample/live examples
  Each code sample or link should be preceded by a brief, introductory paragraph. Code should be formatted properly.

  Components: Code blocks, links to live samples

Use cases
  If the API's purpose is not self-explanatory, or stakeholders require an explicit description of each business or functional use case, add the *Use cases* section. Otherwise, set *Use cases* on a different page.

  *Use cases* is not the same as *Code sample/live examples*.

  *Use cases* should not be placed under the *QuickStart/Tutorials/How-to* section.

  If the *Use cases* section is extremely detailed or composed of large diagrams, move the content to a different page separate from the API documentation.

  For the purpose of API documentation, avoid including Project Management and Business information under the Use cases section.

  Components: UML diagrams, process flow, or a detailed use case description

QuickStart/Tutorials/How-to/Getting started/Walkthrough
  *QuickStart/Tutorials/How-to/Getting* started sections are composed of instructions on how to set up, run, access, invoke, implement, and instantiate the API for specific, basic actions or operations only.

  There is little distinction between the use of the different headings, and the choice between *QuickStart, Tutorials,* and *How-to* is a matter of preference. For consistency, however, the whole reference site should stick to the use of one of the headings across different documentation.

  The steps listed in this section should be practical and should demonstrate the functionality of the API, rather than discuss complex concepts or illustrate advanced properties of the API.

  *Use cases* should not be discussed in this section. However, Use cases can be used in place of Tutorials if the API has a singular or specific set of functions.

Additional features
  The *Additional features* section is added only if the extra features are not assumed along with the main features of the API.

  This section can be placed in the *Appendix* or *API Reference* sections as to not distract from the main API reference text. It can be placed as a separate sub-section if the overall API document is not too long.

API Reference
  Place the contents in tables and use headings to structure the content.

  Generated text from document generators can be used directly in this section. If generated documentation (e.g. Postman, Spring API) is hosted on a different site, add the link to either *Additional documentation, Appendix, References, Related Links,* or *Resources*.

  Components: Methods, actions, parameters, entities, options, queries, return value, data types, interfaces, endpoints, resources definition, field, errors, message format, base URL, handlers, parameter names, possible values, and exception descriptions, code breakdown

Monitoring and additional tools
  Monitoring and additional tools can be moved to Appendix or Reference links, unless they are really necessary for using the API.

  Do not use the section Monitoring and additional tools, if the topic is already discussed under Deployment and configuration.

Operators, expression operators, functions
  Content dedicated to operators and functions can be added in a separate location, or in the Appendix if necessary.

Resolving errors and issues
  Content for this section can be placed in a separate location (e.g. Troubleshooting), a link under Additional documentation, broken down under FAQs, or a child topic under *Error codes* in the *API reference* section.

  Alternative headings: *Troubleshooting, Error handling*

Additional documentation
  Additional documentation can be added to either *Reference links* or the *Appendix* sections.

Versioning/Changelog/Release notes
  This section may include legacy information or links to older documentation. This section can also be placed under Reference links or Appendix.

  If versioning information is already on an external source such as a ReadMe or Markdown file, or is automatically generated, then it isn't necessary to repeat the information here.

  Depending on the final output format and audience of the document, *Versioning/Changelog/Release notes*  can be placed on a different page and linked under *References/Related links* or *Appendix*.

  Components: Decision logs, version information, additional notes, features, support information

References/Related links
  This section may contain either internal or external links.

  *References* or *Related links* is used for any content that needs to be placed on a different page that is relevant to the API, but not necessary to use the API. The links under this section can be separate pages for FAQs, Glossary, SDK, API reference, Downloads, Resources, Terms of use, and Support information.

  Alternative headings: *References, Related links, See also, Related content*

FAQs
  This section may be used as an alternative to *Resolving errors and issues*.

Glossary
  *Glossary* is not the same as *Basic concepts*.

  *Glossary* is always placed in a separate page from the main API reference document, especially if it's lengthy and detailed.

  If specific terms need to be defined, a ``Note`` admonition should be sufficient.

  Do not create a *Glossary* section for 2-5 items.

  Technical jargon should only be added to *Glossary* if it's directly relevant to using the API.

  Terms that are generally well-known and understood in the industry, such as "API" and "server", should not be included in the *Glossary*.

  Alternative heading: *Terminology*

SDK API reference
  This section should be placed on a separate page or as a link under *Additional documentation* or *References/Related links*.

Downloads/Resources
  If the *Downloads/Resources* section is only composed of a few links, move the items to *Reference/Related links*.

  Alternative heading: *Resources, Related content*

Terms of use/Legal restrictions
  *Terms of use* and *Legal restrictions* should be placed on a different page from the main API reference document unless restrictions are specific to that API only.

  *Terms of use* can also be placed as a link under *Reference/Related links*.

Operation and Support
  *Operation and Support* refers to how the software is operated, supported, and monitored by the provider or administrator.

  Ideally, this section should include contact information of support staff or related customer-facing teams.

  Support information can be included with Versioning/Release notes information.

  Alternative headings: *Support information, Support, Help, Contact*

Authentication and authorisation
  This section contains information regarding Oauth, access tokens, client and server side authentication instructions.

Interactive console
  Swagger, a console sandbox, and API explorer tools are examples of interactive documentation.

Appendix
  The Appendix can be placed in a different page entirely if there is a substantial amount of information. The Appendix can also be a separate item under Additional Documentation, Resources, References, or Related Links, although it is generally considered a standalone item.

  Do not use an Appendix section if the links under Resources, References, or Related Links are already comprehensive.

  Components: Links or text for supplementary information specific to the API.

Best practices
  Do not repeat any content found under *Deployment and configuration*, *Resolving errors and issues, QuickStart,* or *Walkthrough* here.

  Alternative headings: *Recommendations, Tips*

Testing/Quality
  Testing and quality documentation refers to descriptions, steps, plans, and options for testing API functionality. This can be included under Tutorials or Use Cases as needed.

Appendix
------------

General rules when describing API code
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Every class, interface, structure and member in the API must have a description.
- Every constant, field, and enum, if applicable, must have a description.
- Every method must have a description for each parameter, return value, and exception.
- There must always be code samples at the top of each unique page of description. The code samples must always be preceded by an introductory sentence or paragraph. The code samples must be comprehensive enough to be descriptive of all relevant operations.

General guidelines for writing API reference content and comments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Always write in present tense. For example, write "Retrieves an aerial image."
- Use verbs when writing the method description. For example, write "Sets the label of a point of interest."
- Capitalize the first word of the description and terminate the statement or phrase with a full stop.
- Use "The" or "A".
- Be as brief as possible.
- Use monosopace/literal/code tags to format API items and components. These include status codes, values, methods, and function names.
- Use the ``<var>`` tag (HTML) or underscores (Markdown) when formatting variables.
- Use two spaces per indent, not tabs when writing code samples.
- Use tables for field-values, error codes/exceptions, and parameters.
- Use inline comments in code.
- Use headings to break up sections and text. Limit headings to 3 or 4 levels.
- Add a brief introduction after each heading.
- Use sections and text that focus on actions, rather than concepts. Emphasize what can be done and how to do it.
- The outcome or output of a task or call should always be clear and unambiguous. An example should always be provided as much as possible.
- Use "Thrown when . . . " or "If" when describing exceptions.
- When referring to deprecated code, always mention the version, as well as the replacement. For example, write "Deprecated. Replaced by getmap-aerial."

Sample documentation output
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. list-table::
  :widths: 25, 25, 25, 25
  :header-rows: 1

  * - Documentation type
    - Publishing tool/method
    - Hosting
    - Notes
  * - Readme.md (BitBucket/GitHub)
    - Cloud versioning service
    - BitBucket
    - Markdown
  * - Wiki site
    - Wiki.js
    - AWS
    - Markdown
  * - Readthedocs.org page
    - Sphinx
    - AWS
    - ReStructuredText and automated pipeline
  * - Confluence pages
    - Confluence
    - Atlassian Confluence
    - Plain Text, HTML, and Markdown. Can be exported to PDF and Word.
  * - Developer Portal API doc
    - Drupal and Swagger
    - AWS
    - Requires maintenance and customization
  * - Javadoc
    - Java
    - Any hosting service
    - Java libraries only
  * - MS Office documents
    - Sharepoint
    - Microsoft file formats, Sway presentations, HTML, XML
    - Lacks flexibility
  * - Asciidoc to HTML
    - Asciidoctor
    - AWS
    - Custom method using Docker, Git, and AWS
