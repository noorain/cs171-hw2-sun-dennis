Problem 1 Answers

### Calendar:
- Audience: contributors, visitors, project managers (everyone); 
- Data: 
	- pull requests on date: `/repos/:owner/:repo/events`
	- issues opened on date: `/repos/:owner/:repo/issues/events`
	- commits on date: `/repos/:owner/:repo/events`
- Many Pushes: If this happens, then the single date will become the darkest
color on the scale. To ensure that a clear gradient is established, the scale
itself could dynamically scale based on the total number of degrees of magnitude.

	2.	Contributors: Audience: contributors, project managers;
		Data: contributors, number of pushes to master, lines added/removed per push, date
		 (???);
		Many Pushes: If this happens, then the scale of the graph will change. One could
		simply increase the size of each user's display window in the screen to ensure the
		most frequent contributors are still able to show some commits in their chart.
	3.	Commit Activity: Audience: contributors, project managers (mostly the latter);
		Data: commits per day, date (???);
		Many Pushes: This would throw off the scale of the bar graph - to fix this, the bar
		graph would have to be dynamic between weeks in the week view.
	4.	Code Frequency: Audience: contributors, project managers (mostly the former);
		Data: additions/deletions per date, date (???);
		Many Pushes: This would potentially alter the scale of the graph, however if the
		pushes are that frequent, each would probably not contain a great deal of changes,
		therefore it would not likely present a huge problem.
	5.	Punchcard: Audience: project managers;
		Data: Number of commits, date, time (???);
		Many Pushes: This could present a problem of the scale of the circles - to adjust this,
		perhaps adding layered circles would help, e.g. using red for the first 10, orange for
		the next 10, etc., layered on top of each other.
	6.	Pulse: Audience: contributors, project managers;
		Data: merged & proposed pull requests, active & new issues, commits, branches, authors, additions,
		deletions, date, files, commit comments (???);
		Many Pushes: