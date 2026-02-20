Overall Estimated Duration: **1 Hours**

# Overview

In this hands-on lab, you will enable Microsoft Security Copilot,
provision a Security Compute Unit (SCU), enable Microsoft Entra Agents,
explore the Agents settings.

# Lab Scenario

Your organization is adopting AI-assisted identity operations. You are
tasked with enabling Security Copilot and configuring Microsoft Entra
Agents to optimize Conditional Access, streamline Access Reviews, and
improve Identity Governance. This reduces manual workload and provides
consistent, secure identity practices across the tenant.

# Lab Objectives

- Task 1: Configure permissions and enable Microsoft Security Copilot.

- Task 2: Enable Microsoft Entra Agent \#1 – Conditional Access
  Optimization Agent.

- Task 3: Enable Microsoft Entra Agent \#2 – Identity Risk Management
  Agent.

- Task 4: Enable Microsoft Entra Agent \#3 – Access Review Optimization
  Agent.

# Prerequisites

- Microsoft Security Copilot licensing is available for the tenant and
  Global Administrator or Security Administrator role.

- Familiarity with Microsoft Entra ID concepts (users, groups, logs,
  governance) and Azure portal navigation.

- Understanding of least-privilege access, group-based access control,
  and identity lifecycle management.

# Task 1 — Enable Microsoft Security Copilot

In this task, we will Enable Security Copilot.

1.  From the LabVM desktop, double-click Microsoft Edge to launch the
    browser.

> ![](./media/image1.png)

2.  Copy and paste the following link into your browser to access the
    Microsoft Security Copilot portal.

> https://securitycopilot.microsoft.com/

3.  If prompted to sign in, use the credentials from the **Environment**
    tab.

4.  Click on **Get started** button

![](./media/image2.png)

5.  Provide the below details and then click on **Continue** button

    1.  Workspace name - **wrkspc4SecCopilot**

    2.  Data storage location – **United States**

![](./media/image3.png)

6.  Provide the below details on the Set up your security capacity page.

    * Azure Subscription – scroll down and choose the available
        subscription

        > \[**Note** - to enable the Security Copilot, you should have
        > Contributor or Owner role on the Subscription \]

    * Resource group – Create new and provide the name as
        **RG4SecurityCopilot**

    * Prompt evaluation location – select **United States**

> ![](./media/image4.png)

7.  Scroll down to the **Select the number of units** section

8.  Enable the checkbox for **I acknowledge that I have read,
    understood, and agree to the Terms and Conditions.**

9.  Click on the **Continue** button.

![](./media/image5.png)

10. On the **Help improve Copilot** page, click on the **Continue**
    button.  
    ![](./media/image6.png)

11. On the **Copilot’s access and storage of Microsoft 365 service
    data** page, click on **Continue** button.

![](./media/image7.png)

12. On the **Logging audit data in Microsoft Purview** page, click on
    the **Skip** button.

![](./media/image8.png)

13. On the Assign roles page, click on the radio button for **No one.
    Add them later** and then click on the **Continue** button.

![](./media/image9.png)

14. On the **You’re all set** page, click on the **Finish** button.

![](./media/image10.png)

15. **Microsoft Security Copilot** is all Set up.  
    ![](./media/image11.png)

16. Click on **Agents** from the left menu.

![](./media/image12.png)

17. Click on the **Next** button on the message for **Agents work on
    your behalf**

![](./media/image13.png)

18. Click on the **View agents** button on the message for **Check the
    Agent’s work**

![](./media/image14.png)

19. We should be able to see the Agents

![](./media/image15.png)

20. From the Agents list click on the **Set up** button for
    **Conditional Access Optimization Agent**

![](./media/image16.png)

21. Click on the **Set up in Entra** button.

![](./media/image17.png)

22. If prompted, click on the **Next** button on the message for
    **Agents work on your behalf**

![](./media/image18.png)

23. If prompted, click on the **View agents** button on the message for
    **Check the Agent’s work**

> ![](./media/image19.png)

24. In the Microsoft Entra admin center, we should be able to see 3
    Agents listed under **Security Copilot agents**.

> ![](./media/image20.png)

# Task 2 — Enable Entra Agent \#1: Conditional Access Optimization Agent

1.  In the Microsoft Entra Admin Center click on the **View details**
    button of the **Conditional Access Optimization Agent**.

> ![](./media/image21.png)

2.  Click on **Start agent**

![](./media/image22.png)

3.  The agent will initiate

![](./media/image23.png)

Note - wait for the agent to initialize, this process takes about 1-2
minutes.

![](./media/image24.png)

4.  Review the Agent summary

![](./media/image25.png)

5.  Click on the **Suggestions** tab and review the suggestions.

![](./media/image26.png)

6.  Click on the **Settings** tab and review the available options, then
    click on **Users** to see Roles which can manage this agent.  
    ![](./media/image27.png)

7.  While in the **Conditional Access Optimization Agent** blade, click
    on the X to return to the Entra Agents page.

> ![](./media/image28.png)

8.  Notice that the **Conditional Access Optimization Agent** is showing
    as **Active**.

![](./media/image29.png)

# Task 3 — Enable Entra Agent \#2: Identity Risk Management Agent

1.  Now click on **View details** button for the **Identity Risk
    Management Agent**.

![](./media/image30.png)

2.  Click on the **Start agent** button.

![](./media/image31.png)

3.  Wait for the agent to initialize, it will take 1-2 minutes

![](./media/image32.png)

4.  Once the agent is ready, click on the **View agent findings**
    button.

![](./media/image33.png)

5.  As this is a Test environment, we do not have any **Risky user**
    listed.

![](./media/image34.png)

6.  Click on **Agent view** button and review the additional options
    available to **Chat with agent** and **Manage agent.**

![](./media/image35.png)

7.  Close the **Risky users** page to return back to agent page and then
    select the **Settings** tab.

8.  On the **Control** sub menu, we have various triggers available to
    configure.

![](./media/image36.png)

9.  Close the agent page and return to the Entra agents page. Now the
    **Identity Risk Management Agent** status should be **Active**.

![](./media/image37.png)

# Task 4 — Enable Entra Agent \#3: Access Review Agent

**Access Review Agent** requires special permission and configuration,
which we need to configure before we enable Access Review Agent.

1.  Click on **Users** under the Entra ID menu.

![](./media/image38.png)

2.  Select the user account **ODL_User XXXXXX**

![](./media/image39.png)

3.  Click on **Add assignments** button.

![](./media/image40.png)

4.  From the Directory roles, select the below two roles and then click
    on **Add** button.

    1.  Identity Governance Administrator

    2.  Lifecycle Workflows Administrator

> ![](./media/image41.png)

5.  The Assigned roles should now show 3 roles.

![](./media/image42.png)

6.  Open a new tab and navigate to
    <https://securitycopilot.microsoft.com/role-assignment>

7.  Click on **+ Add members**

![](./media/image43.png)

8.  In the text box **ODL_user** and select your user account, then
    click on **Add** button.

![](./media/image44.png)

![](./media/image45.png)

9.  Switch back to the **Microsoft Entra admin center**.

10. Expand **ID Governance** and select **Access review**, create a
    **Test Review 1** as shown in the image  
    ![](./media/image46.png)

![](./media/image47.png)

11. From the left menu click on **Entra agents**

![](./media/image48.png)

12. Click on **View details** button of the **Access Review Agent**

> ![](./media/image49.png)

13. Click on **Start agent** button.

![](./media/image50.png)

14. Wait for the agent to initialize

![](./media/image51.png)

15. Click on **Analyze reviews** button

![](./media/image52.png)

16. Click on the **Settings** tab and review the available options.

![](./media/image53.png)

17. Close the **Access Review Agent** page to return to the Entra agents
    page.

18. We have successfully enabled all 3 Security Copilot agents in Entra.

![](./media/image54.png)

19. Switch back to the Microsoft Security Copilot page -
    <https://securitycopilot.microsoft.com/>

20. Click on **Agents**, under **Agents in use**, we should be able to
    see all the agents enabled in **Microsoft Entra admin center**.

![](./media/image55.png)

# Summary

In this lab, we have enabled the Microsoft Security Copilot, configure
the required SCU, then we deployed the Microsoft Entra agents and
configured them wherever applicable.

You have successfully completed the hands-on lab!
