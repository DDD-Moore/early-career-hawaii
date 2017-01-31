## Contents

- [Issues in software development](#issues)
- [Data, science, and activism](#act)
- [Translating data/methods](#translate)
- [Mental health](#mental)
- [OS Software culture clash](#clash)

---

<a name="issues"></a>

## Issues in software development

1. Paradigm for software development: what works well for people doing research + developing software
1. ~~Research paper or software paper~~
1. Software quality / communication
1. Sustainability, branding: what happens if we move on: 
	- For popular packages what if dependency software go away?
	- For newer / specific software the fear on the user’s end on lack of support
1. Software promotion, use diverse languages in research community
1. Tips, philosophies? Bad experiences?

**Ideas**

**1. Paradigm for software development**

- Fast and throw-away as the first pass: first do not try to produce perfect code: no doc, weird language, and ready to throw it away. Implement the prototype that cannot be shipped. Then after a few weeks decide if we’d want to pursue it, and in what structure. 
- This is even different from refactoring. Just start over after experiments.
- Avoid over design. Perfection may be bad.

**3. Software quality / communication**

- Standard for academic software
	- Source control mandatory
	- Industry standard: industry software development is not always better. But a workstyle / management style e.g. scrum model should be implemented, particularly for small scale collaborative software development where this is often ignored
- Communication: software integration of multiple pieces from different developers. Stubbing and Mocking: Provide others the interface of your module first. This is also good to torture test other modules as your module does not work. 

**4. Sustainability, branding**

- Mandatory contribution to software: grant money to contribute maintanence. 
- Modularity is good practice: make smaller generic pieces out of a big software -- though that’d create a lot more work to yourself
- Is github submodule a good way to help modularity?
	- Subtree is better than submodule
	- Separate releases is better than submodule / subtree for reproducibility reasons; unless the other package does not do stable releases

**5. Software promotion**

- Are we going back to re-write well established code in languages that others are familiar with to get larger user base? No conclusion …
- Python  users not familiar with C/C++: a possible solution is to use GO language. Or Python compiled to GO. It is possible to write Python packages in GO instead of C++.
- Try out another languages can help programming skills in ways the old languages cannot achieve.

**6. Tips**

- Experience of failures: using languages not popular in the community, not modular enough for others to adapt and use.
- Tips:
	- codeclimate.com for code review and cleaning
	- Unit-testing can help modularity as codes is testable only when modular
	- Use long variable names (?); use unit indicator (for physics and astronomy) for variables
	- Design data structure with meta info
	- Profile code to identify the slow part
	- Choose newer tech / languages vs. using Python + band-aids when starting new projects. In industry particular start-ups more people are starting to use new tech.


<a name="act"></a>

## Data, science, and activism

- Previous experience with activism: Some people have participated in civic tech efforts and community-driven organizations
- A lot of policy works at the local and state level

**Concerns:**

- Research funding: It is apparently rare for congresspeople to get comments about science funding. Show benefits to local communities; Don’t reinvent the wheel, partner with orgs like League of Concerned Scientists
- Immigration policy
- Environmental issues
- Cybersecurity policy
- Many new federal appointees w/ little experience, might be an opportunity
- Women and gender issues
- FOIA-able work: University e-mail accounts, if you use a university bought laptop
- Public perception of academia: 
	- Rising costs of education, education as a business / consumerization
	- Professor Watch
	- Safe spaces, now a dogwhistle
	- Fact vs opinion
- Being played online
	- Gaming google results, twitter bots, coordinated brigades
	- What level should the solutions be?
	- Alt right goals are to exhaust and overwhelm
	- Working with journalists
	- Playing the game vs. changing it -- do we use their tactics?

**Actions:**

- Need to define agenda/scope of group
- Contacting politicians:
	- It is apparently rare for congresspeople to get comments about science funding
	- Show benefits to local communities
	- Don’t reinvent the wheel, partner with orgs like League of Concerned Scientists
- Data preservation
- Working locally: Chief Resilience Officers for cities
- City vs. rural divide
	- Organizing science and tech literacy outside of our bubbles
	- Data science question: how many people to move to change outcomes
- Digital democracy deliberation platforms (Nick Adams)
- How to talk to our conservative friends and family
	- Rob Willer has a ted talk
	- George Lakoff’s blog on language
- Public understanding of science
	- Astrobites 
	- Citizen science; Citizen journalism / annotation
	- Good documentaries and infographics to go viral
- Caucus of scientists, working with Concerned Scientists
- Need to fund social scientists and humanities 

**Existing / new efforts to join:**

- Slack channel / mailing list
- Laura’s data science newsletter
- Existing @Techsolidarity group, maybe start a science solidarity
- AAS congressional days, visiting reps for your district about science. Maybe get other professional societies to do it
- Writing policy documents to hand to legislatures like ALEC
- Edit wikipedia, especially in your area of expertise
	
<a name="translate"></a>

## Translating data/methods

Intro, personal goals, etc. (names removed):

- How to apply my methods to other data? How to run the entire pipeline?
- Have problems, want to connect easier for methods groups. Complementarity. Good methods often ``find'' new data.
- Data visualization, develop new tools by collaborating with domain scientists to get data.
- How to maintain software after the research is ``done''? Relies mostly on open data (NCBI?).
- Developing instruments/code, make it available and usable which requires significant amount of work. Conflict of interest for allowing customization; competition.
- Apply methods to other data, how to access, how to understand intuitively.

How is data published?

- Want to access ``raw'' data that hasn't been processed to make it less useful. Sometimes there's good reason (reduce computational resources) for this, however.
- With genetic data, often have metadata attached. BAN files with headers?
- User's guides. Standardized formats in the papers for describing the processing.
- Not all fields have requirements for detailing these steps.
- In visualization community, renewed analyses of previously published data is quite common. Often, data and demos are published on the web in conjunction with paper.
- NSF has software maintenance grants.

Standards:

- Standard format/platform for code where certain tasks are specified (running on sample data, reproducing figures, etc.).
- CodeOcean (beta) lets you do this, but not standard templates.
- Templates might be a little limiting. Maybe ``best practices'' is more appropriate.
- Maybe not in machine learning (classification), perhaps some biological pipelines (alignment, genotyping).

Experience finding other datasets:

- Often through collaborators to get access to new data. The expertise comes along with that. Longer-term, but good payoff.
- Other methods group are working on similar problems, may have access as well.

Conflicts of interest:

- To get an edge, often code is published open source, but obfuscated.
- Common if funding is shared/transition with private company that takes over the equipment/software.
- Risks to publishing work in progress. Trade-off between low-hanging fruits and big picture science. What's a good mechanism for this?

Dataset databases:

- Where to find generic listings of datasets that are not tied down to a specific domains.
- Municipalities do this, for example NYC Open Data Initiative. Legal requirements. Data backing reports. Issues of scope and/or quality.
- Often an issue of compatibility across sources (units, types of measurements, etc.).
- Existing places that have these listings may often have small, too ``cleaned-up'' datasets.

<a name="mental"></a>

## Mental health

**Impostor Syndrome**

- Seems to be ubiquitous
- Perhaps related to personality? Especially prevalent in driven people? 
- Academia attracts certain types of people more than other fields: perfectionism and being critical about us and others, especially also the people we work for
- Students working for perfectionist advisors have a deep uncertainty about being good enough, internalize criticism
- Attribution of success and failure can be to external or internal factors
- Underrepresented groups are more likely to feel impostor syndrome, feeling out of place
- Mental health and impostor syndrome is always missing from conversations around diversity and inclusions
- Strategies: 
	- Having a partner for going over your to-do list and re-normalize expectations helps with impostor syndrome
	- Not share to-do lists, but maybe share weekly stand-up of plans for the week
	- LifePCA: sit down for max an hour, go through our weekly to-dos, next week check up on what was done
	- For speakers: in addition to technical talk, hour of sit-down with graduate students about early career development, frequently mention struggles they went through, hearing people talk about it
	- Open frank acknowledgment
	- Talk openly about failure (e.g. CVs of failure)
	- E-mails and grant writing take a lot of time, but don’t give the same sense of accomplishments. Boomerang: adds onto g-mail, delays e-mails to only go out during business hours


**Mental and Physical Health Problems**

- Age where people are graduate students is a similar age where mental health issues can emerge; certain developmental times are well-accepted during a person’s life, but nobody talks about later developmental stages; perfect storm of stressful times in life coincide with times where mental health issues exacerbated by stress emerge
- High-performing young tech person who got a stroke (NYT article): effect of how being highly critical and being in an highly critical environment leads to the person not reading the cues and evidence of mental health and physical health issues
- More and more common that young people get strokes
- People tend to overestimate themselves in terms of what we can achieve: take a step back, be easy on ourselves
- Strategies:
	- Therapy
	- Meditation
	- Engineering a different mental health state: 
		- Scaled down expectations for what is considered productive
		- Don’t work all the time
		- Produce twice as much as never before
		- Take 6-8 weeks of vacation throughout the year
		- Decision in a *group*: take vacation and scale expectations for productivity
		- Normalize taking time off
- Helping others:
	- Making sure people had their own expectations of what they want to accomplish and productive
	- Normalize taking time off!
	- Talk about the plans and activities over the weekend that are not work-related
	- Slack channel on non-work related things: weekend activities and trip photos etc that are not work related
	- Have buddies:
		- Going from PhD student to postdoc leads to a collapse of social network
		- Have a buddy to check to-do lists, discuss things etc
- Feeling Accomplished:
	- Always celebrate successes the way you would have mourned your failures
	- At the end of every day, write down something you feel good about today, and something you would like to improve
	- On the Mac, there is an app called DayOne (sp?)
	- Create tag on e-mail for e-mails where someone sent you something nice, can go through those e-mails on a bad day
	- Understanding that working all over the weekend is not success, but a failure of planning
	- Work about how to optimize productivity
	- Are you doing a sprint or a marathon? 
		- Any day where you have finished one thing that sticks is a great accomplishments
		- Just put two items on your list: one for the morning, one for the afternoon, anything extra is overachievement
	- Momentum: app with motivational messages

**Other tips**

- Book: “The How of Happiness”. Also online course? Taught strategies for improving mental health
- Actionable things: list or separate GitHub page for mental health advice, like DDD mental health
- Slack channel for early-career peer support: peersupportacademics.slack.com
- Experiment with productivity:
	- Trackers like RescueTime to identify time trains
	- Habitica: app to gamify for to-do list
	- Experiment with optimal time for being productivity; recognize that our brains are not infinite 
	- Most people can not focus eight hours a day
	- Work six hours a day in three hour chunks
- Do something in the middle of the day instead of in the evening
- Turn off all notifications on phone and laptop!
- Be careful about the jokes you make with peers or more junior people!
	- Even if it is a joke, it can cause anxiety and stress
	- Most PIs don’t want to hurt junior people, so honest feedback can help!
- PIs claim that students need to work 60-80 hours a week
	- It doesn’t mean that that’s 60-80 hours of work done!
	- Look for blog posts related to that
	- Give yourself space to decompress after stressful periods
- For Future Moore workshops: perhaps have a workshop on mental health, e.g. meditation etc.


<a name="clash"></a>

## OS software culture clash

- Concern about open-source software disappearing / becoming unsupported
	- Can universities help with archival of open-source software?
	- Funding situations?
		- Having grant structures to support the development
		- Placing the software development into the requirements of a grant
	- Possibility of universities getting credit for open-source development projects
- Incentives for software development
	- Grad students / Postdoc aren’t incentivised to develop sustainable software
- Line between open-source and commercial software
	- For-profit companies dedicating funds to further open-source development
		- Microsoft (Linux kernel, Clang, …)
		- Google, Facebook (Machine learning)
	- Non-profit organizations funding specialized development 
		- Python software foundation
- Maintainability of own open-source projects
	- How to keep maintainers engaged in a project
	- Availability of people for code-reviews
	- Finding a balance with grad students between research and software development
	- Critical mass of developers
- Different goals for projects and requirements
	- Throw-away scripts
	- Long-term developed libraries/applications
- Code Curiosity
	- https://codecuriosity.org
	- Tracking contributions
	- Incentives for GitHub development
- Dependency Management
	- Python package dependencies. Shallow dependencies leading to issues
	- Chaining dependencies leading to problems down the line
- Testing
	- Regression testing for matplotlib
- Versioning
	- Semantic versioning
	- Staying at 0.x 
- Visibility
	- Advertisement v word-of-mouth
	- Tweeting about major releases
	- Posting to google groups and mailing lists
	- Critical mass of noticability
	- Popylar (google analytics for code usage)
- Documentation
	- Sphinx, Doxygen
	- Build servers: Travis, Jenkins
- Packaging and distribution
	- Optional dependencies and the hassle of maintaining those
	- Licensing issues. Reimplementing old libraries to circumvent licensing issues
	- Condaforge (https://conda-forge.github.io) v pip
	- Conan (https://www.conan.io)
	- Homebrew
	- Adding new dependencies to condaforge

**Minimize dependencies (libraries, services) and maximize the number of people involved**


