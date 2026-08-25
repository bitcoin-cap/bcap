# Analyzing Bitcoin Consensus: Risks in Protocol Upgrades

Original Authors (V1): Ren Crypto Fish, Steve Lee, Lyn Alden

Thank you to the following people who reviewed drafts of the initial project, providing valuable feedback to improve the quality of the project:

Mat Balez, Jay Beddict, Jeff Booth, Joe Carlasare, Hong Fang, David Harding, Avichal Garg, Gwart, Chaitanya Jain, Shirish Jajodia, Hong Kim, David King, Jameson Lopp, Shehzan Maredia, Sanjay Mavinkurve, Murch, Matt Odell, John Pfeffer, Reardencode, Bradley Rettler, Rijndael, Pierre Rochard, AJ Towns, 0xkrane, jesmros

# Table of contents

- [Introduction](#introduction)
- [What is Bitcoin Consensus](#what-is-bitcoin-consensus)
	- [Technical Aspects of Consensus](#technical-aspects-of-consensus)
	- [How are changes activated](#how-are-changes-activated)
		- [Soft Forks vs Hard Forks](#soft-forks-vs-hard-forks)
		- [Historical Activation Mechanisms](#historical-activation-mechanisms)
	- [What maintains Bitcoin Consensus](#what-maintains-bitcoin-consensus)
		- [State of Mind](#state-of-mind)
		- [Stakeholders](#stakeholders)
			- [Economic Nodes](#economic-nodes)
			- [Investors](#investors)
			- [Media Influencers](#media-influencers)
			- [Miners](#miners)
			- [Protocol Developers](#protocol-developers)
			- [Users and Application Developers](#users-and-application-developers)
		- [Consensus Game Theory](#consensus-game-theory)
			- [How is Consensus Change attained](#how-is-consensus-change-attained)
			- [Stakeholder powers during a consensus change](#stakeholder-powers-during-a-consensus-change)
		- [How to measure Consensus](#how-to-measure-consensus)
		- [Future Scenarios and Considerations](#future-scenarios-and-considerations)
			- [Consensus changes with alternative clients](#consensus-changes-with-alternative-clients)
			- [What is a chain split](#what-is-a-chain-split)
	- [Recommendations](#recommendations)
		- [Proposals Maturing Toward Possible Consensus](#proposals-maturing-toward-possible-consensus)
		- [Key Questions for Stakeholders](#key-questions-for-stakeholders)
		- [Determining Consensus](#determining-consensus)
- [Appendix](#appendix)
  
# Introduction

This paper provides an analysis of bitcoin’s consensus mechanism, focusing on the roles of various stakeholders, their powers, and the incentives that guide their actions. Bitcoin is incredibly difficult to change by design. The default is no change. Any significant change needs to pass that hurdle. We categorize the roles people play in bitcoin's consensus into [six distinct stakeholder groups](#stakeholders), each with their own motivations and influence. We also notice that the relative powers of the stakeholders shift depending on their role in the network’s operation and the stage of the consensus change process. Notably, while [Bitcoin Core maintainers](#protocol-developers) do not have excessive power to change Bitcoin, they possess significant power to veto changes. We also introduce the concept of [State of Mind](#state-of-mind), which affects the degree that stakeholders engage in the process of finding consensus.

Historically, changes to Bitcoin's consensus have typically followed a smooth path. However, it is essential to thoroughly explore and understand potential future scenarios that may be more contentious and could lead to a fragile network. This paper presents [a novel analysis](#consensus-changes-with-alternative-clients) of the challenges and risks associated with adopting alternative clients. Although alternative clients are an important option, their adoption is difficult to achieve. Soft fork consensus changes can be partially deployed without full consensus, creating a fragile network prone to forks with [uncertain outcomes](#upgrade-paths-with-alternative-consensus-clients). During a soft fork, investors also have less power than other stakeholders. We highlight the [risks of bounty claims](#how-might-this-occur-with-a-soft-fork) in contentious consensus change scenarios involving a

*Note: This analysis incorporates quantified thresholds derived from a Bitcoin fork simulation study (Foytik, 2024, arXiv:2608.05461) to provide resolution to qualitative descriptions of stakeholder dynamics.*

## Economic Nodes

Economic Node adoption rates significantly impact chain split risks. Simulation data suggests specific thresholds for these dynamics: an economic cascade floor at $E < 0.50$, an inversion zone between $E \in [0.50, 0.82]$, and an economic override when $E > 0.82$. A self-sustaining consensus point is observed around $E \approx 0.74$ [^1].

## Stakeholder powers during a consensus change

The sequencing of stakeholder actions is critical. Simulations indicate that miner signaling often precedes widespread economic adoption during a consensus change.

## How to measure Consensus

While prediction markets are a potential future measurement tool, a Random Forest probability surface fit to simulated outcomes can provide a quantified stand-in for the probability of a fork resolving toward new rules as a function of economic and mining conditions.

## Determining Consensus

- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...
- [ ]...

*The simulation's ~2,200:1 economic-vs-user weight ratio provides a quantitative basis for the observation that user-node impact is difficult to track [^2].*

[^1]: Foytik, P. (2024). Quantifying Bitcoin Network Resilience Through Critical Scenario Discovery. arXiv:2608.05461.
[^2]: Foytik, P. (2024). Quantifying Bitcoin Network Resilience Through Critical Scenario Discovery. arXiv:2608.05461.