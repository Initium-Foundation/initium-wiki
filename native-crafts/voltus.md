# Voltus

The main purpose of Voluts is to provide a workflow for activation of Initium network features through community vote based on validator stake weight. This craft implements the new features based on validators voting. Based on Voltus, validators would receive Voltus vote tokens (VOLTUS) based on their staked INIX tokens. Voltus tokens are minted representing the total active stake on the network and distributed to all validators based on their INIX stake. Validators vote for feature activation by transferring their vote tokens to a predetermined address. Once the vote threshold is met, the feature is activated.

Initium validator software will support runtime feature activation through the built-in `Feature` craft. This craft will ensure that features will be activated simultaneously across all validators to avoid divergent behavior that would cause hard forks or otherwise break consensus.
