# COVID-19 Contact-Tracing Apps

This repository is intended to aggregate system overviews for the various projects that are working on app-based contact-tracing solutions for the COVID-19 pandemic. Its purpose is to make it easier for experts to evaluate the system architectures and to help facilitate dialog between the projects and the privacy-advocacy community.

## COVID-19 Tracing Apps

* #### [TraceTogether](https://www.tracetogether.gov.sg/) (Singapore)
	**Status**: ~735,000 users

	https://www.tracetogether.gov.sg/common/privacystatement/


* #### [CoEpi](https://www.coepi.org) | Community Epidemiology In Action

	**Status**: In development

	**Technical synopsis**

	The CoEpi app uses Bluetooth to record a list of Interactions with other users.

	* In an Interaction, apps exchange temporary Contact-Event-Numbers (CEN). The other user's CEN is stored along with a timestamp for when the interaction occurred.
	* Temporary CENs are deterministically generated from a cryptographic Key, which is private by default.
	* User can choose to upload their Key, along with symptoms, to a public database
	* The app downloads Keys and their associated Symptoms from the public database and searches local Interactions records to determine if any of the User's interactions were with symptomatic users
	* No location data is captured

* #### [Private Kit: Safe Paths](http://safepaths.mit.edu/)

	**Status**: Apps are live, backends and agency integrations in development

	**Technical synopsis**

	The Safe Paths app saves the user's GPS location data to a local encrypted store.

	* When a user tests positive, they can choose to give their location records to a health professional, who then manually redacts personally-identifiable information and publishes the redacted data to a public database.
	* The app downloads location data of infected cases to search against locally-stored location history

**Need more info:**

* [enigmampc/SafeTrace](https://github.com/enigmampc/SafeTrace) ?
* [corona-trace](https://corona-trace.github.io/) ?
* https://covid19.privicy.com/ ?

## Related trackers

* [Privacy International: Tracking the Global Response to COVID-19](https://privacyinternational.org/examples/tracking-global-response-covid-19)
* [Top10VPN COVID-19 Digital Rights Tracker](https://www.top10vpn.com/news/surveillance/covid-19-digital-rights-tracker/)

## Are you developing a Tracing App?

**Guidelines, suggestions, and requests from the community**

Here are some things that privacy and digital rights advocates would like you to consider as you are implementing a tracing solution:

[Privacy/digital-rights experts: help fill in this section!]

* DO
	* PR an overview of your system into this repo
	* Clearly and regularly let users know what information is being collected, where it is going, and how it could put them at risk
		* If you aren't sure how the information you are collecting could put users at risk, STOP!, slow down, and post an issue to this repo asking for help understanding the implications of your design.
* DON'T
	* Collect "analytics"

## Threat scenarios

* The One-Interaction-User scenario
	* Sequence
		1. Over the course of two weeks, User A only comes near one other user, User B
		2. User B tests positive and uploads case data
		3. User A receives a notification that they've been exposed
		4. User A knows that User B is infected
* ...

## Meta

As the list above becomes more complete, this page will likely become a table with links to the more in-depth system overviews. We're pondering how to aggregate and present community concerns and discussion about the individual projects.

## I want to contribute to covid-apps-tracker

Great! It's easy:

1. Agree with our [Code of Conduct](./CODE_OF_CONDUCT.md)
2. Post an Issue or PR to this repository
