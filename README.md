## Plastic Wallet Maker
This a node.js app that generates 'paper' wallets for Bitcoin Cash. These kinds
of wallets are often called 'cold storage' wallets too. The artwork generated
by this software is intended to etched on
to [PVC plastic cards](https://amzn.to/3bV3cHj) with
a [laser engraver](https://amzn.to/2V9ejXj).

![artwork example](images/laser-engraver-screenshot.JPG)

The artwork is generated as an HTML page that can be captured as screen-shot
images. The images can be exported to the laser engraver and etched onto the
plastic cards.

## Installation

- Install [NodeJS](http://nodejs.org/) LTS version 8.x or greater.

- Clone this repository:

`git clone https://github.com/christroutner/plastic-wallet`

- Install the dependencies:

`cd plastic-wallet && npm install`

## Usage

A typical workflow is

- `npm run generate-wallet` to create the HD wallet used to generate the
address/key pairs. This command will prompt you for two things:
1. The language to use, which will default to English. Just hit enter.
2. The number of addresses to generate. Enter a number, like 5.

- `npm run create` to create the artwork for the laser engraver.

- Delete the `wallet.json` file in the `output/wallets` directory so that no
one can steel the funds. You should also delete the artwork files after etching
them onto plastic.

## Engraver Details
If you use [the same laser engraver I used](https://amzn.to/2V9ejXj), these are
the settings that worked best for the PVC business cards:

1. Power at 35%
2. Depth at 37%

Also, the cards are glossy. I sanded them down with 80 grit sandpaper before
engraving them.
