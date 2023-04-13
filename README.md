# NFT Rarity Calculator

Can be used to see the rarity scores of each item in an NFT collection. Mathematics based on [rarity.tools](https://rarity.tools) scoring.

# Trait count adjustment
Added a new adjustment factor to the rarity score calculation that takes into account the number of trait values an NFT has. This adjustment ensures that NFTs with different numbers of trait values can be compared fairly, as an NFT with more trait values is likely to have a higher rarity score simply because it has more opportunities for rare trait values to occur.

The adjustment factor is calculated by dividing 1 by the number of trait values an NFT has, and is stored in the traitCountFactor variable. The rarity score for each NFT is then multiplied by this adjustment factor, resulting in an adjusted rarity score that reflects the NFT's rarity relative to its number of trait values.

# Formatting Options
type is a variable initialized with a string value of either "1" or "2" It is used to determine the type of formatting used in the rarity_scores.json
If type is less than or equal to 1, it will use minimal formatting, and if type is greater than 1, it will use maximum formatting. 

## Requirements

The project will output an ordered list of each edition with corresponding rarity score. The output file will be `rarity_scores.json`.

You will need to place a `metadata_list.json` file in the directory, which is an array of all metadata for the project.

Built using Node.js 16 with Yarn

Install dependencies before running:

```yarn install```

## Running the project

Once everything is ready to go run the following:

```node index.js```

Inspect your `rarity_scores.json` file to see the results! Enjoy!

## Future plans

* Add web3 support to scrape metadata from blockchain (no list required)
* Tooling to see more information about trait distribution within a collection

## Contribute

You can find me at jabeo.eth
