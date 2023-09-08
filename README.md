## Technical Screener, Enterprise / Premium Support

The following is a series of customer questions, most of them coming from real customer interactions. For each question, write a customer-facing response. For questions that you don't know the answers to, feel free to search for answers online and provide the sources you used. Do not invent facts and do not be afraid to ask the customer for information, if needed.

We will be looking at overall content, ability to research technical questions, ability to present a professional yet friendly response to customers, and your ability to intuit details based on very limited information. This questionnaire should take no more than two hours to complete. If you get stuck, don't be afraid to ask us to clarify anything.

A few things to keep in mind:

- It should always be clear to the person on the other side of the computer that you are a smart, friendly, and awesome person.
- Responses should not contain unneeded filler, yet should not be overly brief. They should be complete.
- Responses should have a greeting and closing.
- GitHub is spelled with a capital G and a capital H.
- GitHub is classy. When in doubt: be classy.

### Question 1

You receive the following ticket from a customer:

> Hi GitHub! So according to the docs at [https://docs.github.com/enterprise-server/rest/reference/teams#add-or-update-team-repository-permissions](https://docs.github.com/enterprise-server/rest/reference/teams#add-or-update-team-repository-permissions), I should be able to add teams to a repo programmatically.
> 
> However, this does not work when using the following code:
> 
> curl -H "Authorization: token BLAHBLAHBLAH" -H "Content-Length: 0" -X put -d "" [https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name](https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name)
> 
> Could someone give me a curl one liner that lets me add teams to repos ? Or at least tell me what facet of the documentation has escaped me for the last 45 minutes?

### Question #1 response:

Hi [Your Name],

Thanks for reaching out to GitHub Support.

I understand that you are having trouble adding a team to a repo using the GitHub API. I've reviewed the command you provided and I can see that you are missing ***permission attribute*** used to determine what permission is granted to the team. The permission property is required to add a team to a repo.

The correct curl command would be:

curl -H "Authorization: token BLAHBLAHBLAH" -H "Content-Type: application/json" -X put -d '{"permission":"pull"}' [https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name](https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name)

This command will add the team ***23*** to the repo ***some-repo-name*** with the ***pull*** permission.

I hope this helps! Let me know if you have any other questions.

I have also added some a link to the rest API documentation for further clarification. This should help you to understand the request better and to troubleshoot the issue if you continue to have problems.

(https://docs.github.com/en/enterprise-server@3.10/rest/teams/teams?apiVersion=2022-11-28#add-or-update-team-project-permissions)[https://docs.github.com/en/enterprise-server@3.10/rest/teams/teams?apiVersion=2022-11-28#add-or-update-team-project-permissions]

I hope this helps! Let me know if you have any other questions.

Thanks,
Olumide Olowe

###Question 2

You receive the following ticket from a customer with 1000 GitHub Enterprise Server seats:

> Hi GitHub,
> 
> We are experiencing serious performance issues and receiving multiple complaints from our developers.
> 
> Browsing the web interface often results in timeouts and Git operations are taking magnitudes longer than usual to complete.
> 
> $ free -m total used free shared buffers cached Mem: 15331 14648 683 0 149 6170 -/+ buffers/cache: 8328 7003 Swap: 0 0 0 $ uptime 10:50:08 up 123 days, 25 min, 1 user, load average: 6.25, 5.51, 3.75

What could be causing these performance issues? What would you recommend doing to mitigate these issues?

Notes

You do not have shell or web interface access to their GitHub Enterprise instance.

### Question #2 response:

_replace this with your response_

### Question 3

You receive a ticket from ACME, Inc. asking if it's possible to adjust GitHub Enterprise's web interface to match their corporate identity better.

> Hi, At ACME, Inc. we have many services running in-house, all matching our orange colored corporate design and showing the ACME, Inc. logo. GitHub Enterprise is the only service that does not seem to support this. How can we alter GitHub Enterprise's design?

GitHub currently does not support modifications to GitHub Enterprise's web interface for two reasons:

- GitHub Enterprise was designed to match GitHub.com to preserve the familiarity many software developers around the world have already acquired on GitHub.com. Changing the GitHub user experience by altering its design could be too confusing for the people actually using our product.
- Changing GitHub Enterprise's design would only be a cosmetic change. It wouldn't have a huge impact on improving how people collaborate and work together as other features we could be working on. There are other items on our product's roadmap with a higher prioritization.

Taking these reasons into account, how would you respond to the customer using your own words?

### Question #3 response:

_replace this with your response_

### Question 4

You receive the following ticket from a customer:

> Hi!
> 
> After installing the latest update this morning I noticed that my browsers are now throwing Invalid SSL Cert errors when attempting to access our instance.
> 
> $ curl -I [https://github.acme.edu](https://github.acme.edu/) curl: (60) SSL certificate problem, verify that the CA cert is OK. Details: error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate verify failed More details here: [http://curl.haxx.se/docs/sslcerts.html](http://curl.haxx.se/docs/sslcerts.html)
> 
> Not sure if anyone else has reported this or what I might be able to do to fix it. I've re-uploaded our key & cert file to no avail.

Notes

You do not have shell or web interface access to their GitHub Enterprise instance, so in your reply you'll need to have the customer do any troubleshooting steps and return the results.

### Question #4 response:

_replace this with your response_
