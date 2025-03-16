# University of South Carolina - Division of Information Technology<br/>GitHub Runner README
> [!NOTE]
> Version 1.0

This github page is here to document the University of South Carolina's Division of Information Technology's usage of **[GitHub Runners](https://docs.github.com/en/actions/using-github-hosted-runners/using-github-hosted-runners/about-github-hosted-runners)**.

GitHub Runners are **virtual machines** that are responsible for executing workflows defined in a repository using YAML or JSON. These workflows are triggered by events specified in push or pull requests or scheduled tasks. When a workflow runs, a runner sees the job and executes each step sequentially. GitHib provides runners running on platforms such as Ubuntu or Windows and come preconfigured with development tools.

# The Use Case for the Division of Information Technology

The **Division of Information Technology** is using GitHub Runners to assist in the automation of requesting a firewall rule change from within the university's network. To get into specifics, the runners' goal is to pull from the [ServiceNow](https://www.servicenow.com/docs/bundle/yokohama-api-reference/page/build/applications/concept/api-rest.html) API to grab information from a ServiceNow request and bring that data to a vCloud server and have that information run through a Python script to query a database to validate the firewall rule request, and if the rule doesn't yet exist, to forward the request to a firewall squad to review the request before further action. Using GitHub Runners will remove most of the current human interaction from the firewall request process and will only notify team members when a rule has not been made so that they can review its parameters before moving forward.
