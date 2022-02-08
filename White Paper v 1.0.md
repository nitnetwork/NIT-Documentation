# New Information Technologies 
![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_logo.png "New Information Technologies")
![NIT](https://github.com/nitnetwork/papers/blob/main/img/nitpgp.png "New Information Technologies")

_@tetakta, @web3nit_
 
11 november 2021 (v1.0)

## Abstract

__VISION__ 👾

We are witnessing the beginning of a new stage in the development of life.
A new, technological and decentralized world is emerging 

It will be fully integrated into the Internet blockchain technology. 
Bitcoin blockchain is already the basis for this development. 
Ethereum is also the solution by which this technology is realized. 
Innovative companies and New Decentralized Companies will regularly use Bitcoin and Ethereum blockchain.
NEW blockchain and WEB3 technologies have launched new Internet concepts:
participants interact directly without going through a trusted intermediary 
users have much greater control over their personal data
internet is accessible to everyone anywhere thanks to ubiquity
user search is more useful and convenient with semantic web
 
__Our mission is to make web3 technologies understandable, convenient and accessible__

---

__Table of Contents__

1. Abstract
2. Intro
3. Market overview and NfX
4. Roadmap
5. Technology
6. Economy
7. Team
8. To the future  . . . 

---

## Intro

__NIT__ is an international open-source community whose members and the public work together to propose solutions to problems such as complexity of search and use, lack of information, and technical interoperability of new web3 technologies.

Over the years, many models have been created to make the blockchain ecosystem more useful, such as layer 2, naming and aggregation systems. We are working to make these systems function as efficiently as possible.

Our main activities include creating standards, guidelines, interfaces for decentralized systems, and integrating web3 technologies.

This will help us bring blockchain into the real world.

__NIT PROTOCOL__ - 
is a core framework for data search, communication and execution in web3 systems

__The NIT protocol and services are:__
- Truth machine - Bitcoin and Ethereum blockchain recording and encoding
- Smart Contract Builder - creation, verification, automation on Bitcoin and Ethereum blockchain
- DAO Builder - algorithmic company, decision making, cryptoeconomics on Bitcoin and Ethereum blockchain
- BTC-ETH bridge

__NIT is also:__
- Blockchain Technology Research and Development Center
- Open-source library of structured information, instructions and methodologies
- Educational programs on blockchain technology


## Market overview and NfX

The global blockchain technology market size was valued at USD 3.67 billion in 2020. It is expected to expand at a compound annual growth rate (CAGR) of 82.4% from 2021 to 2028. Blockchain has emerged as a highly promising technology in the IT domain. It is an open, immutable, distributed public ledger that can be accessed by several parties involved in the transaction and acts as a universal depository of all transactions between the involved parties. The increasing acceptance of cryptocurrency worldwide is one of the major factors driving market growth. Commercial and central banks across the world are now using blockchain technology for payment processing and issuing of their digital currencies. The technology enables cross-border payments that are less expensive and faster as compared to traditional systems.

![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_marketsize.png "New Information Technologies")

The remittance cost within the blockchain is 2% to 3% of the total amount as compared to other third parties as blockchain does not require third-party authentication. Various financial service and solution providers are entering into partnerships with blockchain solution providers to enhance their cross-border payment processes. For instance, in September 2019, Mastercard announced its partnership with R3, an enterprise blockchain software provider, to develop a blockchain-enabled cross-border payment solution.
The traditional stock exchange involves a lot of bureaucracy and stages and thereby, requires three days for processing. However, blockchain technology's decentralization nature in banking removes unnecessary intermediates and enables trade to be run on computers globally. At the same time, blockchain helps improve performance by reducing the redundancy of information in trading transactions. Various financial service providers use blockchain technology for enhancing their stock exchange processes. For instance, in January 2021, SBI Holdings, based in Japan, partnered with Sumitomo Mitsui Financial Group to launch a digital stock exchange in the country by 2022.
The increasing global demand for digital payment systems is driving the market growth in the current days. Digital payment relies on multiple parties to process transactions, including merchant banks, retail banks, card issuers, and payments software companies, which creates the demand for blockchain technology to secure the transactions. Simultaneously, the reliability of users on trusted institutions to complete their day-to-day electronic transactions is also creating the demand for blockchain technology.

__NfX__
![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_NfX_BTC.jpeg "New Information Technologies")

Crypto changes the nature of money in a historical way, because unlike gold or paper money, crypto is a native creature of the new global network. That gives it unfair powers from the future. Unlike fiat currencies, it isn’t constrained by geography or time. Unlike fiat currencies, it’s programmable and can be improved quickly in response to market needs. Most importantly, software-money more easily amplifies the “belief” network effect that gave older forms of currency power, since today the world is more connected and shared, beliefs spread faster in higher densities.


## Roadmap
![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_roadmap.png "New Information Technologies")

## Technology

__Overview__

It is important to every being alive in this world. Today we have in our hands a reliably working, stable and secure technology for our future. It is distributed and belongs to no one, it is more accurate to say it belongs to all of us and we to it, it is our opportunity, our truth and virtue!
Today is the time to start using blockchain widely and bring it to all of our technological attention. The Foundation of New Information Technologies was created to begin developing basic necessary, and at the same time, very simple and accessible tools* for everyone.
It all began with bitcoin, and today we suggest focusing our attention on the bitcoin blockchain, it is the foundation and the beginning, it is the base layer, it is the trust machine of humanity.

Special thanks to Satoshi Nakamoto and Vitalik Buterin for creating reasons to start thought on these topics



  ___NIT PROTOCOL SERVICES___

__Truth machine__ 

A system for bitcoin and ethereum blockchain text writing and reading, as well as verification and escrow using decentralized blockchain and IPFS technologies.

The Truth machine function module has 3 basic functions:
1. Recording
2. Reading
3. Verification

![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_UI.png "New Information Technologies")

---

### WRITE

The library was taken for the recording system blockchaindata-lib
github.com/3s3s/blockchaindata-lib. 

![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_codelib1.png "New Information Technologies")

_WRITING A TEXT DOCUMENT IN BITCOIN BLOCKCHAIN_

The article on which this paper is based:
https://habr.com/ru/post/470884/

Install a library that communicates with bitcoin-cli
https://www.npmjs.com/package/blockchaindata-lib

Write code in Node.js to write text into a blockchain that will read data from a text file

'use strict';
 
const blockchaindata = require('blockchaindata-lib');
const fs = require('fs');

async function write()
{
    try {
        //Сохраняем текст в блокчейне        
        const data = fs.readFileSync('2.txt', 'utf8');
        const ret1 = await blockchaindata.SaveTextToBlockchain(data);
        if (ret1.result == false) throw new Error("SaveTextToBlockchain failed, message: "+ret1.message);

       console.log("SaveTextToBlockchain success! txid="+ret1.txid+"\n--------------------------")
    }
    catch (e) {
        console.log(e.message)
    }
}

write()

Maximum file size ~65 Kilobytes

After a successful write operation hash will be returned to the transaction, which contains our document, compressed using the deflate algorithm by the zlib library

It took 0.00058288 BTC to record two files
(18 dollars on 7.17.21)

After that you can read the file and display its content in the console or redirect the output to another file


'use strict';
 
const blockchaindata = require('blockchaindata-lib');

const hash1 = '8fa9bfbbfb4b62e31b1b52ecc1da3218ece5e8b94648971b52a864ef7a5ba64b';
const hash2 = '557405e2e5e1919f1b3566493a478bf45400607f54a0b371a321242faaa6e437';

async function read()
{
    try {
        const savedObject = await blockchaindata.GetObjectFromBlockchain(hash2);
        if (savedObject.type == 'error') throw new Error(savedObject.message)
        
        // if (savedObject.type == 'text')
        console.log(Buffer.from(savedObject.base64, 'base64').toString('utf8'));
        //else// console.log(savedObject.base64);

    }
    catch(e) {
        console.log(e.message)
    }
}

read();


Description




Details:
UI
Description
Action

Blockchain selection buttons for recording
[functionality is oriented to the selected ecosystem]

Author data block. Name, wallet, tag/keyword, signature (+signature download button)
[text input fields. pressing the button opens a standard file downloader]

File upload module. The file is uploaded to IPFS and its ipfsID is assigned to the given blockchain record
[pressing the button opens the standard file downloader]



The text entry field of the record. The number of characters is limited to 20 thousand.
[the character count works when you type]




Transaction weight and commission counter, consent check (consent that the data will be irrevocably written to the blockchain), "write" button
[with the consent checkbox selected, pressing the button records, the transaction becomes a queue]



_READ_
The following references were taken for the reading system:
Messages from the Mines (MFTM) 
https://github.com/brangerbriz/messages-from-the-mines

// get an array of all of the messages from a certain block (using it's index)
// from the mysql database. searches three tables:
//     - coinbase_messages
//     - address_messages
//     - op_return_messages

bitcoin-blockchain-parser https://github.com/alecalve/python-bitcoin-blockchain-parser/blob/master/examples/texts-in-coinbases.py
  
read coinbase text/ py lib

Description | Flow 

Details:

UI
Description
Action

The user chooses the blockchain to write to. Bitcoin or Ethereum.
[when selecting a blockchain, the system changes functionality towards the selected ecosystem]

Blockchain Navigation. Sequential
[explorer moves between blocks sequentially when clicked]

Keyword search filter (in records)
[when explorer is pressed, filter blocks by keyword. reset only when filter is canceled]

Data block. Contains transaction ID. If the record is made through B.TR/machine\ then it has another set of data such as : name, wallet, tag/keyword, key/signature
[when you click on the transaction ID/hash, it is copied to the clipboard]

Entry text.  Full text, Block information (number, extraction date, hash)
 "share" and "download" buttons
[clicking on the button "share" opens the module share in social networks; clicking on the button "download" the entry is downloaded to your computer in .png format in a graphic template NIT]



__INFO__



## Economy

__Overview__
__NIT is an ERC-20 token that is a key to NIT Protocol features. The native utility token of the NIT Network (NIT Token) is used to pay fees for operations (transactions) in the NIT ecosystem.__
NIT Token is divided up till 0.00000001 and will be issued as erc-20 standard compliant tokens on the Ethereum blockchain, in the next stages it may be driven by our own unique technology.
We need to provide the economic incentives to encourage participants to contribute and maintain the ecosystem. Computational,economic and human resources are required to maintain the NIT Network, thus providers of these resources would be rewarded with NIT tokens (i.e. "economic mining"). 

NIT aims to use a potential of equilibrium model for circulating supply. 

In near future staking validators and delegators will secure the network by staking their NIT in smart contracts, which are used to support the network(achieve consensus and other contributions).

__For each transaction in a system equivalent 1$ NIT fee is paid which goes to next pools:__

- Contributors community  65 %
- Miners                  15 %
- DAO                     10 %
- Treasury                10 %


 __Usage__

1. Transaction fees on the NIT Protocol: Token can be used to pay for transactions and operations, and users also receive a discount for doing so
2. NIT Token is a utility token which functions as the unit of payment and settlement between participants in the NIT ecosystem 
3. Trading: NIT Token can be traded for other cryptocurrencies on various exchanges
4. Loans and transfers: NIT can be used as collateral for loans on certain platforms

__Allocation__

One billion NIT tokens will be minted at genesis and will become accessible over the course of 10 years. Every year 10% of tokens with a two year lock are distributed.  

The initial 10 year allocation of NIT Token is as follows:

- 65.00% to contributors community 650,000,000 (founders,core team,individuals and groups,community initiatives, airdrops, hundreds of Discord and Telegram users)
- 15.00% to miners 150,000,000 (hybrid mining,liquidity providers)
- 10.00% to DAO 100,000,000 (community will choose different individuals or organizations with hybrid vesting who will be responsible for effective maintenance of the NIT ecosystem)
- 10.00% to treasury 100,000,000 (ecosystem insurance)


At genesis year 10% NIT tokens will be distributed with a two year lock as following:

- Founders 20,000,000 NIT 
- Individuals and groups 20,000,000 NIT 
- Liquidity providers 15,000,000 NIT (based on snapshot ending January 3, 2023, at 12:00 am UTC)
- Core Team 10,000,000 NIT 
- Developers 10,000,000 NIT
- DAO 10,000,000 NIT
- Treasury 10,000,000 NIT 
- Holders Airdrops 2 500 000,00 NIT  (based on snapshot ending January 3, 2024, at 12:00 am UTC)
- Telegram and Discord users 2 500 000,00 NIT 

For the airdrop all you need to do is to have 100 NIT Token on your balance.

Contributor’s community pool will retain 65% [650,000,000 NIT] of token supply to distribute on an ongoing basis through grants and other programs aimed to develop and expand NIT ecosystem. 

See table for token allocation schedule: https://docs.google.com/spreadsheets/d/1Puvlw3n1jc9aWaP-QrEcgEkKguzSHvMWoQgB8jLobAE/ 

Every half a year from 2024 (start of a profit period) NIT Network will use 10% of its profits to buyback and lock NIT Tokens. We will continue to perform buybacks until 300 000 000 million tokens – 30% of the total supply will be locked.

Annually DAO can decide if a certain amount of tokens to be burned or minted but it will require significant Voting Power with max supply that won't ever exceed 1 billion     NIT tokens.

NIT holders will take part in building a technological,user-friendly ecosystem by voting on different proposals. Every user has its own level of Voting Power due to the amount or equivalent of NIT Tokens. A community-driven NIT DAO opens up a world of infinite possibilities such as ecosystem grants and funding.

DAO supreme governance will begin when more than 50% of tokens will be mined and the system will be decentralized, technologically mature and complianced. Our minimal goal - 50% decentralization by the end of 2027. At now administration of the root contracts is centralized and controlled by a multisig with founders as keyholders. 

This period will provide the NIT community enough time to familiarize itself with the governance system and begin discussions and communications around potential governance proposals. 

NIT holders are responsible for ensuring that governance decisions are made in compliance with applicable laws and regulations. Our community will consult legal and regulatory professionals before implementing any specific proposals.

NIT holders will have abilities and ownership of: 

- NIT governance 
- NIT Treasury & DAO funds
- nit.eth ENS name 
- The protocol fee 

Initial governance parameters are as follows: 

  50% of NIT total supply to reach quorum

  25% +1 of NIT total supply required to vote 'yes' for proposal to pass

  30 day voting period 

  7 day timelock delay on execution


We have established an entity called The NIT For People in the USA to legally represent the DAO, e.g. fulfill any tax obligations. The articles of incorporation give token holders the right to appoint and dismiss directors, and to instruct entity to take real-world actions.

__NIT Digital Statute__

As part of the governance process, NIT holders will hold genesis voting on a proposed NIT Digital Statute which is a set of rules and guidelines for the NIT community on how NIT should be governed. To pass, it’ll need 25% +1 approval and a quorum of 50% of all total tokens. Vote proposals will be open on September 1, 2022 and voting will start 03.01.2027 . Users will be encouraged to delegate their voting power to a community member that represents their views (call for delegates).

__To become an early contributor you can claim a unique NIT NFT which will allow you to receive 1000 NIT and special DAO privileges (private channels,early delegates).__


__Contracts__
- NIT Token: https://etherscan.io/token/0x 
- Liquidity mining:https://etherscan.io/token/0x 
- Governance: https://etherscan.io/address/0x
- Timelock: https://etherscan.io/address/0x 

__Legal__
This document  is an integral part of the General Legal Terms (available by the link: https://nit.network/legal), legal provisions of which (including, but not limited - responsibilities, risks, guarantees) are completely applicable to this document.

By reading, downloading or opening this document you automatically and totally agree to comply with all the provisions of the General Legal Terms (available by the link: https://nit.network/legal) and in such a way you confirm that we have no responsibility for the provided information (including, but not limited with this document, General Legal Terms, information placed on the website https://nit.network ) and you have no objections to us (and won’t have it in the future). The document is intended only for the information purposes.

Nothing mentioned in the current document is a proposal of any kind (including tender offer for investments), legal request or application about a purchase or sale of any securities in any jurisdiction within NIT or any other system of the related company. The information provided here is not a proposal, legal request or application of NIT tokens in any jurisdiction within NIT or in any jurisdiction where such a proposal, requirement or sale would be illegal. Some allegations and assessments, which are contained in the current document, represent projected statements or information. These projected statements are related to the known and unknown risks and uncertainty, which can appear significantly different from factual developments or results, implied or expressed in such projected statements.
NIT Token does not in any way represent any shareholding, participation, right, title, or interest in the company, the issuer, its affiliates, or any other company, enterprise or undertaking, nor will NIT Token entitle token holders to any promise of fees, dividends, revenue, profits or investment returns, and are not intended to constitute securities in Singapore or any relevant jurisdiction. Ownership of NIT Token carries no rights, express or implied, other than that which may be afforded by the NIT Network and/or any other third parties who may use such Tokens.

In particular, it is highlighted that NIT Token:

1. is non-refundable and cannot be exchanged for cash (or its equivalent value in any other virtual currency) or any payment obligation by the company, the issuer or any affiliate;
2. does not represent or confer on the token holder any right of any form with respect to the company, the issuer (or any of its affiliates), or its revenues or assets, including without limitation any right to receive future dividends, revenue, shares, ownership right or stake, share or security, any voting, distribution, redemption, liquidation, proprietary (including all forms of intellectual property or licence rights), or other financial or legal rights or equivalent rights, or intellectual property rights or any other form of participation in or relating to the NIT Network, the company, the issuer and/or their service providers;
3. is not intended to represent any rights under a contract for differences or under any other contract the purpose or pretended purpose of which is to secure a profit or avoid a loss;
4. is not intended to be a representation of money (including electronic money), security, commodity, bond, debt instrument or any other kind of financial instrument or investment;
5. is not a loan to the company, the issuer or any of its affiliates, is not intended to represent a debt owed by the company , the issuer or any of its affiliates, and there is no expectation of profit; 
6. and does not provide the token holder with any ownership or other interest in the company, the issuer or any of its affiliates.


## Team

![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_team.png "New Information Technologies")




---



## To the future  . . . 




The time has come to New Information Technology

With them, humanity can build a civilization that is strong, free in mind and spirit, and filled with sense and love! 



Create meanings as root causes

Generate love as an energy of power

Be honest(because truth now has a place to be written down)

__Be free ...__


![NIT](https://github.com/nitnetwork/papers/blob/main/img/NIT_action.png "New Information Technologies")


