
PCP

Create a Genesis Block
======================


In this activity, you will learn to create a new blockchain, beginning with a genesis block, and print the information within the chain.




<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10650499/PCP.gif" width = "480" height = "320">




Follow the given steps to complete this activity.
1. Create a genesis block.


* Open the file blockchain.py.


* Check if the length of the chain is 0, and call the createGenesisBlock() method.


    `if(len(self.chain) == 0):
    self.createGensisBlock()`


* Set newBlock.index to 1


    `newBlock.index=1`
   
* Set the current hash of the last block as the previous hash.
 
    `newBlock.previousHash = self.chain[-1].currentHash`  


* Create a method createGenesisBlock.


    `def createGenesisBlock(self):`
       
* Create a new block using the block class with index 0, current time, empty transaction, and no previous hash.


    `genesisBlock = Block(0, time(), {}, "No Prevoius Hash Present. Since this is the first block.")`


* Append the block to the chain.


    `self.chain.append(genesisBlock)`
       
* Open the file index.html from the templates folder.


* Remove and condition to only check blockData.

    `{% if blockData %}`

* Run the loop for each block in the blockData to show the accordion-item for each block.

    `{% for block in blockData %}`

* Show block information.

    `<b>Block Number:</b> <span>#{{block.index}}</span> <br>
    <b>Vendor:</b> <span>{{block.transaction['vendor']}}</span> <br>
    <b>Receiver:</b><span>{{block.transaction['receiver']}}</span> <br>`

* Show block information.

    `<strong>Part Number:</strong> 
        <span>{{block.transaction['partNumber']}}</span><br>
    <strong>Part Name:</strong> 
        <span>{{block.transaction['partName']}}</span><br>
    <strong>Dimensions:</strong> 
        <span>{{block.transaction['dimensions']}}</span><br>
    <strong>Weight:</strong> 
        <span>{{block.transaction['weight']}}</span><br>
    <strong>Timestamp:</strong> 
        <span>{{block.timestamp}}</span><br>`

* End the for loop.


    `{% endfor %}`


* Save and run the code to check the output.