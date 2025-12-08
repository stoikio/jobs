# Go Senior Backend Engineer — Technical test

## Introduction

We want to build an **Email Security** tool to flag emails with potential financial fraud attempts (fake president, fake supplier, etc.) that are received by our clients. We focus on clients that are using Google Workspace and Microsoft O365 so users and emails can be retrieved through relevant APIs. 

The goal of this test is to:
- design the entire architecture of a system that is reliable and scalable.
- code the service retrieving the emails. 
- reflect on how to flag such emails: (1) enumerate feature ideas in the readme, (2) think about the pipeline. 

## Requirements

### Must have

- Use excalidraw or similar tool to write down the architecture
- Build the service in Go
- Use PostreSQL
- Dockerize the service
- Tests

### Liberties 

You can assume the following functions (or very similar variants) exist (and mock them).

```go
func GetMicrosoftUsers(tenantID uuid.UUID) ([]MicrosoftUser, error) 
func GetMicrosoftEmails(userID uuid.UUID, receivedAfter time.Time, orderBy string) ([]MicrosoftEmail, error)
func GetGoogleUsers(tenantID uuid.UUID) ([]GoogleUser, error)
func GetGoogleEmails(userID uuid.UUID, receivedAfter time.Time, orderBy string) ([]GoogleEmail, error)

```


## What we will look for
- Do you a clear plan to make the design evolve towards a system supporting 10 million emails / day?
- How your system will cope with failures and spikes in the workload?
- Do you have interesting ideas, can discuss them with energy and can execute efficiently?
- Are you able to switch from macro view to micro details?
- Is the discussion constructive?
