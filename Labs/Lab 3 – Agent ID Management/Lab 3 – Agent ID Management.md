# Lab 3 – Agent ID Management

**Overall Estimated Duration:** *1 Hour*

# Overview

In this hands-on lab, you will explore **Microsoft Entra Agent ID**, an
identity type designed for AI agents that operate autonomously on behalf
of users or systems. You will create, register Agent IDs from
**Microsoft Copilot Studio** and **Azure AI Foundry**, then manage them
in Microsoft Entra admin center.

# Lab Scenario

Your organization is adopting AI agents across application development
and security operations. You have been asked to implement a secure and
governed model using **Microsoft Entra Agent ID** to ensure:

- AI agents authenticate securely

- Their lifecycle is controlled and governed

- Access to resources is protected and compliant with least privilege

You will work with two common agent creation surfaces—**Microsoft
Copilot Studio** and **Azure AI Foundry**—and configure security,
permissions, and governance.

# Lab Objectives

- **Task 1:** Create and register Agent IDs using Microsoft Copilot
  Studio

- **Task 2:** Create and register Agent IDs using Azure AI Foundry

- **Task 3:** Verify the Agents in Microsoft Entra

- **Task 4:** Task 4 - Review Agent ID Properties

- **Task 5:** Disable AI Agent identity

# Prerequisites

- Global Administrator / Identity Administrator role

- Access to Microsoft Entra ID

- Access to *Microsoft Copilot Studio* and *Azure AI Foundry*

- Understanding of app registrations and managed identities

# Task 1 - Create & Register an Agent ID in Microsoft Copilot Studio

In this task, you will create an agent in Copilot Studio and
automatically generate its corresponding Agent ID in Entra ID.

1.  Open **Microsoft Edge** and navigate to
    `https://copilotstudio.microsoft.com/`

2.  Sign in using your lab credentials from the Environment tab.

3.  Click on **Start free** trial  
![](./media/image1.png)

4.  Click on **Got it!** Button

![](./media/image2.png)

5.  Click on **Got it** button

![](./media/image3.png)

6.  Click on **Agents**

![](./media/image4.png)

7.  Click on **New agent**

![](./media/image5.png)

8.  Copy and paste the below text to create an agent, then click on the
    right arrow

    > ***Entra ID Security Posture Analyzer***
    >
    > ***Purpose: Helps evaluate and improve an organization's Entra security posture.***
    >
    > ***Capabilities:***
    >
    > ***Analyze passwordless readiness***
    >
    > ***Provide recommendations using Identity Secure Score***
    >
    > ***Detect weak configurations (e.g., global admin assignments)***
    >
    > ***Suggest Zero Trust identity controls***
    >
![](./media/image6.png)

9.  Click on the **Create** button.

![](./media/image7.png)

![](./media/image8.png)

10. Click on the **Skip** button

11. ![](./media/image9.png)

12. Click on the newly created Agent  
![](./media/image10.png)

13. Click on the **Edit** button.

![](./media/image11.png)

14. Provide the name as **Entra ID Security Posture Analyzer** and then
    click on save button.

![](./media/image12.png)

15. In the Test you Agent text box paste the below query and click on
    the right arrow

    > `Assess our passwordless readiness. We currently use MFA with SMS and
    > have no FIDO2 keys deployed`.


![](./media/image13.png)

16. As the agent is functional, we have successfully created an Agent
    from Copilot Studio.

![](./media/image14.png)

# Task 2 - Create & Register an Agent ID in Azure AI Foundry

Azure AI Foundry allows developers to create application agents with
secure identity bindings.

1.  In your browser, navigate to <https://ai.azure.com/>

2.  Click on **Sign in to get started.**

![](./media/image15.png)

3.  Click on **Create an agent**

![](./media/image16.png)

4.  Click on **Advanced Options**, then provide the below details and
    click on **Create**

    - **Project Name:** `AIFoundry-AgentDemo`

    - **Microsoft Foundry resource** - `AIFoundry-AgentDemo-resource`
    
    -  **Resource Group:** - Create new resoruce group as `RG-AgentIDs`

    - **Region:** East US 2

    - ![](./media/image17.png)

    - ![](./media/image18.png)

5.  Agent is created successfully.

![](./media/image19.png)

# Task 3 - Verify the Agents in Microsoft Entra

In this task we will verify the Agents created in Microsoft Copilot
Studio and Azure AI Foundry

1.  Open a new tab and navigate to <https://entra.microsoft.com/>

2.  Click on **Agent ID (Preview)**

![](./media/image20.png)

3.  On the **Overview** page we should be able to see the Agents in your
    tenant count.

![](./media/image21.png)

4.  Click on **All agent identities (Preview)**

![](./media/image22.png)

5.  In the list we should be able to see the Agents created in Microsoft
    Copilot Studio

![](./media/image23.png)

# Task 4 - Review Agent ID Properties

In this task we will review the properties of the agent created in the
earlier task.

1.  Select the Agent created in Task 1 or Task 2.

2.  Review:

    - **Properties**

    - **Owners**

    - **Permissions**

    - **Sign-in logs**

    - **Usage & insights**

![](./media/image24.png)

![](./media/image25.png)

3.  From the left menu, select **Agent registry (Preview)**, we should
    be able to see 1 gent listed with details, where the Agent was
    created.

![](./media/image26.png)

# Task 5 – Disable AI Agent identity 

1.  In Microsoft Entra we can govern Agent ID.

2.  From the **All Agent Identities (Preview)**, page, select the Agent
    ID – **Agent (Microsoft Copilot Studio)**created in Task 1, then
    click on **Disable** button.

![](./media/image27.png)

3.  We can see that the Agent ID is disabled success fully

![](./media/image28.png)

# Summary

In this lab, you accomplished the following:

- Created and registered Agent IDs using **Microsoft Copilot Studio**
  and **Azure AI Foundry**.

- Verified the Agents in Microsoft Entra.

- Reviewed the Agent properties.

- Disabled Agent ID created in Task 1

You have successfully completed the hands-on lab!
