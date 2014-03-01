###Problem 1 Answers

### Calendar:
- Audience: contributors, visitors, project managers (everyone); 
- Data: 
	1. pull requests per date: `/repos/:owner/:repo/pulls`, get `created_at`.
	2. issues opened per date: `/repos/:owner/:repo/issues`, get `created_at`.
	3. commits per date: `/repos/:owner/:repo/commits`, get all for each `date`.
- Many Pushes: If this happens, then the single date will become the darkest
color on the scale. To ensure that a clear gradient is established, the scale
itself could dynamically scale based on the total number of degrees of magnitude.

### Contributors:
- Audience: contributors, project managers;
- Data: 
	1. contributors: `/repos/:owner/:repo/events`, then go through the JSON file and find all
		of the individuals who have made commits.
	2. number of pushes to master per date: `/repos/:owner/:repo/events`.
	3. lines added/removed per push: `/repos/:owner/:repo/commits`, 
		then `/repos/:owner/:repo/commits/:sha` for each commit. In `stats`, get `additions` and `deletions`.
- Many Pushes: If this happens, then the scale of the graph will change. One could
simply increase the size of each user's display window in the screen to ensure the
most frequent contributors are still able to show some commits in their chart.

###Commit Activity:
- Audience: contributors, project managers (mostly the latter);
- Data: 
	1. commits per date: `/repos/:owner/:repo/commits`, and for each, get `date`.
- Many Pushes: This would throw off the scale of the bar graph - to fix this, the bar
graph would have to be dynamic between weeks in the week view.

###Code Frequency:
- Audience: contributors, project managers (mostly the former);
- Data: 
	1. additions/deletions per date `/repos/:owner/:repo/commits`, 
		then `/repos/:owner/:repo/commits/:sha` for each commit. In `stats`, get `additions` and `deletions`.
- Many Pushes: This would potentially alter the scale of the graph, however if the
pushes are that frequent, each would probably not contain a great deal of changes,
therefore it would not likely present a huge problem.

###Punchcard: 
- Audience: project managers;
- Data: 
	1. Number of commits per date: commits per date: `/repos/:owner/:repo/commits`, get all for each `date`.
	2. Time of commit: parse out the time from above.
- Many Pushes: This could present a problem of the scale of the circles - to adjust this,
perhaps adding layered circles would help, e.g. using red for the first 10, orange for
the next 10, etc., layered on top of each other.

###Pulse: 
- Audience: contributors, project managers;
- Data: 
	1. proposed pull requests: `/repos/:owner/:repo/pulls`, get `created_at` for date.
	2. merge requests
	3. active & new issues: `/issues`, get `created_at`, as well as `closed_at`.
	4. commits: `/repos/:owner/:repo/commits`, get all for each `date`. 
	5. branches
	6. authors
	7. additions/deletions: `/repos/:owner/:repo/commits`, 
		then `/repos/:owner/:repo/commits/:sha` for each commit. In `stats`, get `additions` and `deletions`.
	8. files
	9. commit comments: `/repos/:owner/:repo/comments`, as well as each `created_at`.
- Many Pushes: