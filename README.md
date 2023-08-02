# REMIX-ETHEREUM

The entire foundation of using solidity assessment is initialized by this program, which is doing so by combining all of those modules into one token.

## Description
The ability to browse the Ethereum blockchain will be made possible by this unique program, which is recognized as evolving over many years. And by doing so in the most common manner: by using coding! This demonstrates that blockchain is the foundation.


## Getting started
 ### Installing the software
   This is the easy and most efficient way to get through the Blockchain stuff. Just get to https://remix.ethereum.org/. and get started with your token! Of course, it's not THAT easy isn't it? well just press the plus (+) button and you're good to code! (with minor adjustments like naming your file with .sol whichever you like) ()

   This is what i did on mine, pretty simple yet can be organized immediately
```javascript

MyToken.sol

   ```

## 1st Code
  Secondly, you'd need to copy and paste the code regarding the final assessment and then follow Chris' instructions on how to efficiently use the remix and the coding altogether
```javascript
contract MyToken {

    // public variables here

string public tokenName = "KEVIN";
string public tokenAbbrv = "KEV";
uint public totalSupply = 0;



```

You'll need to put variables of your Token name and the Abbreviation of that token being a public domain which helps you differenciate the Name and the Abbreviations. (as stated in here, i did caps-on 'KEVIN' and the abbreviation of it being 'KEV' with all caps) 

and initiating with mapping the variable (making the Address => uint as your public balances) 
uint is basically an unsigned int that doesnt go by negative and also doesn't add anything hence, being a zero (0) value towards the public variables indicated in the code.
## 2nd Code


```javascript

    // mapping variable here
    mapping(address => uint) public balances;

```
So Here at mapping variable the mapping variable is used to track of the balance of each address in the token contract
(therefore its called 'balances')

## 3rd Code

And here the mint function is needed in a token contract to create and distribute new tokens so it allows the contract owner to generate additional tokens. Since it has a parameter should have an address and a value (in which i did underscore address and underscore value (_address, _value) to differenciate the parameters into the normal values)!

```javascript

 // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
     }
```
in the second one we would need to do the burn and minting function which is basically the same except using the functions of  '+=' on the mint function 

in the mint function this will be the increasing of total supply by the amount of that's already passed by using the total supply and balances (with calling the _address and adding the value altgoether) and the address being increased by the balances together with the value. 



```javascript
    // burn function
    function burn (address _address, uint _value) public {
        if (balances [_address ] >= _value) {

        totalSupply -= _value;
        balances [_address] -= _value;
        }
        
    }

```

in the burn function works the opposite of the mint function as it destroys tokens (it will take an address in value just like in the mint function) and removes the total supply and the balance from the address altogether. Copy pasting the mint function but the opposite run by using the subtraction symbol when it has the plus symbol underneath it and viola! you have now just gotten the burn function that basically annihilates your token!

you'll be using the opposite which is '-=' (A brief reminder that any number that pertains as a negative will never be called in this section e.i -1 or so. So the value would always be either 0 or above. )

lastly on the burn function being called out; you need to make a condition to make sure the balance of the amount you gotten is greater or equal that's supposed to be burned.
(giving the if function to differinciate the value you gave to the mint and the one you're supposed to burn)

and calling the total supply and the balances altogether

once this is all connected you'll need to open the "solidity compiler" on the left side of the remix.etherium.org (which you'll be doing your compiling) and use the 'compile my token.sol' which is located at the left side. once that's done it will run on the bottom of the website saying it ran. 


## Running the Code


4th thing you'll need to do is deploy and run tab which is located below at the solidity compiler button. with it opening, you'll see the orange button that says deploy which grants you to see if your token is available or not. You'll have to test the waters a.k.a the tokens(abbrv, name, and total supply buttons) within the 'deployed contracts'

lastly and most importantly youll need to copy your account which is directed at the depoly and run transactions and copy paste it and opening the mint and burn below the deployed contracts. Giving them value (equal or greater than the one you're burning) and pasting the account numbers you just got and putting them into the address section and giving value to the value section. When ran by the token abbrv it will give the certain amount of you just did (500 for example to the mint function that will call out and give you 500 tokens as an example) and giving it the total supply of also 500. the same with Burn section, same sequence different number (1000 for example, it will burn the 1k you just gotten to the burn function) and testing it with the totalsupply section and the token abbrv and you're done! that's the whole sequence of mytoken! 

 ### Authors
   LEGASPI.KEVIN JASH
   @skevs on discord
