# RC-0.6.0 Load Test Report

## Methodology

This load test was conduct on GCP region us-east1-c, using the (Pocket Network Simulator)[https://github.com/pokt-network/pns] software found here. 

## Scenario Configuration

All the configuration for the scenario run, can be found in the Load Testing Scenario Configuration spreadsheet, with a summary below:

1. Genesis Configuration: configurations done at the genesis level when the network is kickstarted such as validators, apps and accounts in the Pocket Network.
2. Pocket Core Configurations: Configurations done in the `config.json` of each Pocket Core instance that's spun up during the test.
3. Instance configurations: Configurations that pertain to the actual instance created in GCP to run 1-N Pocket Core processes, from CPU, RAM and Disk configurations.
4. PRLTS Configurations: (Pocket Relay Load Testing System)[https://github.com/pokt-network/prlts] is the software used to simulate the Pocket Core Apps that would be using the Pocket Network.

## Scenario 1

Scenario 1 was meant to achieve the next milestone in the Pocket Network with the following metrics:

1. 5,000 Validator Nodes
2. 4,166,666 Relays per session (1 hr sessions).
3. ~15 minute blocks

## Limitations

1. The peering capabilities is done via Seed Nodes, as using persistent peering proved problematic for consensus in the earlier blocks.
2. There are hardware limitations in the number and size of instances that GCP can provision in a single run.
3. Disk space limited the generation of PRLTS evidence.

## Conclusion

Several observations were made during the load test:

1. Memory climbs when processing claims and proof as observed in the Memory RSS Graph image.
2. The test processed ~4.133 M relays according to aggregated PRLTS data.
3. Claims were succesfully submitted and finalized into the state.
4. Proofs were submitted, however hardware limitations knocked more than 33% of the validator power offline, causing a chain halt.

Test Result: Inconclusive due to hardware limitations of the environment.