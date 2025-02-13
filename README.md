# User-Intent-App-Categories
A propsal for application categories that focus on user intent and workflow, rather than strict overly-specific categorization.

## Design Specification: A User-Centric Application Categorization System

**1. Introduction**

This document outlines a new approach to categorizing applications on desktop environments, aiming for improved user experience and discoverability. Traditional categorization often focuses on technical aspects of the software, leading to confusion and difficulty in finding the right tools. This system prioritizes *user intent*, grouping applications based on what the user is trying to achieve.

**2. Goals**

*   **Improve User Experience:** Make it easier for users to find the applications they need, regardless of their technical expertise.
*   **Increase Discoverability:** Expose users to a wider range of applications by grouping them in a more intuitive way.
*   **Reduce Confusion:** Eliminate artificial distinctions between application types that are not relevant to the user's workflow.
*   **Adapt to Evolving Software:** Create a flexible system that can accommodate new types of applications and changing user needs.

**3. Core Categories**

This system utilizes the following core categories:

*   **Editing / Creation:** For all applications involved in creating or modifying content of any kind (images, documents, audio, video, code, etc.).
*   **Hardware / Devices:** For applications that configure or manage how hardware devices connect and communicate with the system. (gamepads, pen tablets, RGB settings, XR headsets, etc.) This focuses on user-level settings, not system-wide changes.
*   **Content / Consumption:** For applications that allow users to experience content (media players, RSS readers, e-book readers, etc.).
*   **Games / Interactive:** For native games and games running with compatibility layers (excluding emulation), and other interactive experiences. Simulations may also fall into this category.
*   **Emulation:** For applications that emulate other systems to run software designed for those systems (retro gaming emulators, DOSBox, virtual MIDI devices, etc.).
*   **File Management / Sharing:** For applications that organize, manipulate, and transfer files (file managers, archive managers, file transfer clients, etc.).
*   **Virtualization / Containers:** For applications that create isolated environments to run software (VirtualBox, Docker, etc. - distinct from emulation).
*   **Connections / Communication:** For applications that allow users to communicate with others, connect to remote servers, and manage network connections.
*   **Assistance / Automation:** Applications that help the user interact with the system more effectively. This includes tools that provide accessibility, AI assistance, or automate tasks. The primary focus is on facilitating user control over the system, regardless of the underlying technology.
*   **Tools:** For tools that do not permanently make changes, such as calculators.
*   **User Utilities:** For tools that only concerned with the current user or their experience. (User calendars, desktop appearance, etc..)
*   **System Configuration:** For tools that affect multiple users, or the entire system. (firewalls, parental controls, etc..)

**4. Key Principles**

*   User Intent First: Categorize applications based on what the user is trying to do.
*   Embrace Ambiguity: Recognize that many applications can serve multiple purposes. Overlap is acceptable. Mild ambiguity is a strength of the system that allows flexibility with new technologies.
*   Descriptive Category Names: Use clear, user-friendly category names.
*   Detailed Descriptions: Provide detailed descriptions for each category, explaining its scope and intended use. Categories may be broad, but this is also the case with existing categorization systems. If the user knows what they want to do "edit an audio file", then they can find the program they want, even if they've forgotten the name.

**5. Benefits**

*   Intuitive Organization: The categories are based on user tasks, making it easier to find the right application.
*   Reduced Clutter: Consolidating categories (e.g., eliminating and redefining conceptually similar groups like "Accessories", "Utilities", and "System Tools") simplifies the application menu.
*   Increased Discoverability: Users may discover new applications by browsing categories based on their goals. They can use keywords or third party subgrouping if needed. The goal here is to focus on the foundational categories and avoid branching menus.
*   Flexibility: The system can accommodate new types of applications without requiring new hyper-specific categories. Trust that the user can find what they're looking for by pointing them in the right direction with broad groups. Over-specializing leads to user confusion down the line.

**6. Potential Pitfalls and Mitigation Strategies**

*   Ambiguity: Some applications may legitimately fit into multiple categories.
    *   Mitigation: Use clear category descriptions. Place the application in the *most relevant* category based on its primary function. Some menus may choose to layer name/description searching,  tags, or keywords over these categories as desired. Allowing applications to exist in multiple categories may also be possible.
*   "Wrong" Category Placement: Users may disagree with the placement of certain applications.
    *   Mitigation: Provide a mechanism for users to suggest global category changes, or personal overrides.
*   Overly Broad Categories: Some categories (e.g., "Editing / Creation") may become too broad over time.
    *   Mitigation: Continuously evaluate category usage. If necessary, consider splitting categories into siblings based on user data. Avoid child categories.
*   Technical Users: Some technical users may prefer more granular categories based on technical function.
    *   Mitigation: Provide a way for advanced users to view applications by technical categories (as an alternative view, not the primary one). This may be where tagging or keywords are most useful.

**7. Examples of Category Changes**

| Application            | Old Category (Typical) | New Category           | Rationale                                                                                                                                                                                                                                                                                                                          |
| :--------------------- | :--------------------- | :--------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| GIMP                   | Graphics               | Editing / Creation     | User is creating or editing visual content.                                                                                                                                                                                                                                                                                          |
| LibreOffice Writer     | Office                 | Editing / Creation     | User is creating or editing documents.                                                                                                                                                                                                                                                                                               |
| Visual Studio Code     | Development            | Editing / Creation     | User is creating or editing code.                                                                                                                                                                                                                                                   |
| Audacity               | AudioVideo             | Editing / Creation     | User is creating or editing audio.                                                                                                                                                                                                                                                                                                     |
| PulseAudio Volume Control | AudioVideo, System     | Hardware / Devices     | User is configuring audio hardware settings.                                                                                                                                                                                                                                                                                               |
| 7-Zip                  | Utilities              | File Management        | User is managing files.                                                                                                                                                                                                                                                                                                             |
| VirtualBox             | System                 | Virtualization         | User is creating isolated environments.                                                                                                                                                                                                                                                                                                 |
| GParted                | System                 | System Utilities      | It does affect system operation and requires root privileges. The user will typically be doing something like setting up hard drives, which affects other users of the system.                                                                                                                                                         |
| Flight Simulator        | Games                  | Games / Interactive    | This involves simulation.                                                                                                                                                                                                                                                                                                            |
| Local AI Assistant      | Accessories                  | Assistance / Automation      | Provides assistance.                                                                                                                                                                                                                                                                                                            |
| Screen Reader          | Accessibility          | Assistance / Automation      | Helps users interact with the system.                                                                                                                                                                                                                                                                                             |

**8. Addressing Potential Objections**

*   "This system is too simplistic. I need more granular categories."

    *   "Some users may prefer more detailed categories. However, This goal is to create a system that is easy to use for *all* users, including those who are not technically inclined. We believe that clear descriptions can compensate for the lack of granular categories. Having more broad categories without relying on hyper-specific subcategories or tree hierarchies is intended to allow users to more easily find the application they're looking for, based on what they want to do. We are also open to exploring alternative views for advanced users in the future."

*   "I don't agree with the placement of certain applications."

    *   "There may be disagreement about the best category for certain applications. That's why user feedback and community input are important, especially as technology changes. Please provide feedback if there's something you'd like to know or be let known.

*   "How will this system handle new types of applications?"

    *   "This system is designed to be flexible. New types of applications can typically be accommodated within the existing categories. If a new type of application doesn't fit into any of the existing categories, a new category could potentially be created based on user needs and feedback."

*   "Is Assistance / Automation just a catch-all for anything new and shiny?"

    *   "No. 'Assistance / Automation' is specifically for applications that *help* the user interact with the system. It's not limited to AI; it includes any technology designed to make the user's life easier in interacting with the system. On-screen keyboards, talkback, or other accessibility features can find a home here.

**9. Conclusion**

This new application categorization system offers a more user-centric and intuitive approach to finding and organizing applications. By focusing on user intent and embracing some ambiguity, we can create a system that is both easy to use and adaptable to the ever-changing software landscape.
