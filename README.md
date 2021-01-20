# Novelcoin
Novel Coin Source Code
}Novel:Coin{ const abi = [
  {
    inputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "constructor",
  },
  {
    anonymous: false,
    inputs: [
      {
        indexed: true,
        internalType: "address",
        name: "owner",
        type: "address",
      },
      {
        indexed: true,
        internalType: "address",
        name: "spender",
        type: "address",
      },
      {
        indexed: false,
        internalType: "uint256",
        name: "value",
        type: "uint256",
      },
    ],
    name: "Approval",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      {
        indexed: false,
        internalType: "uint256",
        name: "total",
        type: "uint256",
      },
      {
        indexed: false,
        internalType: "address",
        name: "tokenAddress",
        type: "address",
      },
    ],
    name: "Multisended",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      {
        indexed: false,
        internalType: "address",
        name: "previousOwner",
        type: "address",
      },
      {
        indexed: false,
        internalType: "address",
        name: "newOwner",
        type: "address",
      },
    ],
    name: "OwnershipTransferred",
    type: "event",
  },
  {
    anonymous: false,
    inputs: [
      { indexed: true, internalType: "address", name: "from", type: "address" },
      { indexed: true, internalType: "address", name: "to", type: "address" },
      {
        indexed: false,
        internalType: "uint256",
        name: "value",
        type: "uint256",
      },
    ],
    name: "Transfer",
    type: "event",
  },
  {
    constant: true,
    inputs: [{ internalType: "address", name: "", type: "address" }],
    name: "Users",
    outputs: [
      { internalType: "uint256", name: "amount", type: "uint256" },
      { internalType: "uint256", name: "Id", type: "uint256" },
    ],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: true,
    inputs: [
      { internalType: "address", name: "owner", type: "address" },
      { internalType: "address", name: "spender", type: "address" },
    ],
    name: "allowance",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "spender", type: "address" },
      { internalType: "uint256", name: "value", type: "uint256" },
    ],
    name: "approve",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: true,
    inputs: [{ internalType: "address", name: "owner", type: "address" }],
    name: "balanceOf",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [{ internalType: "uint256", name: "value", type: "uint256" }],
    name: "burn",
    outputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "from", type: "address" },
      { internalType: "uint256", name: "value", type: "uint256" },
    ],
    name: "burnFrom",
    outputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: false,
    inputs: [],
    name: "buy",
    outputs: [],
    payable: true,
    stateMutability: "payable",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "decimals",
    outputs: [{ internalType: "uint8", name: "", type: "uint8" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "spender", type: "address" },
      { internalType: "uint256", name: "subtractedValue", type: "uint256" },
    ],
    name: "decreaseAllowance",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "erc20token",
    outputs: [{ internalType: "address", name: "", type: "address" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "spender", type: "address" },
      { internalType: "uint256", name: "addedValue", type: "uint256" },
    ],
    name: "increaseAllowance",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address[]", name: "_contributors", type: "address[]" },
      { internalType: "uint256[]", name: "_balances", type: "uint256[]" },
    ],
    name: "multisendToken",
    outputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "name",
    outputs: [{ internalType: "string", name: "", type: "string" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "owner",
    outputs: [{ internalType: "address", name: "", type: "address" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [],
    name: "register",
    outputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "symbol",
    outputs: [{ internalType: "string", name: "", type: "string" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: true,
    inputs: [],
    name: "totalSupply",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "to", type: "address" },
      { internalType: "uint256", name: "value", type: "uint256" },
    ],
    name: "transfer",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: false,
    inputs: [
      { internalType: "address", name: "from", type: "address" },
      { internalType: "address", name: "to", type: "address" },
      { internalType: "uint256", name: "value", type: "uint256" },
    ],
    name: "transferFrom",
    outputs: [{ internalType: "bool", name: "", type: "bool" }],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: false,
    inputs: [{ internalType: "address", name: "newOwner", type: "address" }],
    name: "transferOwnership",
    outputs: [],
    payable: false,
    stateMutability: "nonpayable",
    type: "function",
  },
  {
    constant: true,
    inputs: [{ internalType: "address", name: "customer", type: "address" }],
    name: "txCount",
    outputs: [{ internalType: "uint256", name: "", type: "uint256" }],
    payable: false,
    stateMutability: "view",
    type: "function",
  },
  {
    constant: false,
    inputs: [{ internalType: "uint256", name: "_amount", type: "uint256" }],
    name: "withDraw",
    outputs: [],
    payable: true,
    stateMutability: "payable",
    type: "function",
  },
];

let network;
let contract_address;
let connection;
let mainAccount;
let interval;
let interval2;
let hash1 = "";
let hash2 = "";
let Accounttype = "0";
contract_address = "0x22eDD76CB243297c8A107804180bFc2ef96d53D4";
window.addEventListener("load", () => {
  interval = setInterval(function checkConnection() {
    if (typeof web3 === "undefined") {
      connection = "Metamask is not available";
      jQuery("#metamaskConnection").text(connection);
    } else {
      connection = "Connected to Wallet.";
      console.log(connection);
      jQuery("#metamaskConnection").text(connection);
      mainAccount = web3.eth.getAccounts(function (err, accounts) {
        mainAccount = accounts[0];
        // jQuery("#txtmetawallet").val(mainAccount);
        //  $("#createaccount").removeAttr("disabled");
        jQuery(document).ready(function () {
          getBalanceOfAccount();
          getContractBalance();
          isLocked();
        });
      });
    }
    web3.version.getNetwork((err, netId) => {
      switch (netId) {
        case "1":
          console.log("This is mainnet");
          jQuery("#network").text("This is mainnet");
          Accounttype = "1";
          network = "mainnet";
          break;
        case "2":
          console.log("This is the deprecated Morden test network.");
          jQuery("#network").text(
            "This is the deprecated Morden test network."
          );
          break;
        case "3":
          console.log("This is the ropsten test network.");
          jQuery("#network").text("This is the ropsten test network.");
          network = "ropsten";
          break;
        case "4":
          console.log("This is the Rinkeby test network.");
          jQuery("#network").text("This is the Rinkeby test network.");
          network = "Rinkeby";
          break;
        case "42":
          console.log("This is the Kovan test network.");
          jQuery("#network").text("This is the Kovan test network.");
          network = "Kovan";
          break;
        default:
          console.log("This is an unknown network.");
          jQuery("#network").text("This is the unknown test network.");
      }
    });
  }, 3000);
  // if (window.ethereum) {
  //   window.web3 = new Web3(ethereum);
  //   try {
  //     // Request account access if needed
  //     ethereum.enable();
  //   } catch (error) {
  //     // User denied account access...
  //   }
  // }
});
function isLocked() {
  web3.eth.getAccounts(function (err, accounts) {
    if (err != null) {
      console.log(err);
      jQuery("#lock").text(err);
    } else if (accounts.length === 0) {
      console.log("MetaMask is locked");
      jQuery("#lock").text("MetaMask is locked.");
    } else {
      console.log("MetaMask is unlocked");
      jQuery("#lock").text("MetaMask is unlocked.");
    }
  });
}
function getEventData() {
  console.log(contract.getPastEvents);
  console.log(contract.allEvents());
}
function register() {
  try {
    console.log("web3" + web3);
    let contract = web3.eth.contract(abi).at(contract_address);
    //   let RequestAmount = jQuery("#ddlRequestAmount").val;
    contract.register.sendTransaction(
      {
        //gasLimit:21000,
        gasPrice: 30000000000,
      },
      (error, result) => {
        if (result) {
          jQuery("#registerId").text("Hash:" + result);
        }
      }
    );
  } catch (error) {
    console.log("sss", error);
  }
}
function withDraw() {
  try {
    let amount = jQuery("#withDrawAmount").val();
    console.log("amount:" + amount);
    let contract = web3.eth.contract(abi).at(contract_address);
    //   let RequestAmount = jQuery("#ddlRequestAmount").val;
    contract.withDraw.sendTransaction(
      amount,
      {
        gasPrice: 30000000000,
      },
      (error, result) => {
        if (result) {
          jQuery("#withDrawId").text("Hash:" + result);
        }
      }
    );
  } catch (error) {
    console.log("sss", error);
  }
}
function BuyToken() {
  try {
    let amount = jQuery("#EtherValue").val();
    console.log("amount:" + amount);
    let contract = web3.eth.contract(abi).at(contract_address);
    //   let RequestAmount = jQuery("#ddlRequestAmount").val;
    contract.buy.sendTransaction(
      {
        value:web3._extend.utils.toWei(amount,'ether'),
        gasPrice: 30000000000,
      },
      (error, result) => {
        if (result) {
          jQuery("#buyId").text("Hash:" + result);
        }
      }
    );
  } catch (error) {
    console.log("sss", error);
  }
}
function GetUserDetail() {
  try {
    let address = jQuery("#userDetailId").val();
    //console.log("amount:" + amount);
    let contract = web3.eth.contract(abi).at(contract_address);
    //   let RequestAmount = jQuery("#ddlRequestAmount").val;
    contract.Users.call(address,(error,response)=>{
      if(response){
        console.log(response);
        console.log(response[1].c[0]);
        console.log(web3._extend.utils);
        let obj={
          Id:response[1].c[0],
          amount:web3._extend.utils.fromWei(response[0].c[0]/10000,'wei')+' '+'Eth',
        }
        console.log(obj);
        jQuery("#UserId").text("USER Data:" + JSON.stringify(obj));
      }else{
        console.log(error);
      }
    });
    
  } catch (error) {
    console.log("sss", error);
  }
}
function getBalanceOfAccount() {
  web3.eth.getBalance(mainAccount, function (err, res) {
    if (!res.c[1]) {
      var combine = (res.c[0] * 100000000000000) / 1000000000000000000;
      $("#getBalance").text(combine);
    } else {
      var combine =
        (res.c[0] * 100000000000000 + res.c[1]) / 1000000000000000000;
      $("#getBalance").text(combine);
    }
  });
}
function getContractBalance() {
  web3.eth.getBalance(contract_address, function (err, res) {
    if (!res.c[1]) {
      var combine = (res.c[0] * 100000000000000) / 1000000000000000000;
      $("#contractBalance").text(combine);
    } else {
      var combine =
        (res.c[0] * 100000000000000 + res.c[1]) / 1000000000000000000;
      $("#contractBalance").text(combine);
    }
  });
}
