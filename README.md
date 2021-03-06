# BigchainDB Examples

This repo contains examples and tutorials for BigchainDB.

__Warning__: These examples are for demonstration purposes and should not be used as-is for production

See the [documentation](http://bigchaindb-examples.readthedocs.io/en/latest/index.html):
* [Installing](http://bigchaindb-examples.readthedocs.io/en/latest/install.html)
* [Running](http://bigchaindb-examples.readthedocs.io/en/latest/run.html)
* [Troubleshooting](http://bigchaindb-examples.readthedocs.io/en/latest/troubleshooting.html)

Examples:
* [On the Record](#example-on-the-record)
* [Share Trader](#example-share-trader)

### Dependencies

The examples can be [run via Docker](http://bigchaindb-examples.readthedocs.io/en/latest/install.html#the-docker-way)
(**recommended**), but, if you'd like, you can [run them locally](http://bigchaindb-examples.readthedocs.io/en/latest/install.html#install-from-source)
with the following system dependencies:

 - OS dependencies: see [setup BigchainDB & RethinkDB](https://bigchaindb.readthedocs.io/en/latest/installing-server.html#install-and-run-rethinkdb-server)
 - python>=3.4
 - node>=5.3 using [nvm](https://github.com/creationix/nvm#installation) (**recommended**), or [manually](https://nodejs.org/en/download/)
 - [npm>=3.3](https://docs.npmjs.com/getting-started/installing-node) (should be installed with node)


## Example: "On the Record"

"On the Record" is a simple logging app, wrapped as a messaging board.

You should see the app running on [http://localhost:3000/ontherecord/](http://localhost:3000/ontherecord/),
or if running docker, `http://docker-machine:32800/ontherecord/` (replace `docker-machine` as
necessary with `localhost` or your docker-machine ip).

<p align="center">
  <img width="70%" height="70%" src ="./docs/img/on_the_record_v0.0.1.png" />
</p>

### Use cases

- Immutable logging of data
- Notarization of data, text, emails

### Functionality

#### Create assets
- with arbitrary payload
- and an unlimited amount

#### Retrieve assets
- that you currently own (like UTXO's)
- by searching the asset data/payload
- state indicator (in backlog vs. on bigchain)

#### What this app doesn't provide

- Proper user and key management
- Transfer of assets

## Example: Share Trader

Share Trader is a simple share allocation and trade app. Each square represents an asset that can be traded amongst accounts.

You should see the app running on [http://localhost:3000/sharetrader/](http://localhost:3000/sharetrader/),
or if running on docker, `http://docker-machine:32800/sharetrader/` (replace `docker-machine` as
necessary with `localhost` or your docker-machine ip).

<p align="center">
  <img width="70%" height="70%" src ="./docs/img/share_trader_v0.0.1.png" />
</p>

### Use cases

- Reservation of tickets, seats in a concert/transport, ...
- Trade of limited issued assets

### Functionality

#### Create assets
- assets are created following a structured payload
- the amount is limited

#### Transfer assets
- easy transfer of assets between accounts by:
 - clicking on an account first. This will give the assets for that account
 - clicking on an asset of that account. Transfer actions will appear on the right side.

#### Retrieve assets
- that you currently own (like UTXO's)
- all assets on bigchain
- state indicator (blinks if asset has various owners)

#### What this app doesn't provide

- Proper user and key management
- Proper signing of transfers
- Proper search by payload

## Acknowledgements:

Special thanks to the BigchainDB/ascribe.io team for their insights and code contributions:

@r-marques, @vrde, @ttmc, @rhsimplex, @SohKai, @sbellem, @TimDaub
