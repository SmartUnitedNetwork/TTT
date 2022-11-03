# TTT THUNDER TREND TOKEN
Smart Contract Audit Report
AUDIT SUMMARY
THUNDER TREND TOKEN Audit ReportTHUNDER TREND TOKEN is a new TRC-20 token on TRON.

For this audit, we reviewed the project team's TronThunderToken contract at TYJt6vAN3KtG7WtgqSQbNFei64DAtnBdbk on the TRON Mainnet.

AUDIT FINDINGS
Please ensure trust in the team prior to investing as they currently own 100% of the total supply.
Date: April 3rd, 2022.
CONTRACT OVERVIEW
The total supply of the token is set to 210 million $TTT [210,000,000].
No mint or burn functions are present; though the circulating supply can be reduced by sending tokens to the 0x..dead address.
At the time of writing this report, 100% of the total supply belongs to the owner.

There are no fees associated with transferring tokens.
The owner can transfer ownership to a new address at any time. When doing so, the current owner's token balance will also be transferred to the new owner.
No other ownership-restricted functionality is present.
As the contract is deployed with Solidity v0.8.6, it is protected from overflows/underflows.
The contract complies with the TRC-20 token standard.
AUDIT RESULTS
Vulnerability Category	Notes	Result
Arbitrary Jump/Storage Write	N/A	PASS
Centralization of Control	The team currently owns 100% of the total supply.	PASS
Compiler Issues	N/A	PASS
Delegate Call to Untrusted Contract	N/A	PASS
Dependence on Predictable Variables	N/A	PASS
Ether/Token Theft	N/A	PASS
Flash Loans	N/A	PASS
Front Running	N/A	PASS
Improper Events	N/A	PASS
Improper Authorization Scheme	N/A	PASS
Integer Over/Underflow	N/A	PASS
Logical Issues	N/A	PASS
Oracle Issues	N/A	PASS
Outdated Compiler Version	N/A	PASS
Race Conditions	N/A	PASS
Reentrancy	N/A	PASS
Signature Issues	N/A	PASS
Unbounded Loops	N/A	PASS
Unused Code	N/A	PASS
Overall Contract Safety	 	PASS

INHERITANCE CHART
Smart Contract Audit - Inheritance

FUNCTION GRAPH
Smart Contract Audit - Graph

FUNCTIONS OVERVIEW

 ($) = payable function
 # = non-constant function
 
 Int = Internal
 Ext = External
 Pub = Public

 +  Context 
    - [Int] _msgSender
    - [Int] _msgData

 +  Ownable (Context)
    - [Pub]  #
    - [Pub] owner
    - [Int] _transferOwnership #

 + [Int] ITRC20 
    - [Ext] totalSupply
    - [Ext] balanceOf
    - [Ext] transfer #
    - [Ext] allowance
    - [Ext] approve #
    - [Ext] transferFrom #

 + [Int] ITRC20Metadata (ITRC20)
    - [Ext] name
    - [Ext] symbol
    - [Ext] decimals

 +  TRC20 (Context, Ownable, ITRC20, ITRC20Metadata)
    - [Pub]  #
    - [Pub] name
    - [Pub] symbol
    - [Pub] decimals
    - [Pub] totalSupply
    - [Pub] transferOwnership #
       - modifiers: onlyOwner
    - [Pub] balanceOf
    - [Pub] transfer #
    - [Pub] allowance
    - [Pub] approve #
    - [Pub] transferFrom #
    - [Int] _transfer #
    - [Int] _mint #
    - [Int] _approve #
    - [Int] _spendAllowance #
    - [Int] _beforeTokenTransfer #
    - [Int] _afterTokenTransfer #

 +  ThunderTrendToken (TRC20)
    - [Pub]  #
       - modifiers: TRC20
ABOUT SOLIDITY FINANCE
Solidity Finance was founded in 2020 and quickly grew to have one of the most experienced and well-equipped smart contract auditing teams in the industry. Our team has conducted 1000+ solidity smart contract audits covering all major project types and protocols, securing a total of over $50 billion U.S. dollars in on-chain value across 1500 projects!.
Our firm is well-reputed in the community and is trusted as a top smart contract auditing company for the review of solidity code, no matter how complex. Our team of experienced solidity smart contract auditors performs audits for tokens, NFTs, crowdsales, marketplaces, gambling games, financial protocols, and more!

Contact us today to get a free quote for a smart contract audit of your project!

WHAT IS A SOLIDITY AUDIT?
Typically, a smart contract audit is a comprehensive review process designed to discover logical errors, security vulnerabilities, and optimization opportunities within code. A Solidity Audit takes this a step further by verifying economic logic to ensure the stability of smart contracts and highlighting privileged functionality to create a report that is easy to understand for developers and community members alike.

HOW DO I INTERPRET THE FINDINGS?
Each of our Findings will be labeled with a Severity level. We always recommend the team resolve High, Medium, and Low severity findings prior to deploying the code to the mainnet. Here is a breakdown on what each Severity level means for the project:

High severity indicates that the issue puts a large number of users' funds at risk and has a high probability of exploitation, or the smart contract contains serious logical issues which can prevent the code from operating as intended.
Medium severity issues are those which place at least some users' funds at risk and has a medium to high probability of exploitation.
Low severity issues have a relatively minor risk association; these issues have a low probability of occurring or may have a minimal impact.
Informational issues pose no immediate risk, but inform the project team of opportunities for gas optimizations and following smart contract security best practices.
