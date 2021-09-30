# Introduction

Explain the context for this tutorial and why it matters, what we're going to build and learn in this tutorial.

- Explain this section like you're explaining it to 5-year-old (**ELI5**)
- Explain everything in 5-6 lines maximum.

*For example -*

NEAR is a platform that allows anyone to create decentralized applications that can perform tasks without the need for a central entity. Building a Voting dApp is a good candidate for something that can showcase NEAR's power and potential. We're going to build a smart contract using Solidity, with a ReactJS front-end and at the end, we will deploy our dApp on the NEAR testnet.

# **Prerequisites**

Any prior knowledge needed or existing tutorials that need to be completed first, any tokens that are needed, mention them here.

*For example -*

- In this tutorial, we're going to build a Voting dApp on NEAR using DataHub so before we proceed further make sure to complete the Tutorial 1 "Connect to NEAR Node using DataHub" of the [NEAR Pathway](notion://www.notion.so/network-documentation/near/tutorials/intro-pathway-write-and-deploy-your-first-near-smart-contract/1.-connecting-to-a-near-node-using-datahub.md).
- Complete the [Simple AssemblyScript App](notion://www.notion.so/network-documentation/near/tutorials/simple-webassembly-script.md) Tutorial, first.

# **Requirements**

Any technology that needs to be installed **prior** to starting the tutorial and that the tutorial will not cover (`Metamask`, `node`, `truffle`, etc). Do not list packages that will be installed during the tutorial.

*For example -*

- We'll need Metamask in this tutorial, install it from [HERE](https://metamask.io/).
- Make sure to have NodeJS 12.0.1+ version installed.

**OPTIONAL :** Embed any video content in this section, if your tutorial has any.

# Body of the Tutorial

Points to remember:

- **Section headings like Introduction, Prerequisites, etc. *must* all be H1, keep all sub-headings at H2.**
    - In Markdown syntax, a single hashmark is used for H1 headings: #
    - Two hashmarks are used for H2 headings: ##
- Add all relevant Code Blocks, with the appropriate syntax highlighting:
    - ```text must be used for terminal output, terminal commands and plaintext.
    - ```javascript can be used for both JavaScript and Solidity, while ```jsx can be used for ReactJS code.
    - Use ```rust and ```toml when highlighting Rust or TOML syntax.
    - Use ```graphql when highlighting GraphQL
    - Use ```json when highlighting valid JSON (for invalid JSON examples, use ```text instead).
    - ```bash should *only* be used for Code Blocks where you need to have # style comments. This must be done carefully because in many situations the # character will render as a heading. If this happens it will usually wreck the Table of Contents.
- Add necessary comments in Code Blocks.
- Add any text content necessary to guide readers through your tutorial.
- Add Images or Code Blocks to reflect expected terminal output.
- Add common errors and steps to troubleshoot the errors, *for example -*

**Not able to connect to the Avalanche Node and getting error on executing `node connect.js`**

Let's check for some common causes:

- First, make sure you have the `.env` file saved and it's in the correct format as given in the tutorial.
- If you're getting an error message like `UnauthorizedError: { "message":"Invalid authentication credentials" }` then make sure to replace the `<API_KEY>` with your correct API key which you copied from the DataHub Dashboard.
- Make sure to have the `.env` file saved in your project root folder.
- Make sure `NODE_URL` in the `.env` file is correct.
- If you're still experiencing the same issue, reach out to us on [Discord](https://discord.gg/fszyM7K) or on the [Forum](https://community.figemnt.io/) for help.

# **Conclusion**

This section should summarize what was learned, reinforce key points and also congratulate the learner for completing the tutorial. Use a maximum of 5-6 lines.

# Next Steps *(Optional)*

Use this section to explain what can be done next after this tutorial for continued learning.
Feel free to add recommended projects and articles here which are related to this tutorial. If you're working on any other advanced tutorials, you can briefly mention them here.

# About The **Author**

Keep it short. One or two lines at most. You can include a link to your GitHub profile + [Figment Forum](https://community.figment.io) profile, however please refrain from adding your LinkedIn or Twitter here.

# **References**

This section ***must*** be present if you have taken any help in writing this tutorial from other documents, GitHub repos and existing tutorials.

Credit sources by adding their name and a link to the document when possible. 

If it is not a digital document, include an ISBN or other form of reference.
