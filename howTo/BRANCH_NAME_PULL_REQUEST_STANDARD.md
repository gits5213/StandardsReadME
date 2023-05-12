## Local Branch Naming Convention based on the Lint 
	® Local Branch naming: test/storyNumber-short-Story-Description
		○ test/2454335-Update-Storage-Account
		○ refactor/2454335-Update-Storage-Account
	® Test class Naming Convention 
		○ Test case class name should contain the user story name and number (i.e. rds-123-story-name) 

## PR Create Standards workflow
	® PR Name as the same name of the local branch name following lint convention 
	® Description: What you have accomplished in this current PR
	® Add pass result screenshot 
	® Add PR Reviewer at least two (1. QA Engineer, 2.Corresponding Developer) 
	

## For Reviewer  Standards workflow
Validate,
	®  Branching naming convention
	® ADO Link
	® PR Description matches with the Story assertion
	® Code matches with the Story assertion 
	® No white space (o unnecessary spaces)
	® No unnecessary comments line
	® Return statement end of the code on the class or file (One Extra Line)
	® Leverages reusable methods for common steps or line of code using on every test cases.
	® Will it be easy to maintain or difficult to change
	® Naming convention for JAVA PL. 
	® Pull the branch in your local and execute based on the README.md file instruction 
		○ Does the code run 
		○ Does the test pass
	® Follow the DRY & KISS principle 
	® Comments on line by line editing 
	® Point out challenges not the solutions
	® Be clear on what is your opinion and what is an objective fact.
	® Test class doesn't contain hard coded (leverage data driven concept)
	® Generate report and it accessible for everyone on the team 
	® For UI: 
		○ Must use CSS locator
		○ Leverage: Data, Keyword driven, Page Object Model Concept
		○ Allure Report / serenity bdd reporter
