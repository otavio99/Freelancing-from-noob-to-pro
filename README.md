# Dummy Utility Token (DUTO) Manager(????)

This project is the initial effort of creating a system that will manage utility tokens that should work more or less like vouchers.

The goal of this project is to enable a token/reward system for people who donate to charity entites, by rewarding them with tokens that can be exchanged in a digital service market that will be created specially to boost the use of the tokens.

### Simple Use Case

For this use case, we are going to have 3 parties: customer, freelancer volunteer, charity volunteer/manager. 
The description of each role is:

- **Customer:** A person who wants to donate and utilize rewarded tokens to exchange for utilities or services in the digital market.
- **Freelancer volunteer:** A person who is willing to offer a small-time service inside the digital market in exchange of tokens and free marketing of their services.
- **Charity Volunteer/Manager:** A person who is in charge of helping charities and is looking for more funding to boost the charity cause

The current scenarios of use are:

```gherkin
Scenario: customers donates to Charity
  Given customers wants to donate $$ reais to a convenied charity entity
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

Scenario: Freelancer receives a request from customer
Scenario: Charity Volunteer notifies donation
```
