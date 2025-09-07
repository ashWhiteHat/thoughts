---
layout: default
title: "Smart Contracts: Ethereum's Failures and Contract Design in the Anonymous Economy"
description: "Analysis of smart contract design challenges in anonymous economies, examining Ethereum's failures and proposing solutions for contract design in decentralized systems."
date: 2024-08-13
categories: [smart-contracts, ethereum, contract-design, anonymous-economy]
---


# Smart Contracts: Ethereum's Failures and Contract Design in the Anonymous Economy

## Overview

The advent of Bitcoin enabled the management of economic value and its ownership transfer over the internet. By attaching conditions to this ownership transfer, it becomes possible to realize a mechanism for automatically executing transactions, similar to a vending machine. This concept was proposed by Nick Szabo as a "smart contract." However, its implementation and operation face numerous challenges. This article reviews concepts related to previously proposed smart contracts and discusses the design of smart contracts.

## Smart Contract

A contract is an agreement between two or more parties to perform specific actions or obligations in a legally binding manner. Controlling this through cryptographic technology and executing it autonomously in a distributed way constitutes the smart contract proposed by Nick Szabo. Representative similar concepts include Bitcoin Script and Ethereum's smart contracts.

## Bitcoin Script

Bitcoin Script is a stack-based language for describing validation rules in Bitcoin transactions. It is primarily used for specifying transfer conditions. Due to its low expressiveness and stateless nature, implementing complex cryptographic protocols or financial applications is difficult.

## Ethereum Smart Contract

Ethereum is a platform designed to perform arbitrary computations on the blockchain. It enables Turing-complete and stateful transaction execution, allowing high expressiveness and flexible implementation of cryptographic protocols and financial applications. Unlike Nick Szabo's concept, it is closer to a general-purpose program, so it is more appropriate to call it a "smart program." This has enabled the implementation of applications such as DAOs and DeFi, but the generalization of functions has led to drawbacks due to design complexity.

## Drawbacks from Generalization

Due to the system's complexity, Ethereum has become heavily reliant on trust. In Ethereum, development is primarily done using the Solidity language, and the completed code is compiled into an executable form for the EVM (Ethereum Virtual Machine). This compiled code is linked to a contract address, and users send transactions by specifying the address and the function to execute.
In smart contract development, the complex processes of code compilation and operation verification make bugs prone to occur. Therefore, service providers must conduct audits (verifications) by specialized agencies to ensure security. These audits require high costs and long periods, placing a significant burden on developers.
Additionally, to verify the legitimacy of transactions when using a contract, users need to check a vast number of opcodes. These opcodes represent interactions and operations between the stack, memory, and storage, but expecting users to verify them is unrealistic. As a result, users trust providers and often sign transactions without confirming their contents. To ensure upgradability, many designs use indirect code references, allowing providers to freely rewrite contracts.
In fact, this complexity caused the DAO incident. To resolve this situation, a rollback was ultimately performed based on community consensus that relied on trust. In other words, due to the system's complexity, the design, operation, and even some consensus mechanisms currently depend on trust. Despite involving important financial contracts related to assets, the prevalence of blind trust is not healthy.

## Toward an Ideal Design

In Bitcoin Script, the limited functionality prevented the implementation of comprehensive smart contracts. On the other hand, Ethereum's generalization of functions resulted in a structural flaw of dependence on provider trust. Therefore, to implement smart contracts in a trustless manner, it is practical to propose simple designs and high-function locking mechanisms as templates tailored to contract types. This can maximize the potential of smart contracts.

## Future Discussions

For future discussions, we will examine the types of contracts conducted in previous anonymous economies and their challenges, as well as the sequences, roles, functionality, and economic and cryptographic principles of establishment for smart contracts.
