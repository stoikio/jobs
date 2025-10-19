# Go Senior Backend Engineer — Technical test

## Introduction

We want to build an **Email Security** tool to flag emails with potential financial fraud attempts (fake president, fake supplier, etc.) that are received by our clients. We focus on clients that are using Google Workspace and Microsoft O365 so users and emails can be retrieved through relevant APIs. 

The goal of this test is to:
- design the entire system architecture.
- code the service retrieving the emails. 
- reflect on how to flag such emails and enumerate feature ideas.

## Requirements

### Must have

- Use excalidraw or similar tool to write down the architecture
- Build the service in Go
- Use a SQL storage
- Dockerize the service
- Tests

### Liberties 

You can assume the following functions (or very similar variants) exist (and mock them).

```go
func GetMicrosoftUsers(tenantID uuid.UUID) ([]MicrosoftUser, error) 
func GetMicrosoftEmails(userID uuid.UUID, receivedAfter time.Time) ([]MicrosoftEmail, error)
func GetGoogleUsers(tenantID uuid.UUID) ([]GoogleUser, error)
func GetGoogleEmails(userID uuid.UUID, receivedAfter time.Time) ([]GoogleEmail, error)

```


## What we will look for

- Do you have interesting ideas and can execute efficiently?
- Are you able to switch from macro view to micro details?
- Is the discussion constructive?
