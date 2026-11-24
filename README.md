
# FitGear Anniversary Email & SMS Campaign | Salesforce Marketing Cloud & AMPscript

## Project Overview

A personalized customer anniversary campaign developed for FitGear, a fictional online sports retailer.

Built in Salesforce Marketing Cloud (SFMC), using HTML and AMPscript, the project demonstrates purchase-based discount calculations, conditional messaging, dynamic content, and personalized redemption links across email and SMS.

## Business Scenario

FitGear wants to celebrate customers reaching their one-year anniversary by rewarding their loyalty with personalized discounts.

Instead of offering the same discount to every customer, the campaign uses total yearly spend and average basket size to assign discounts ranging from 10% to 30%.

The campaign consists of two communications:

| Communication | Timing | Purpose |
|---|---|---|
| Anniversary Email | Customer's first anniversary | Celebrate customer loyalty with a personalized discount |
| SMS Reminder | 7 days after email, if the offer remains unredeemed | Remind customers about their anniversary reward |

The SMS follow-up timing and redemption-based audience selection are part of the campaign brief. The submitted implementation focuses on the dynamic email and SMS content.

## AMPscript Features Demonstrated

### 1. Personalization
- Dynamic first-name greetings
- Personalized email subject lines
- Name formatting using Trim() and ProperCase()
- Fallback greetings for missing first names

### 2. Conditional Messaging
- IF / ELSEIF / ELSE / ENDIF statements
- Nested conditional logic
- Purchase-based anniversary messages
- Customer-specific discount assignment

### 3. Data Extension Lookups
- Lookup() to retrieve customer spending information
- CustomerID as the matching identifier
- Retrieval of TotalYearlySpend and AvgBasketSize

### 4. Data Transformation
- Customer name cleaning and formatting
- Discount percentage and reference assignment
- Dynamic redemption URL generation using Concat()

### 5. Dynamic Content
- Personalized email messaging
- Dynamic anniversary discounts from 10% to 30%
- Customer-specific redemption links
- SMS messages based on purchasing behaviour
- RedirectTo() for email redemption links

## Data Extensions

### Anniversary_Audience

Stores customer contact information used for the anniversary email and SMS communications.

**Fields:**
- CustomerID
- FirstName
- LastName
- Email
- Mobile

### MarketingCustomerView

Stores customer information and calculated purchasing metrics used for campaign personalization.

**Fields:**
- CustomerID
- FirstName
- LastName
- Email
- TotalYearlySpend
- AvgBasketSize
- Tenure

CustomerID connects the two Data Extensions.

## Campaign Communications

### 1. Anniversary Email

**Purpose:** Celebrate the customer's first anniversary with FitGear through a personalized discount offer.

**Key Features:**
- Personalized subject line and greeting
- Name formatting and fallback handling
- Customer spending data retrieval
- Nested discount calculation logic
- Dynamic anniversary messaging
- Personalized discount reference
- Dynamic redemption link

### 2. Anniversary SMS Reminder

**Purpose:** Reinforce the anniversary offer through a personalized SMS communication.

**Key Features:**
- Personalized first-name greeting
- Same discount calculation rules as the email
- Dynamic SMS messaging based on average basket size
- Customer-specific discount reference
- Short-form redemption link

## Preview and Testing

The email and SMS messages were previewed using sample customer profiles in Salesforce Marketing Cloud.

Testing focused on:

- First-name formatting and fallback handling
- Customer spending data retrieval
- Discount percentage assignment
- Dynamic email and SMS messaging
- Personalized redemption links
- Consistent discount references across both channels

### Sample Personalization Results

| Customer | Yearly Spend | Avg Basket Size | Discount |
|---|---:|---:|---:|
| John | $505.50 | $50 | 20% |
| Sarah | $1,210.65 | $155 | 30% |
| Missing First Name | $300.00 | $30 | 10% |

These sample profiles demonstrate different personalized messages and discount assignments using the same underlying business rules.

## Project Files

- `01-Anniversary-Email.ampscript` — Anniversary email personalization and discount logic
- `02-Anniversary-SMS.ampscript` — Anniversary SMS personalization and reminder messaging

## Tools and Technologies

- Salesforce Marketing Cloud (SFMC)
- Email Studio
- AMPscript
- HTML
- Data Extensions
- GitHub

## Project Note

This project was completed as part of the AMPscript Academy Capstone 3 assignment.

FitGear is a fictional brand, and the customer information and redemption links are used for educational and portfolio demonstration purposes.

The submitted project demonstrates the personalization logic for email and SMS. It does not represent a deployed automated journey or live campaign performance.
