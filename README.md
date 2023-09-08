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

Hi,

Thanks for reaching out to GitHub Support.

I understand that you are having trouble adding a team to a repo using the GitHub API. I've reviewed the command you provided and I can see that you are missing ***permission attribute*** used to determine what permission is granted to the team. The permission property is required to add a team to a repo.

The correct curl command would be:

curl -H "Authorization: token BLAHBLAHBLAH" -H "Content-Type: application/json" -X put -d '{"permission":"pull"}' [https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name](https://hostname/api/v3/organizations/10/team/23/repos/jimmy/some-repo-name)

This command will add the team ***23*** to the repo ***some-repo-name*** with the ***pull*** permission.

I have also added some a link to the rest API documentation for further clarification. This should help you to understand the request better and to troubleshoot the issue if you continue to have problems.

[https://docs.github.com/en/enterprise-server@3.10/rest/teams/teams?apiVersion=2022-11-28#add-or-update-team-project-permissions](https://docs.github.com/en/enterprise-server@3.10/rest/teams/teams?apiVersion=2022-11-28#add-or-update-team-project-permissions)

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

Hello,

Thanks for reaching out to GitHub Support.

Based on the information you have provided, it shows that your environment is experiencing some performance issues. Here are a few things that could be causing these issues:

- **High CPU usage:** The load average output of uptime shows that the CPU is being heavily utilized. This could be due to a number of factors, such as a large number of concurrent users, a large number of open files, or a resource-intensive process running on the server.

- **Disk I/O contention:** The system could also be experiencing disk I/O contention, which can occur when multiple processes are trying to access the disk at the same time. This can cause delays in file operations, such as Git operations.

- **Low memory:** The free output shows that there is only 683 MB of free memory available. This is not a lot of memory, and it could be causing the system to swap, which can significantly impact performance.

To mitigate these issues, you can try the following:


* **Reduce the number of concurrent users:** You can try reducing the number of users who have access in your environment. You can also try limiting the number of concurrent connections that each user can have.

* **Close unused files:** The lsof command tcan be used to list open files on the system and you can close any files that are not being used.

* **Identify and kill resource-intensive processes:** The top command can be used to list all of the running processes on the system, you can identify and kill any processes that are using a lot of CPU or memory.

* **Increase the amount of memory available:** You can increase the amount of memory allocated.

* **Optimize the disk I/O:** You can try optimizing the disk I/O by using a faster disk or by adding more disks to the system.

If you have tried these steps and you are still experiencing performance issues, you can contact us for further assistance.

I hope this helps! Let me know if you have any other questions.

Best Regards

Olumide Olowe

### Question 3

You receive a ticket from ACME, Inc. asking if it's possible to adjust GitHub Enterprise's web interface to match their corporate identity better.

> Hi, At ACME, Inc. we have many services running in-house, all matching our orange colored corporate design and showing the ACME, Inc. logo. GitHub Enterprise is the only service that does not seem to support this. How can we alter GitHub Enterprise's design?

GitHub currently does not support modifications to GitHub Enterprise's web interface for two reasons:

- GitHub Enterprise was designed to match GitHub.com to preserve the familiarity many software developers around the world have already acquired on GitHub.com. Changing the GitHub user experience by altering its design could be too confusing for the people actually using our product.
- Changing GitHub Enterprise's design would only be a cosmetic change. It wouldn't have a huge impact on improving how people collaborate and work together as other features we could be working on. There are other items on our product's roadmap with a higher prioritization.

Taking these reasons into account, how would you respond to the customer using your own words?

### Question #3 response:

Hi,

Thanks for reaching out to GitHub Support.

I understand that you would like to adjust GitHub Enterprise's web interface to match your corporate identity better. I appreciate your interest in GitHub Enterprise, and I want to make sure that you are happy with your experience.

Unfortunately, GitHub currently does not support modifications to GitHub Enterprise's web interface. There are two main reasons for this:

- GitHub Enterprise was designed to match GitHub.com to preserve the familiarity many software developers around the world have already acquired on GitHub.com. Changing the GitHub user experience by altering its design could be too confusing for the people actually using our product.
- Changing GitHub Enterprise's design would only be a cosmetic change. It wouldn't have a huge impact on improving how people collaborate and work together as other features we could be working on. There are other items on our product's roadmap with a higher prioritization.

I know, this may not be the answer you were hoping for, but I hope you understand our reasoning.

I would like to offer you a few suggestions that may help you achieve your goal of matching GitHub Enterprise's web interface to your corporate identity:

- You could use a custom theme for your GitHub Enterprise instance. There are a number of third-party themes available that you can use to change the look and feel of GitHub Enterprise. Here is a link to GitHub supported themes (https://pages.github.com/themes/)[https://pages.github.com/themes/]
- You could use a custom logo for your GitHub Enterprise instance. You can upload your own logo to GitHub Enterprise and it will be displayed in the header of the web interface.
- You could use a custom domain name for your GitHub Enterprise instance. This will make your GitHub Enterprise instance look more like a part of your corporate website.

I hope these suggestions are helpful. Please let me know if you have any other questions.

Thanks,

Olumide Olowe

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

Hi,

Thanks for reaching out to GitHub Support.

I understand that you are experiencing an SSL certificate issue after installing the latest update to your GitHub Enterprise instance. I appreciate your patience as we work to resolve this issue.

The error message indicates that the SSL certificate for your GitHub Enterprise instance is not being verified by the client. This can happen for a few reasons, such as:

- The certificate is not trusted by the client's operating system or browser.
- The certificate is expired or invalid.

In your local CA certificate store you have certs from trusted Certificate Authorities that you then can use to verify that the server certificates you see are valid. They are signed by one of the certificate authorities you trust.

To troubleshoot this issue, I would recommend you do the following:

- I would like you to confirm if you are using a self-signed or a certificate signed by a certificate authority (CA). Verify that the certificate is trusted by the client's operating system or browser. 
    - You can do this by opening the certificate in a text editor and looking for the "Issuer" and "Subject" fields. The Issuer should be a trusted certificate authority, such as Let's Encrypt, DigiCert, Comodo, RapidSSL, Sectigo. The Subject should be the name of your GitHub Enterprise instance.
    
- Check the expiration date of the certificate. The certificate should be valid for at least 90 days.

- You can also check to see if the client's clock is synchronized. This can be done by running the date command and then adjusting the time as needed.

I would recommend you contact your system administrator to help check and verify the certificate.

I hope this helps! I will await your feedback.

Thanks,

Olumide Olowe
