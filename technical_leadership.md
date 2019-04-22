# Technical Leadership

Technical Leadership is a relatively new role in the world of software development. There's little structured content about it available in either books or blog posts. Most content is presented as reports on the goals and experiences of individuals or companies. This is a natural process as the industry adapts and learns what combination of attributions are best suited for the role, the same process happened to the now much less obscure role of DevOps engineer. In the spirit of learning from feedback and collaboration, we want to be part of the debate by sharing what it means to be a Tech Leader at Vinta.

For us, Tech Leaders are accountable for various monitoring and guidance activities for a wide-range of perspectives, from systems to individuals. They need to have technology and architecture fluency to support business goals from a technical standpoint, as well as to keep up with co-workers individual needs and goals. There are two big cornerstones to the role: People and Technology. I'd say they are equally important and will probably require about the same mental effort on daily activities. 

The Tech Leader of a project is not necessarily the most technically experienced person in the team and forcing such a thing is not wise. Primarily because the team would be losing productive time from someone that could be best allocated as a full-time programmer and also because that person might not be interested or willing to act on the People part of the job. So a Tech Leader is someone that can both smoothly deal with people and that has a very good understanding of the project in business and technical terms.

Here is the breakdown of the most important activities Vinta expects from a person in this role.

## The People Cornerstone

### Communication
Tech leaders need to have an open and safe channel with team members. The goal is to build a relationship where people feel that they have the [psychological safety](https://rework.withgoogle.com/blog/five-keys-to-a-successful-google-team/) to impact the project. But where at the same time they trust the Tech Leader final decisions and will do their best to make them successful. Keeping up that kind of communication should also provide a better understanding about each team member strengths and needs, allowing for a clearer overview of the team. It's not possible to a good leader without knowing who you are leading.

### Project Leadership
Technical decisions should always be backed by business goals. The choice for language or framework for a particular project should be based on the knowledge of the current project status and the vision of the business next steps. The same goes for technical debts and refactorings, the decision to tackle them should be backed by precise project or business-related goals, e.g.: "this will help us to be more productive in the midterm", or "there will be a change in X feature so we need to refactor this part of the code for it to be more flexible". This means that Tech Leaders need to keep up with the other project leaders. They need to be in sync with areas such as business, marketing and finance so they can take better technical decisions based on those. Also notice that other leaders will need inputs from the Tech Leader to better accomplish their work as well. It's the Tech Leader job to push for the technical tasks to get included and accounted during product planning. Communicating technical risks and negotiating trade-offs are very important activities here.

### Mentorship
In-company mentorship programs are a great way to help people grow their careers and understand how to navigate the company processes and hierarchy. Everyone at Vinta has a mentor that will be available from time to time to hear and advise on those high level topics. This is a great resource but in general it's aimed at mid/long term goals. Tech Leaders can serve as great resources to fill in the gap of short term advisory. Teams often have processes and specific needs and that require someone inside the project to pass them on. Also, Tech Leaders are experienced people that can advise on more specific things such as people skills that can be worked on, technologies that are more important to that particular project and also provide daily feedback on various aspects.

### Pairing
Pairing is a great tool to pass knowledge on in a team. Teams that don't work full time pairing should be encouraged to pair from time to time. The more you mix people around, the better. Junior developers should pair with more experienced developers and experienced people should pair with each other now and then. Due to their understanding of the codebase and architecture, Tech Leaders should dedicate some of their time to pairing. This somewhat has the same goals as mentoring but from a more hands-on perspective.

### Connecting People / Knowledge Matching
Time is limited and it's not always possible to be available to assist teammates. That means Tech Leaders should be smart about when they should be directly jump in and help or when someone else can be assigned. To do this it's very important that she knows not only what are the strengths of people in the team but also build a strong network of people in the company that can assist on specific subjects. This will allow her to optimize how can people meet and help each other. Matching the right people is a great way to improve the performance of the team while also accelerating individual growth.

### Managing Ownership
As we'll see later in the "The Technology Cornerstone", there are many activities which the Tech Leader is ultimately accountable for (from a business perspective), but other people can be responsible to work on them. Those people should have the autonomy to execute key technical activities beyond feature development, but always receiving timely feedback from the Tech Leader to ensure continuous improvement. The Tech Leader must empower people to be owners of key aspects of the software product, like security or backups. That ownership can also rotate periodically to avoid creating gatekeepers or increasing risk due to concentrated skills. Rotating roles can also force people to document better, create processes, and consolidate knowledge. Additionally, the Tech Leader must ensure no activity is being forgotten, i.e., there are no ownership gaps.

### Hearing / Trusting the Team
In under no circumstances Tech Leaders should act as gatekeepers. Although they are experienced developers this doesn't mean that technical decisions should be taken without consulting the team. Everyone in the team regardless of experience level should be encouraged to speak and opine in all parts of the code. Ultimately is up to the Tech Leader to decide what will be done, but all decisions should take team inputs into account. This also means that Tech Leaders should not own any part of the code. There's no architecture or feature that can only be implemented by the Tech Leader. Such a thing is a red flag and can lead to disastrous situations like burnout for the Tech Leader. A much healthier approach is act as coach, unblocking and helping other people to work in those complex tasks.

## The Technology Cornerstone

### Monitor the Codebase
As one of the most experienced programmers in the team, the Tech Leader should have control of the codebase. What languages and libraries are being used? How long since they've been updated? Are there any security updates available? What architecture will be used for that new feature? Are code practices standardized? Are tests being properly written? How fast is technical debt growing? Are the gains really worth the compromises of acquiring that debt? Those are some of the questions the Tech Leader should be constantly thinking and also inquiring the team. Here is a list of tasks that need continuous monitoring:
- Libraries and tools updates
- Security releases (especially for the major tools and frameworks)
- Development processes and methodologies
- Linters (to easily standardize practices)
- Test coverage and depth (unit, integration, acceptance, etc)
- Permission tests in all endpoints
- Technical Debt (tracking and paying)
- Continuous Deployment
- Database Migrations (forwards, backwards)
- Feature Flags (managing and cleaning)
- Configurability (hard-coded values vs. environment vars vs. admin toggles)

### Guide Architecture
Good architecture decisions can save a lot of development time. Regardless of the size of the feature, insights from an experienced person can reduce a lot the effort to complete a task, simplify solutions and improve the code quality. This kind of insight can only come from someone that is both an experienced developer and that has a good understanding of the project business logic. Therefore, it's a perfect task for Tech Leaders. It's important to emphasize here that although Tech Leaders should have the final call on the architecture decisions, they should always take into account inputs from the team and should act as mentors, not gatekeepers of complex tasks.

### Monitor Application Service-level
Growing is painful, so preparing for growing can avoid a lot of stressful situations. At the beginning of new projects, is common to trade system performance and robustness for development speed. While in many cases those are worthwhile tradeoffs, they should be taken carefully as the software product grows. Tech Leaders should keep an eye on application metrics to foresee increasing demands and prepare for them at the appropriate time. Additionally, they should always be closely looking to the most critical points of the application, i.e., the key transactions where failure is the riskiest for the business. Some key activities related to service-level monitoring are:
- Scaling up application infrastructure (including optimizing settings)
- Setting up and reacting to alerts for application performance and uptime (using New Relic, for example)
- Setting up and reacting to alerts for errors (including end-user specific errors, like 4xx HTTP errors or frontend errors, using Sentry, for example)
- Enforcing backup policy (including periodic verification of backups)
- Enforcing logging policy (including end-user activity logs)
- Ensuring proper platform compatibility (specific browser versions, network conditions, etc)
- Documenting and enforcing quality-ensuring processes (downtime recovery, error postmortems, QA, deploy and release, end-user support, …)
- As well as other [non-functional requirements](http://evolutionarytesting.blogspot.com/2012/12/non-functional-requirements-checklist.html)

Note that the Tech Leader isn't the sole responsible for those activities, but she's the one Accountable (the A in the [RACI matrix](https://en.wikipedia.org/wiki/Responsibility_assignment_matrix)) for them. If anything goes wrong, the blame ultimately goes to the Tech Leader, because from a business perspective she's the one that should ensure the proper execution of tech-related activities.

### Support and Monitor Customer Success
Happy customers is the goal of the best products. There's no point in having a great codebase, with the perfect architecture if customers are not satisfied with the product. Customer Success (CS) is often the role of a full time person (or a whole team depending on the size of the product) so it's not something a Tech Leader can keep up all by herself. But it is her job to make sure the people doing it have the tools and the data to support their work. This involves adding functionalities that will facilitate the CS job, adding as much metrics and logs as possible to the product (especially to the critical flows and key transactions). Besides the service-level metrics and logs, [UX KPIs](https://designmodo.com/ux-kpi/) like *Time on Task* are other important Customer Success goals that Tech Leads can help the CS person to track and improve. Also, the Tech Leader should empower the team to answer questions and solve bugs swiftly (by ensuring good communication channels and processes, for example).

### Code Reviews
A great way to keep up with all parts of the system and mentor coworkers is by reviewing PRs. PRs are a great place to give feedback, identify when architecture is tilting to the wrong side and keep a good overview of different parts of the codebase. Tech Leaders should do as much PR reviewing as possible but doing all or close to all reviews is considered a bad practice. Everyone in the team should be reviewing each other code for the same reasons previously mentioned plus that it's a good way for less experienced people to learn.

### Experiment
Tools get outdated and new improved stuff is constantly released. Many times those can improve code quality, speed up development or automatize some process. Tech Leaders should keep an eye on those and systematically experiment and review if they are useful in the team context.

### Guide through Crisis
Crises will eventually arise in all projects. It's important that Tech Leaders are prepared for them because many times there will be people in the team that are not. Maintaining calm and thinking straight during those situations is required and will also give the confidence the team needs to sail smoothly through crisis. Tech Leaders should know who among the team are the best to tackle the situation while also asserting how many people should be deviated from their planned tasks to work on the issue.

### Tackle Tasks
Last but not least, Tech Leaders should keep actively working in project tasks. The hard part of this is actually choosing the right kind of task that will fit the schedule. Tech Leaders need to be very smart so they keep up with technical work without leaving aside all the other important activities. It's normally a good idea to look for challenging tasks with a stretched deadline. What is the best kind of task will vary according to the current project needs, but the key thing is to keep working on things that you enjoy and that you will be proud at the end of the day. There's no such thing as a non technical Tech Leader. 

