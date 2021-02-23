# Naming conventions

Just initial ideas so that there is some consistency. Very much open to change as they are road tested

## Web pages

> {TopLevelArea}/{PageSubject}

Pascal Case (without spaces)

e.g. 
- BulkyWaste/StartHere
- BulkyWaste/WasteItemsList
- BulkyWaste/Complete

## Web templates

### General use templates

> {GenericOrProjectSpecificDefinition}

or

> {Framework}/{Definition}

Pascal Case (without spaces)

e.g.
- FullPageText
- FullPageWithEntityList
- GDS/TaskList
- GDS/CheckYourAnswers

### Page-specific templates

> {TopLevelArea}/{PageSubject}

e.g.
- BulkyWaste/StartHere
- BulkyWaste/WasteItemsList
- BulkyWaste/Complete

To be avoided when possible but often required.

When page-specific templates are required, it is often a sign that general use templates can be refactored or a new general use template created

## Page templates

### General use templates

> {GenericOrProjectSpecificDefinition}

or

> {Framework}/{Definition}

Pascal Case (without spaces)

e.g.
- FullPageText
- FullPageWithEntityList
- GDS/TaskList
- GDS/CheckYourAnswers

### Page-specific templates

> {TopLevelArea}/{PageSubject}

e.g.
- BulkyWaste/StartHere
- BulkyWaste/WasteItemsList
- BulkyWaste/Complete

Don't automatically assume that every web template requires a page template. Try to keep the number of Page Templates to a minimum.

## Site settings

> {TopLevelGroup}/{SubCategory}/{UniqueSetting}

Site settings are globally accessible so best practice to use for parameterised logic. This list can get very long so spending time to properly categorise is worth the investment.

Site setting keys are often used in web templates so refactoring down the line can be tricky.

e.g. 
- Authentication/LoginThrottling/IpAddressTimeoutTimeSpan
- Authentication/LoginThrottling/MaxAttemptsTimeLimitTimeSpan
- GrantAllowance/Adult/Value
- GrantAllowance/Child/Value

## Content snippets

> General/{Description}

or

> {Area}/{Page}/{Description}

or

> {Area}/{Page}/{Description}/{Value}

Content snippets are globally accessible so useful to use for shared content on multiple pages or variable page content.

This list can get very long so spending time to properly categorise is worth the investment.

Content snippet keys are often used in web templates so refactoring down the line can be tricky.

e.g.
- General/WhatHappensNextHeader
- General/WhatYouNeedHeader
- General/SignInText

or  

- GrantAllowance/StartHere/WhatYouNeed
- GrantAllowance/Complete/WhatHappensNext

or

- GrantAllowance/Complete/Status/Active
- GrantAllowance/Complete/Status/Inactive

## Entity forms

> {Area}/{Page}

or

> {Entity}/{Description}/{Destination}

Entity forms (and potentially Web forms) are the most likely to require a different convention in different projects, depending on the design of entity forms per page or re-use of forms over many web pages. 

e.g. 
- GrantAllowance/FamilyDetails
- GrantAllowance/CompleteService

or

- Contact/ContactDetails/ToMarketingPreferences
- Contact/MarketingPreferences/ToCheckYourAnswers

## Entity lists

> {Area}/{Entity}

or

> {Entity}/{View}/{Use}

or 

> {Entity}/{Use}

e.g.
- GrantAllowance/Benefits

or

- Contact/ContactsBeingFollowed/MapView
- BookableResourceBookings/ODataFeed

## Web roles

> {Persona Definition}

or 

> {Area}/{PersonaDefinition}

Choice depends on the security structure developed, whether it is simple persona-based or based on areas and hierarchy.

e.g. 
- Authenticated User
- Grant Manager

or 

- GrantManagement/Administrator
- GrantManagement/Approver
- TravelCentre/Administrator

## Entity permissions

> {Entity}/{PrivilegesList}

or

> {Entity}/{PrivilegesList}/{Filter}

Most cases will be covered with the first, but more complex security set ups require more detail which should be visible in longer lists of permissions 

e.g. 
- Contact/CreateReadWrite
- Case/Write/WhereContactsAccountIsCustomer

