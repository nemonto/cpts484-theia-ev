# Domain, Stakeholders, Objectives:
- Issue 1: Stakeholders Role
	- Classification: Ambiguous
	- Reason: Staff members and police are included as stakeholders but their role and responsibilities are not made explicit
- Issue 2: Connected Buildings
	- Classification: Inconsistent
	- Reason: The domain is a single multi-floor building that users are assumed to be familiar with, but this objective adds routes between connected buildings without saying whether connectors are in scope.
- Issue 3: Domain definition with shared spaces
	- Classification: Ambiguous
	- Reason: The assumptions masterlist states that navigation does not include inside of rooms, only from one location to another. This needs to be addressed if a location is only accessible via passing through another room(reaching a conference room within a library).

# Functional Requirements:
- Issue 1: Figuring out what the next action(s) would be, based on the user's schedule or habit, and suggesting/accepting  the user's choice
	- Classification: Ambiguous
	- Reason: How does it "figure out" those actions, is it by path history, by the initial setup of the caretaker
- Issue 2: Placing emergency calls and messages, possibly after detecting a fall or when the system has lost its current location
	- Classification: Unsound
	- Reason: Losing the location happens routinely (between beacons, phone in a pocket), treating it as an emergency would cause false alarms, and it doesn't say who gets called or whether the user confirms first.
- Issue 3: Directional and Distance metrics
	- Classification: Ambiguous
	- Reason: The current preliminary definition isn't clear on how to comminate to a user how long they should walk for. We also need to alert the user if they need to walk along a bended sidewalk or walk around a statue or fountain.  

#  Non-Functional Requirements:
- Issue 1: The system shall be "ubiquitous"
	- Classification: Ambiguous
	- Reason: Ubiquitous does not explicitly describe what is being tested or the grounds for testing.
- Issue 2: The system shall lead the user through the fastest route
	- Classification: Ambiguous
	- Reason: It doesn't define on what is considered fastest (e.g. quickest route by speed, or distance, turns, etc., safest)
- Issue 3: Safe Navigation, Fast Navigation, Comfortable Navigation
	- Classification: Incomplete 
	- Reason: Doesn't specify on what exactly each of these modes do in the functional requirements
- Issue 4: "The system shall be customizable to every user" vs. "the caretaker sets the configuration of the app"
	- Classification: Inconsistent
	- Reason: Chapter 1 says the caretaker sets the configuration but Chapter 3 says each user can customize it (volume, instruction interval), so it's unclear who can change settings.
- Issue 5: Alerting nearby pedestrians 
	- Classification: Incomplete
	- Reason: While detecting pedestrians is out of scope it is important that nearby pedestrians are alerted to step out of the way of where a user is walking through. 


# Possible redundancies: 
- Issue 1: Coverage of Multiple Floors
	- Classification: Incomplete
	- Reason: Requirements mention navigation between each classroom in building but doles not account for using staircase or using elevator
	- Reason for removal: Master list assumes user can operate stairs or elevators. 

