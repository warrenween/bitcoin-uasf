# bitcoin-uasf
## Running

Version bitcoin-0.14.1-bip148_segwit0.3

`docker build -t bitcoin-uasf .`  
`docker run -d -v $PWD/data:/home/uasf/.bitcoin/blocks bitcoin-uasf`
