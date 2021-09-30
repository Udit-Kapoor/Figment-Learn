# Introduction
Hey Reader! Welcome to this Tutorial on How to write, deploy & interact with a smart contract on Tezos in SmartPy. We will be learing a lot and having fun alongside!
You will be able to understand the industry standards of coding on SmartPy and be able to deploy your own Calculator Smart Contract whilist Understading the code as well.

- Tezos is an open-source blockchain protocol for assets and applications backed by a global community of validators, researchers, and builders. The Tezos protocol is secure, upgradable, and built to last.
- SmartPy is an intuitive and powerful smart contract development platform for Tezos and is available through a Python library for building and analyzing Tezos smart contracts.


# **Prerequisites**

You need basic understanding of Python Language. Rest all will be covered from getting XTZ from the Faucet to Coding and Deployment!


# **Requirements**

You will need to have Temple Wallet Installed in your browser. Get it [HERE](https://templewallet.com/).


# Body of the Tutorial
##Section 1 : SmartPy IDE
Hi all ! Let me start with explaining what SmartPy actually is ,  SmartPy is a high-level smart contracts library and comes with related tools in the form of [SmartPy.io](https://smartpy.io/) to greatly ease the accessibility, understandability and provability of smart contracts on Tezos.

So Head on over to [SmartPy.io](https://smartpy.io/) and let us begin writing our First Smart Contract!

When you reach SmartPy.io , You will have a screen like below

__IMAGEEE___

Here we have two important links namely 
-[Online Editor](https://smartpy.io/ide)
-[Documentation](https://smartpy.io/docs/)

The Online Editor will help us write , execute and test our Smart Contract before it is deployed on the Blockchain and Documentation will help us with various DataStructures , Conditions , DataTypes and much more!

Click on Online Editor Button and you will get a screen like below
___IMAGE___
Here SmartPy has provided us with various Template and sample contracts. It includes Games , Token Contracts and some basic Utility Contracts.
We will be coding our own version of Calculator Contract that is present as one of the Examples.

Before we start on with the coding we need to cover some of the basics

We will be importing SmartPy library and use it throughout the Contract

```
import smartpy as sp
```
And the functions of SmartPy will be called with the prefix sp.

Moving on Python does not support direct conversion of Python Code to Michelson. Hence we would have to use functions present in SmartPy to even do basic operations. 
-sp.if
-sp.else
-sp.verify
-sp.for
-sp.while

Next We have to understand that all SmartContracts are essentially Python Classes which have to be inherited from ```sp.Contract``` , All the Class Attributes will taken as the Contract Storage and All the Class methods will be considered as EntryPoints of the Contract which we can call from FrontEnd to change the state of the Contract.

**NOTE: No change will take place in the Contract unless called the user via EntryPoint**

Now on to Coding our Contract:
We will import SmartPy Library

```
import smartpy as sp
```

Create a Python Class that inherits the class ```sp.Contract``` and define it's Storage

```
class Calculator(sp.Contract):
    def __init__(self):
        self.init(value = sp.TInt)
```
Here we have taken a variable *value* and defined it's DataType as *sp.TInt*

As we know that Python does not support direct conversion of Python Code to Michelson, we have to use different Data Types as well. For Example:
-sp.TInt 
-sp.TBool
-sp.TTimestamp
-TBytes

And Also Tezos Specific Data Types like:
-sp.TAddress
-sp.TMutez
-sp.big_map

You can read up about all the DataTypes and their equivalent SmartPy counterparts in the [Documentation](https://smartpy.io/docs/)


```
import smartpy as sp

class Calculator(sp.Contract):
    def __init__(self):
        self.init(value = 0)

    @sp.entry_point
    def multiply(self, x, y):
        self.data.value = x * y

    @sp.entry_point
    def add(self, x, y):
        self.data.value = x + y

    @sp.entry_point
    def subtract(self, x, y):
        self.data.value = x - y

    @sp.entry_point
    def divide(self, x, y):
        self.data.value = x / y

    @sp.entry_point
    def square(self, x):
        self.data.value = x * x

    @sp.entry_point
    def factorial(self, x):
        self.data.value = 1
        sp.for y in sp.range(1, x + 1):
            self.data.value *= y
```


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
