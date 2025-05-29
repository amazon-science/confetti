## ConFETTI: Conversational Function-Calling Evaluation Through Turn-Level Interactions 

ConFETTI is a Conversational Function-Calling
benchmark that works on the turn-level. 
The benchmark is designed to evaluate function-calling 
capabilities and response quality of large language models
(LLMs). Current benchmarks lack comprehensive
assessment of LLMs in complex conversational
scenarios. CONFETTI addresses this gap through
109 human-simulated conversations, comprising
313 user turns and covering 86 APIs.


### Conversation Complexities 

These conversations explicitly target various conversational
complexities, such as follow-ups, goal correction
and switching, ambiguous and implicit goals. Below is a list of all included complexities 
and the number of dialogs covering those complexities. 

| COMPLEXITY                | # DIALOGS | DESCRIPTION |
|---------------------------|-----------|-------------|
| EXCEPTION_IN_EXECUTION    | 5 | Errors or exceptions that occur during the execution of an action |
| FAILED_CONVERSATION       | 5 | Interactions where the intended goal is not achieved |
| CONFIRMATION              | 6 | Requesting user approval before executing an action |
| GOAL_SWITCHING            | 6 | When the user changes their objective during the conversation |
| NO_TARGET_COMPLEXITY      | 6 | Conversations without specific complexity requirements |
| GOAL_CORRECTION           | 7 | Adjusting or refining the user's goal based on feedback |
| GOAL_STACKING             | 7 | Managing multiple user objectives simultaneously |
| AMBIGUOUS_GOAL            | 9 | When the user's intention is unclear and requires clarification |
| FOLLOWUP_QUESTION         | 10 | Additional queries or requests for information after the initial response |
| IMPLICIT_DESCRIPTIVE_GOAL | 10 | The user describes a problem/background without directly stating their goal |
| OVERFILL                  | 11 | Providing more information than required for an action |
| UNDERFILL                 | 11 | Missing required arguments or information for an action |
| GOAL_NOT_SUPPORTED        | 15 | The user's request is not supported by the available tools or is out of scope |


### Dialog Acts
We provide dialog act annotation to assess response quality. We include the following dialog acts:
* Agent seeking information (seek_info): targets responses that elicit information from the
user, whether it is intent elicitation, param-
eter elicitation, or asking for clarification or
confirmation.
* Agent informing user (inform): targets responses that provide information to the user,
whether the information is general or specific
to the function-calling results.
* Agent rejecting request (reject): targets responses that reject the user request.
* Other: any response that does not belong to
the previous dialog acts.

### Usage

The data is formatted and structured to work with the Berkeley Function-Calling Leaderboard ([BFCL](https://github.com/ShishirPatil/gorilla/tree/main/berkeley-function-call-leaderboard)).

### Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

### License

This project is licensed under the CC-By-4.0 License. 
