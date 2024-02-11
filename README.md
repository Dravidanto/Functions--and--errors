# Photoelectric Effect 

## Overview

This Solidity smart contract simulates the photoelectric effect, a phenomenon in physics where electrons are emitted from a material when it is exposed to light. The contract allows users to observe the photoelectric effect by turning on a light source, setting a threshold frequency, and monitoring the emission of electrons.


### State Variables

- `bool public lightSourceOn`: Indicates whether the light source is turned on or off.
- `uint256 public thresholdFrequency`: Represents the threshold frequency for the photoelectric effect.
- `uint256 public emissionStartTime`: Records the start time of electron emission.
- `uint256 public numberOfEmittedElectrons`: Tracks the number of electrons emitted.

### Modifiers

1. `requireLightSourceOn`: Ensures that the light source is turned on before executing certain functions.
2. `assertThresholdFrequency`: Asserts that the threshold frequency is greater than or equal to 10.
3. `checkEnergyGenerated`: Checks if the number of emitted electrons exceeds 100,000, reverting the transaction if true.

### Events

1. `LightSourceTurnedOn`: Fired when the light source is turned on.
2. `EmissionStarted`: Fired when observing the photoelectric effect, providing the start time and duration.
3. `EnergyGenerated`: Fired when a specified number of electrons is emitted, indicating the generation of 10 units of energy.

### Functions

1. `observePhotoelectricEffect`: External function to observe the photoelectric effect. Requires the light source to be on and asserts the threshold frequency.
2. `energyGenerated`: External function to emit an event when a certain number of electrons is emitted, triggering the generation of 10 units of energy.
3. `turnOnLightSource`: External function to turn on the light source.
4. `turnOffLightSource`: External function to turn off the light source.
5. `setThresholdFrequency`: External function to set the threshold frequency.
6. `setNumberOfEmittedElectrons`: External function to set the number of emitted electrons.

## License

This smart contract is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
