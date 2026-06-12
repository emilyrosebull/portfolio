# Task It configuration guide

Use our admin console to customize Task It to your organization's needs. We save new and updated configuration details from the admin console in the Task It API.

<figure markdown="span">
  ![The Task It admin console overview, showing navigation for all configurable sections](images/admin-console-overview.png)
  <figcaption>Admin console overview</figcaption>
</figure>

## Authentication

<span class="badge badge-required">required</span>

Set up your preferred identity provider (IdP), choose an authentication protocol, and optionally set up Single Sign-On (SSO) to protect user data.

<figure markdown="span">
  ![The Task It accounts authentication screen, where users enter a Task It username and password](images/auth-task-it-accounts.png){ width="250" height="571" }
  <figcaption>Task It accounts authentication method</figcaption>
</figure>

<figure markdown="span">
  ![The Enterprise Single Sign-On authentication screen, where users log in with existing company credentials](images/auth-enterprise-sso.png){ width="250" height="571" }
  <figcaption>Enterprise Single Sign-On SSO authentication method</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Auth and SSO section of the admin console, showing fields for authentication method, protocol, and session timeout](images/auth-configuration.png)
  <figcaption>Authentication configuration</figcaption>
</figure>

Select **Auth & SSO** to configure the following components:

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Method<br><span class="badge badge-required">required</span> | Select one of the following authentication methods (how users log into the Task It application):<ul><li><strong>Task It account:</strong> Users create a Task It username and password.</li><li><strong>Enterprise SSO:</strong> Users log into Task It use their existing company credentials and your existing Identity Provider (IdP).</li></ul> | Task It account |
| Protocol<br><span class="badge badge-optional">optional</span> | If you select the Enterprise SSO authentication method, you must also select one of the following protocols:<ul><li>OpenID Connect (OIDC) <span class="badge badge-recommended">recommended</span></li><li>Security Assertion Markup Language (SAML)</li></ul> | OIDC |
| Session timeout<br><span class="badge badge-required">required</span> | We log users out of the Task It application if they're inactive for a set period of time. Select one of the following session timeout options:<ul><li>1 hour</li><li>4 hours</li><li>8 hours</li></ul> | 1 hour |

## Landing page

<span class="badge badge-required">required</span>

The main screen displaying a user's in-progress tasks, goals, and rewards.

<figure markdown="span">
  ![The Task It landing page, showing a greeting message, daily progress, a streak counter, and a list of tasks organized by category](images/landing-page.png){ width="250" height="571" }
  <figcaption>Task It landing page</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Landing page section of the admin console, showing configuration fields for the greeting message, progress message, streaks, and category settings](images/landing-page-configuration.png)
  <figcaption>Landing page configuration</figcaption>
</figure>

Select **Landing page** to configure the following components:

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Greeting message<br><span class="badge badge-optional">optional</span> | Displayed at the top of the landing page. The message includes a combination of:<ul><li>Copy (configurable)</li><li>First name using the &#123;name&#125; variable (not configurable)</li></ul>If you don't configure a greeting message, we don't display it. | Good morning, &#123;name&#125; |
| Progress message<br><span class="badge badge-optional">optional</span> | Displayed following the greeting to show a user's daily task progress. The message includes a combination of:<ul><li>Copy (configurable)</li><li>Number of tasks the user completed today using the &#123;#&#125; variable (not configurable)</li><li>Total number of tasks the user needs to complete today using the &#123;total&#125; variable (not configurable)</li></ul>If you don't configure a progress message, we don't display it. | &#123;#&#125; of &#123;total&#125; tasks done |
| Streaks<br><span class="badge badge-optional">optional</span> | A card illustrating how many consecutive days a user has been active in the application. Configuration options:<ul><li>On</li><li>Off</li></ul> | On |
| Streaks message<br><span class="badge badge-optional">optional</span> | Displayed following the greeting to show a user's streak progress. The message includes a combination of:<ul><li>Copy (configurable)</li><li>Number of days the user has been active in the application using the &#123;streak&#125; variable (not configurable)</li></ul>If you don't configure a streaks message, we don't display it. | &#123;streak&#125;-day streak |
| Category<br><span class="badge badge-optional">optional</span> | You can organize tasks into one of the following categories:<ul><li><strong>Time-based:</strong> Today, Tomorrow, Next 7 days, Next 30 days</li><li><strong>Theme:</strong> Work, Personal, Health</li><li><strong>No categories:</strong> Flat list</li></ul> | Time-based |

## Task creation

<span class="badge badge-required">required</span>

The flow that guides users through creating a new task and setting details such as name, category, and recurrence rules (daily, weekly, or one-time). Users can also connect a task to an ongoing, time-bound goal.

<figure markdown="span">
  ![The Task It task creation modal, showing fields for task name, category, recurrence, and a toggle to link the task to a goal](images/task-creation.png){ width="250" height="571" }
  <figcaption>Creating a new task, linked to a goal</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Task creation section of the admin console, showing configuration fields for task limits, heading, labels, placeholder copy, and call-to-action copy](images/task-creation-configuration.png)
  <figcaption>Task creation configuration</figcaption>
</figure>

You can configure the following components from the 

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Task Limits<br><span class="badge badge-required">required</span> | You can configure the maximum number of tasks a user is allowed to create. If you don't want a limit, leave this field blank. | No limit |
| Heading<br><span class="badge badge-optional">optional</span> | Displayed at the top of the task creation modal. If you don't configure a heading, we don't display it. | Add a task |
| Labels<br><span class="badge badge-required">required</span> | You can configure labels preceding the following sections:<ul><li>Task name input</li><li>Category dropdown</li><li>Recurrence dropdown</li><li>Goal toggle</li></ul> | **Task name input label:** Task name<br>**Category dropdown label:** Category<br>**Recurrence dropdown label:** Recurrence<br>**Goal toggle label:** Link to a goal |
| Placeholder copy<br><span class="badge badge-optional">optional</span> | Text displayed in the task and goal name input fields. This text disappears when a user starts typing. If you don't configure placeholder copy, we don't display it. | e.g. Drink 8 glasses of water<br>e.g. Run a 5K |
| Call-to-action (CTA) copy<br><span class="badge badge-required">required</span> | When a user selects the CTA, we create the task and add it to the landing page. | Add task |

## Rewards

<span class="badge badge-required">required</span>

Users can earn rewards (such as points) for completing tasks, and redeem their rewards for tangible incentives. 

<figure markdown="span">
  ![The Task It rewards screen, showing a user's earned points total and a list of redeemable incentives](images/rewards.png){ width="250" height="571" }
  <figcaption>A user's earned points and redeemable rewards</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Rewards section of the admin console, showing configuration fields for reward type, value, incentives, section heading, and button copy](images/rewards-configuration.png)
  <figcaption>Rewards configuration</figcaption>
</figure>

Select **Rewards** to configure the following components:

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Type<br><span class="badge badge-required">required</span> | You can configure the type of rewards you want to you want to award users, depending on your rewards system. | Points |
| Value<br><span class="badge badge-required">required</span> | You can configure the rewards value tasks and goals are worth depending on the category users select (work, personal, or health). | <ul><li><strong>Work:</strong> 250</li><li><strong>Personal:</strong> 50</li><li><strong>Health:</strong> 100</li></ul> |
| Incentives<br><span class="badge badge-required">required</span> | The tangible rewards users can redeem. You can configure the following incentive details:<ul><li>Name <span class="badge badge-required">required</span></li><li>Cost <span class="badge badge-required">required</span></li><li>Icon <span class="badge badge-optional">optional</span></li></ul> | N/A |
| Section heading<br><span class="badge badge-optional">optional</span> | Displayed preceding the incentives list. If you don't configure a section heading, we don't display it. | Redeem rewards |
| Button copy<br><span class="badge badge-required">required</span> | You can configure button copy for the following states:<ul><li><strong>Default:</strong> The user has enough rewards to redeem for the incentive.</li><li><strong>Redeemed:</strong> The user redeemed the incentive.</li><li><strong>Insufficient balance:</strong> The user doesn't have enough rewards to redeem for the incentive.</li></ul> | <ul><li><strong>Default:</strong> Redeem</li><li><strong>Redeemed:</strong> Redeemed</li><li><strong>Insufficient balance:</strong> Need more pts</li></ul> |

## Integrations

<span class="badge badge-optional">optional</span>

Allow users to sync Task It with with Google Calendar, Jira, and wearable devices for automatic task syncing and completion.

<figure markdown="span">
  ![The Task It Apps screen, showing available integrations including Google Calendar, Jira, and wearable device options](images/integrations.png){ width="250" height="571" }
  <figcaption>A user's integration options</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Integrations section of the admin console, showing configuration fields for available integration options, heading, and description](images/integrations-configuration.png)
  <figcaption>Integration configuration</figcaption>
</figure>

Select **Integrations** to configure the following components:

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Integration Options<br><span class="badge badge-required">required</span> | You can configure one or more the following integration options:<ul><li>Google Calendar</li><li>Jira</li><li>Apple Health</li><li>Google Health</li><li>Garmin</li><li>Fitbit</li></ul>When you configure an integration option, users will see it in the application's "Apps" section. If a user connected an integration option and you delete it, we automatically disconnect it from their application. | <ul><li>Google Calendar</li><li>Jira</li></ul> |
| Heading<br><span class="badge badge-optional">optional</span> | Displayed at the top of the "Apps" screen. If you don't configure a heading, we don't display it. | Connected apps |
| Description<br><span class="badge badge-optional">optional</span> | Displayed following the heading. If you don't configure a description, we don't display it. | Sync your calendars and tools. |

## Notifications

<span class="badge badge-optional">optional</span>

You can configure push notifications that remind users to complete upcoming tasks.

<figure markdown="span">
  ![A Task It push notification reminder displayed on a mobile device](images/notifications.png)
  <figcaption>Push notification reminder</figcaption>
</figure>

### Configuration details

<figure markdown="span">
  ![The Notifications section of the admin console, showing configuration fields for reminder timing and notification copy](images/notifications-configuration.png)
  <figcaption>Notifications configuration</figcaption>
</figure>

Select **Notifications** to configure the following components:

| **Component** | **Configuration details** | **Default** |
| --- | --- | --- |
| Reminder timing<br><span class="badge badge-required">required</span> | You can choose one of two reminder timing options:<ul><li><strong>At a time:</strong> Choose a time to send a push notification reminding users of incomplete tasks.</li><li><strong>Before due date:</strong> Select how many hours before a task is due to send a push notification reminding users of that day's incomplete tasks.</li></ul> | At a time, 5:00 PM |
| Copy<br><span class="badge badge-required">required</span> | You can configure a push notification title and body using a combination of copy and one or both of the following variables:<ul><li>&#123;taskName&#125;</li><li>&#123;firstName&#125;</li></ul> | Don't forget: &#123;taskName&#125;<br>Hi &#123;firstName&#125;, you still have tasks to complete today. |
