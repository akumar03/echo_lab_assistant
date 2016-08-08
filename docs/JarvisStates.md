# JarvisStates File
A file containing all of the Jarvis States.

## AuthenticateState Class
Checks if their is a user currently logged in.
If not it transitions to LoginState. If their is
it transtitions to the GetIntentState

## GetIntentState Class
Gets the users intent and then redirects the request to the proper
state.

## ExpeirmentOpenCloseState Class
Get here from the GetIntentState. Either opens or
closes and experiments based on the users intent.
If Opened, can return IntentState if successfull or ReturnState
if unsuccessfull. If Experiment close intent then always returns ReturnState.

## LogoutState Class
Clears the current user logged in and closes experiment.
Logs user out. Returns ReturnState.

## LoginState Class
If a username is provided logs user in. If not tells user to provide a username.
Always returns ReturnState

## ValidateState Class
Checks if the intent is valid based on your previous actions. Can return either ReturnState if
it is an error or IntentState if it is valid.

## IntentState
Calls the correct method based on the users Intent. Can be either an Experiment Intent or a Get Intent
Always returns ReturnState

## ReturnState
Returns a response. Does not return the name of the next state like the other states but instead
returns a response based on the previous states

