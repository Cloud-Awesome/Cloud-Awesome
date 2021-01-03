# Power Portals

## Initial notes

- Avoid webforms like the plague
  - And why
  - List the only times when you think they should be used (e.g. save state and return)
    - Possible workarounds to theselimited exceptions
- Prefer liquid over Javascript
- Prefer web templates for re-use and site consistency
	- Define page to types as early as possible (c.f. GDS)
    - Can/should be an output from UX/UR testing
- Strongly prefer calculation of data required for logic as earlier as possible and at least before the required page loads
	- To allow for not using web templates
	- And to promote Liquid over JavaScript
- Record naming conventions
- Consider: prefer external (Azure-hosted) artifacts (JavaScript, etc) to CRM-hosted?

## Liquid

- Preference for liquid over client-side script
- Build Web Templates as re-useable 'classes' that can be used with `{{ include 'template ' }}` when required
- 

## URL structure

- Hackable/predictable
- Hierarchical (e.g. sections and sub-sections)
- 

## Site settings

- Extensive use of settings are easily callable parameters which can be re-used throughout different templates
- Naming convention, to make settings easier to navigate once the list gets bigger

## Web pages

- Avoid custom javascript and/or CSS 
- Prefer using out of the box attributes for unique strings; over conntent snippets; over hard-coded strings

## Content snippets

- 

## CRUD API...