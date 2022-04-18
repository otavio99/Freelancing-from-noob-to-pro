# Scenarios

This section will describe scenarios not only for a possible system but for the whole interaction around the token economy, its entire cycle.

For these scenarios, we are going to have 3 parties: customer, freelancer volunteer, charity volunteer/manager.
The description of each role is:

- **Customer:** A person who wants to donate and utilize rewarded tokens to exchange for utilities or services in the digital market.
- **Freelancer volunteer:** A person who is willing to offer a small-time service inside the digital market in exchange of tokens and free marketing of their services.
- **Charity Volunteer/Manager:** A person who is in charge of helping charities and is looking for more funding to boost the charity cause

The current scenarios of use are:

```gherkin
Rule: There is a defined amount $$ per token
  Scenario: customers donates to Charity
    Given customers wants to donated $$ (money) to a convenied charity entity
    When customers donates, they sends their id with donation to charity manager
    Then customers register to their side of the system the receip for the donation (pix/ted/doc)

Scenario: Charity Manager notifies donation
  Given donation received from customers plus their ids
  When the charity manager identifies donation in the bank account
  Then charity manager goes to their side of the system a notifies donation by inputing amount, id, and proof of donation

Scenario: customers get confirmation for their donation
  Given customers have donate a given amount to charity entity
  When the donation is confirmed by charity manager
  Then customers are notified
    And will be able to see the token at their balance

Scenario: Customers go to marketplace
  Given customers with tokens
  When they want to exchange their tokens for services
  Then they go to the marketplace to look for services they might be interested in

Scenario: Customers wants to exchange token for a service
  Given customers have found the desired service
  When verify if the token they have available has enough for service
  Then they can request service by notifying freelancer at the market place

Rule: Freelancer can only take X number of requests per week
  Scenario: Freelancer take request to provide service
    Given freelancer received a notification about a user request
    When freelancer confirm availability to take request
    Then freelancer poke customer to start the service providing process

Scenario: Charity Volunteer notifies donation
```
