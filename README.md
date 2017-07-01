# Bitcoin Core User Activated Soft Fork UASF
## Running docker image

Version bitcoin-0.14.2-bip148_segwit0.3

Running node is as simple as running  
`docker run -d -v $PWD/data:/home/uasf/.bitcoin/blocks -p 8333:8333 3h4x/bitcoin-uasf`

Important thing to preserve data is mounting a volume (-v) to docker image.

If you want to build it yourself  
`docker build -t bitcoin-uasf .`  
`docker run -d -v $PWD/data:/home/uasf/.bitcoin/blocks -p 8333:8333 bitcoin-uasf`

## Cloudformation

Cloudformation is AWS service to provision infrastructure.  
Before you lunch bitcoin node in cloud you should know that:  
- "Full nodes are only meaningful if you run them on hardware you exclusively control." - luke-jr
- There is possibilty of attacking the network with a <a href="https://en.wikipedia.org/wiki/Sybil_attack" target="_blank" title="Sybil Attack">Sybil attack</a>

[![Launch Bitcoin Full Node with UASF](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/cloudformation-launch-stack-button.png)](https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=bitcoin-uasf&templateURL=https://s3.amazonaws.com/bitcoin-uasf/uasf.yaml)
