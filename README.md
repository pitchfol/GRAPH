# GRAPH

**Example User Story:**
As a MS Teams Admin,
I want to see all Teams and their Members,
So that I can administer and report on the count of teams and their spread of members across my organisation

**Setup:**
Each query will:
  - request data based on permissions assigned to an Azure hosted App, see: https://docs.microsoft.com/en-us/graph/auth-v2-service for details.
  - need the Client Credentials and Client Secret of the App setup with Graph Permissions assigned. This can be set as a parameter instead of hardcoding if you prefer.
  - need the domain of your tenant added to the auth login, for example "ACMECOMPANY" "RelativePath = "/ACMECOMPANY.onmicrosoft.com/oauth2/token?api-version=1.0"
  - return a single dataset that can then be joined against the respective ID (Group id, User id) to show which Users are members of each Team.

Report:
A single report can be built to return a view, as an example, of the current count of MS Teams, User's in at least one team and Members per team in your organisation.
