
## Testing Contract: Voting

All functions are covered with 42 passing tests.

### Testing Modifier OnlyOwner
* onlyOwner should be able to addvoter (474ms)
* onlyOwner should be able to StartProposalRegistering (168ms)
* onlyOwner should be able to endProposalsRegistering (166ms)
* onlyOwner should be able to startVotingSession (216ms)
* onlyOwner should be able to endVotingSession (146ms)
* onlyOwner should be able to tallyVotes (108ms)
### Testing Modifier OnlyVoter
* onlyVoters should be able to getVoter (44ms)
* onlyVoters should be able to getOneProposal (39ms)
* onlyVoters should be able to addProposal (214ms)
* onlyVoters should be able to setVote (272ms)
### Testing All Requires
* owner should add voters only during RegisteringVoters state (393ms)
* voter should be registered only once (399ms)
* voter should add proposals only during ProposalsRegistration state (348ms)
* voter should NOT add empty proposal (651ms)
* voter should vote only during VotingSession state (274ms)
* voter should vote only once (1331ms)
* voter should vote for an existing proposal (901ms)
* proposal registration should start after registering voters (298ms)
* end of proposal registration should start after registering proposals (173ms)
* voting session should start after end of registering proposals (86ms)
* ending voting session should start during voting session (111ms)
* tally votes should start after ending voting session (82ms)
### Testing Common Events submission
* should emit a VoterRegistered event (251ms)
* should emit a ProposalRegistered event (420ms)
* should emit a Voted event (750ms)
### Testing State Events submission
* should emit a WorkflowStatus event for starting proposal registering (113ms)
* should emit a WorkflowStatus event for ending proposal registering (99ms)
* should emit a WorkflowStatus event for starting voting session (109ms)
* should emit a WorkflowStatus event for ending voting session (120ms)
* should emit a WorkflowStatus event for ending voting session (121ms)
### Testing Registering Voter
* should register a voter (367ms)
### Testing Registering Proposals
* should add one proposal in the proposals array (179ms)
* should add many proposals in the proposals array (1442ms)
### Testing Vote
* should save the proposalId that the voter has chosen (250ms)
* should save the fact that the voter has voted (190ms)
* should increment proposal vote count (232ms)
### Testing State Change
* should start with RegisteringVoters status (67ms)
* should change to ProposalsRegistrationStarted status (155ms)
* should change to ProposalsRegistrationEnded status (162ms)
* should change to VotingSessionStarted status (148ms)
* should change to VotingSessionEnded status (195ms)
### Testing tally votes
* should tallyVotes (1827ms)


42 passing (21s)
