Technical writing and consumer electronics
================================================

Most veteran technical communicators understand the benefits of topic-based writing and its relationship with structured authoring, particularly when it comes to product lines and electronics available in the market today. Some of them may even understand the tools that work in the backend such as XSLT transformations, single-source publishing and XML toolchains. With practice and experience, it is easy to get too comfortable with writing tasks, concepts, reference topics and short descriptions. Unfortunately, when you've written, reused and updated dozens of manuals and release versions of documentation for consumer electronics, you can easily forget a basic and important element to consider when writing: your audience.

The changing mainstream user
------------------------------

*DITA Best Practices* from IBM Press gives the advice that writing task-oriented information means you focus on the goals of the user and target a specific audience. However, how can you focus on specific end-results and a defined audience, when the end-user is increasingly well-versed not only in the jargon, but the technology behind electronic products and services? The line between the traditional layman "mainstream" user and the skilled technical adept is now blurred.

The challenge of writing documentation for consumer electronics has become more pronounced with the rise of affordable, powerful and portable devices and highly advanced home electronics. Along with technical advancements in the last couple of decades is the increase in technical aptitude by everyone - it is no longer the wealthy, the well-educated or even the enthusiast who grasps technical concepts, but even the most casual of users.

Consumers are more sophisticated now than they were 20 years ago as evidenced by large online communities of technical dilettantes and self-educated experts. The Internet has made even the most uninterested user a potential savant. Anyone can pick up a Raspberry Pi, an entry-level HP laptop, a Lenovo tablet or a Samsung Galaxy S4 and take advantage of the power of GPS, database and multimedia server functions, VPN and VOIP without reading a single article or reference topic in a manual or user guide.

Take as an example the touch screen interface. Although touch screen technology has been around for decades, it wasn't until they were made available in mobile phones that the man on the street learned how to effectively use one. As recent as 2006, teenagers and professionals still struggled with single-finger touch gestures and swipes. Today, 5 to 10-point touch screens are as mundane as smartphones. Everyone from the street cleaner to the business executive is adept at swiping across screens and tapping and dragging app elements. It is true that some manufacturers have special touch functions included with their products and a few pages in the manual are devoted to them, but do technical writers have to write several DITA tasks on tapping, dragging, pinching and swiping?

Electronic products today, particularly the smartphone, aren't one-trick ponies. A mundane and standard feature like the rear-facing camera of a mobile device can be used as a scanner, portable translator, motion detecting sensor and even an X-ray machine. They are all tasks users may wish to accomplish and implementing the aforementioned tasks with a smartphone does not take a high-degree of skill. Should all of these functions be included in the user guide as well?

Many technical communicators would argue that minimalism is key and that you should provide only the information that users need. However, again, who decides what today's users actually do with the electronic products that they purchased? It is very easy to write documentation with the misconception that the writer himself represents a typical user.

However, just because the writer isn't familiar with Android's bootloader, that doesn't necessarily mean a great deal of users aren't aware of it. It's also easy to underestimate just how many tinkerers and even casual users are capable of customizing and improving consumer electronics while demanding specific information from the official User guide or Integration manual.

Concepts, Tasks, and Reference topics
----------------------------------------

One of the responsibilities of the technical communicator is to review the DITA or concept maps of consumer documentation. This review should now take into consideration the rapidly changing technical aptitude of consumer electronics users.  Here are just a few questions to think about when writing and designing task outlines, concepts, maps tasks and reference topics:

Task topics:

1. Would the manufacturer recommend this particular activity or task for this product?
2. Will this task topic benefit a wide range of users or only a small subset of consumers?
3. Will adding this procedure to the documentation cause the problem of too many related topics, subtasks or child tasks? Writing a task regarding streaming media using an app or router, for example, opens up other topics such as troubleshooting hardware support, configuring media renderers and opening ports in the network.
4. Will additional limitations or requirements be needed in the Short description ``<shortdesc>`` or context ``<context>`` tags for this task topic?
5. Will this task topic need too many optional steps or decisions for the user?
6. Is the outcome of the task consistent and predictable for every user?

Concept topics:

1. What was considered jargon before but is understood by users today? In 1999, not everyone knew what a memory card was. Today, everyone knows that a tablet or smartphone benefits from an extra 32GB micro SD card for photos and apps. Managing the levels of technical jargon has always been a challenge and recent technical style guides such as the *Microsoft Manual of Style for Technical Publications* acknowledges that usage and scenarios are rapidly changing.
2. How detailed should the concept topic be for prevalent technologies and applications such as Bluetooth, Wi-Fi, lock screens and touch screens?
3. Should definitions include related technologies, products and services as well as its benefits? Support for NFC, for example, is growing in home audio devices, but it is also linked to payment methods and even authentication.

Reference topics:

1. Is there a specific body that provides details regarding a hardware or technological standard? For example, where can the customer go to learn more about MHL or DisplayPort if they need to check if it works with a specific display or adapter?
2. What other products, accessories or even software will work with this product? Is it important enough to be mentioned in the User manual or Integration guide?  Do it yourself (DIY) hardware such as barebones small form-factor PCs, convertible laptops and 2-in-1 tablets are just some examples of products that may benefit from such a reference.

The success of technical documentation depends on whether or not the reader, user or consumer finds what he or she is looking for when he opens the PDF manual or accesses the Online Help page. It is the responsibility of the technical communicator to make sure that users gets the information they need, whether they write it themselves or refer the user elsewhere.

Event-driven technology, intuitive user experience and the technical writer
-------------------------------------------------------------------------------

Apple and admirers of Apple often praise their products for being intuitive. This is one of the primary goals of developers and designers: product usage without the need for extra technical knowledge or reference. As mainstream users become more and more comfortable with today's technology, developers and designers are aiming to make the user experience of electronics as simple and straightforward (some say invisible) as it can be.

Consumer electronics have shown signs of even going in the direction of event-driven technology, where the product anticipates the user's needs or responds immediately to a stimuli such as an available Wi-Fi or the presence of a finger or person. The effects of these two trends will more likely have a profound impact on how product documentation will be written and how much is actually needed.

In the same way software developers and hardware engineers have to balance advanced features with ease of use, technical writers for consumer documentation have to realize that today's users are not as ignorant about technology as they used to be. Education, culture and the media have all contributed to the rise of capable and intelligent consumers. Some things, predictably, have not changed. Consumer electronics documentation should not be overly superfluous, but specific and genuinely useful to today's audience. DITA, structured authoring and the XML toolchain provide the rigidity and flexibility to consumer documentation.  However, what has changed is the renewed importance of technical communicators to review and revise what is essential to the user and consumer's experience and then add or remove accordingly.
