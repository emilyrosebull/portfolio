# Task It configuration guide

Use our admin console to customize Task It to your organization's needs. We save new and updated configuration details from the admin console in the Task It API.

<figure markdown="span">
  ![The Task It admin console overview, showing navigation for all configurable sections](images/admin-console-overview.png)
  <figcaption>Admin console overview</figcaption>
</figure>

## Authentication <span class="badge badge-required">required</span>

Set up your preferred identity provider (IdP), choose an authentication protocol, and optionally set up Single Sign-On (SSO) to protect user data.

<figure markdown="span">
  ![The Task It accounts authentication screen, where users enter a Task It username and password](images/auth-task-it-accounts.png)
  <figcaption>Task It accounts authentication method</figcaption>
</figure>

<figure markdown="span">
  ![The Enterprise Single Sign-On authentication screen, where users log in with existing company credentials](images/auth-enterprise-sso.png)
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
| Method <span class="badge badge-required">required</span> | Select one of the following authentication methods (how users log into the Task It application): **Task It account:** Users create a Task It username and password. **Enterprise SSO:** Users log into Task It use their existing company credentials and your existing Identity Provider (IdP). | Task It account |
| Protocol <span class="badge badge-optional">optional</span> | If you select the Enterprise SSO authentication method, you must also select one of the following protocols: OpenID Connect (OIDC) <span class="badge badge-recommended">recommended</span> Security Assertion Markup Language (SAML) | OIDC |
| Session timeout <span class="badge badge-required">required</span> | We log users out of the Task It application if they're inactive for a set period of time. Select one of the following session timeout options: 1 hour 4 hours 8 hours | 1 hour |

## Landing page <span class="badge badge-required">required</span>

The main screen displaying a user's in-progress tasks, goals, and rewards.

<figure markdown="span">
  ![The Task It landing page, showing a greeting message, daily progress, a streak counter, and a list of tasks organized by category](images/landing-page.png)
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
| Greeting message <span class="badge badge-optional">optional</span> | Displayed at the top of the landing page. The message includes a combination of: Copy (configurable) First name using the {name} variable (not configurable) If you don't configure a greeting message, we don't display it. | Good morning, {name} |
| Progress message <span class="badge badge-optional">optional</span> | Displayed following the greeting to show a user's daily task progress. The message includes a combination of: Copy (configurable) Number of tasks the user completed today using the {#} variable (not configurable) Total number of tasks the user needs to complete today using the {total} variable (not configurable) If you don't configure a progress message, we don't display it. | {#} of {total} tasks done |
| Streaks <span class="badge badge-optional">optional</span> | A card illustrating how many consecutive days a user has been active in the application. Configuration options: On Off | On |
| Streaks message <span class="badge badge-optional">optional</span> | Displayed following the greeting to show a user's streak progress. The message includes a combination of: Copy (configurable) Number of days the user has been active in the application using the {streak} variable (not configurable) If you don't configure a streaks message, we don't display it. | {streak}-day streak |
| Category <span class="badge badge-optional">optional</span> | You can organize tasks into one of the following categories: **Time-based:** Today, Tomorrow, Next 7 days, Next 30 days **Theme:** Work, Personal, Health **No categories:** Flat list | Time-based |

## Task creation <span class="badge badge-required">required</span>

The flow that guides users through creating a new task and setting details such as name, category, and recurrence rules (daily, weekly, or one-time). Users can also connect a task to an ongoing, time-bound goal.

<figure markdown="span">
  ![The Task It task creation modal, showing fields for task name, category, recurrence, and a toggle to link the task to a goal](images/task-creation.png)
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
| Task Limits <span class="badge badge-required">required</span> | You can configure the maximum number of tasks a user is allowed to create. If you don't want a limit, leave this field blank. | No limit |
| Heading <span class="badge badge-optional">optional</span> | Displayed at the top of the task creation modal. If you don't configure a heading, we don't display it. | Add a task |
| Labels <span class="badge badge-required">required</span> | You can configure labels preceding the following sections: Task name input Category dropdown Recurrence dropdown Goal toggle | **Task name input label:** Task name<br>**Category dropdown label:** Category<br>**Recurrence dropdown label:** Recurrence<br>**Goal toggle label:** Link to a goal |
| Placeholder copy <span class="badge badge-optional">optional</span> | Text displayed in the task and goal name input fields. This text disappears when a user starts typing. If you don't configure placeholder copy, we don't display it. | e.g. Drink 8 glasses of water<br>e.g. Run a 5K |
| Call-to-action (CTA) copy <span class="badge badge-required">required</span> | When a user selects the CTA, we create the task and add it to the landing page. | Add task |

## Rewards <span class="badge badge-required">required</span>

Users can earn rewards (such as points) for completing tasks, and redeem their rewards for tangible incentives. 

<figure markdown="span">
  ![The Task It rewards screen, showing a user's earned points total and a list of redeemable incentives](images/rewards.png)
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
| Type <span class="badge badge-required">required</span> | You can configure the type of rewards you want to you want to award users, depending on your rewards system. | Points |
| Value <span class="badge badge-required">required</span> | You can configure the rewards value tasks and goals are worth depending on the category users select (work, personal, or health). | **Work:** 250<br>**Personal:** 50<br>**Health:** 100 |
| Incentives <span class="badge badge-required">required</span> | The tangible rewards users can redeem. You can configure the following incentive details: Name <span class="badge badge-required">required</span> Cost <span class="badge badge-required">required</span> Icon <span class="badge badge-optional">optional</span> | N/A |
| Section heading <span class="badge badge-optional">optional</span> | Displayed preceding the incentives list. If you don't configure a section heading, we don't display it. | Redeem rewards |
| Button copy <span class="badge badge-required">required</span> | You can configure button copy for the following states: **Default:** The user has enough rewards to redeem for the incentive. **Redeemed:** The user redeemed the incentive. **Insufficient balance:** The user doesn't have enough rewards to redeem for the incentive. | **Default:** Redeem<br>**Redeemed:** Redeemed<br>**Insufficient balance:** Need more pts |

## Integrations <span class="badge badge-optional">optional</span>

Allow users to sync Task It with with Google Calendar, Jira, and wearable devices for automatic task syncing and completion.

<figure markdown="span">
  ![The Task It Apps screen, showing available integrations including Google Calendar, Jira, and wearable device options](images/integrations.png)
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
| Integration Options <span class="badge badge-required">required</span> | You can configure one or more the following integration options: Google Calendar Jira Apple Health Google Health Garmin Fitbit When you configure an integration option, users will see it in the application's "Apps" section. If a user connected an integration option and you delete it, we automatically disconnect it from their application. | Google Calendar<br>Jira |
| Heading <span class="badge badge-optional">optional</span> | Displayed at the top of the "Apps" screen. If you don't configure a heading, we don't display it. | Connected apps |
| Description <span class="badge badge-optional">optional</span> | Displayed following the heading. If you don't configure a description, we don't display it. | Sync your calendars and tools. |

## Notifications <span class="badge badge-optional">optional</span>

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
| Reminder timing <span class="badge badge-required">required</span> | You can choose one of two reminder timing options: **At a time:** Choose a time to send a push notification reminding users of incomplete tasks. **Before due date:** Select how many hours before a task is due to send a push notification reminding users of that day's incomplete tasks. | At a time, 5:00 PM |
| Copy <span class="badge badge-required">required</span> | You can configure a push notification title and body using a combination of copy and one or both of the following variables: {taskName} {firstName} | Don't forget: {taskName}<br>Hi {firstName}, you still have tasks to complete today. |
