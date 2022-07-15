---
description: >-
  This article describes the validator anatomy on the Inanis version. This
  document is subjected to the change progress and changes in the Initium
  protocol.
---

# Anatomy

### General Outline&#x20;

Also called a "blockchain verifier," validators are computers that maintain the blockchain's integrity by constantly computing the linkage from the first block to the last. There is generally an abbreviated version of the blockchain for this purpose that is much smaller than the full chain, which contains every transaction.

Validators for a public blockchain are maintained primarily by volunteers, who typically dedicate a computer to the process.

Validator anatomy on the Initium Inanis version has the anatomy as the picture below.&#x20;

![Figure 1. Validator Anatomy on the Initium Inanis version. ](../../.gitbook/assets/validator-64cad642fda2dc0de9cd1b695651e620.svg)

### Pipelining

The validators extensively use an optimization standard in CPU design called _pipelining_. Pipelining is the right tool for the job when a stream of input data needs to be processed by a sequence of steps, and there's different hardware responsible for each. The quintessential example is using a washer and dryer to wash/dry/fold several loads of laundry. Washing must occur before drying and drying before folding, but each of the three operations is performed by a separate unit. To maximize efficiency, one creates a pipeline of _stages_. We'll call the washer one stage, the dryer another, and the folding process a third. To run the pipeline, one adds a second load of laundry to the washer just after the first load is added to the dryer. Likewise, the third load is added to the washer after the second is in the dryer, and the first is folded. This way, one can progress on three loads of laundry simultaneously. Given infinite loads, the pipeline will consistently complete a load at the rate of the slowest stage in the pipeline.

### Pipelining in the Validator

The validator contains two pipelined processes, one used in leader mode called the **TPU** and one used in validator mode called the **TVU**. In both cases, the pipelined hardware is the same, the network input, the GPU cards, the CPU cores, writes to disk, and the network output. What it does with that hardware is different. The TPU exists to create ledger entries, whereas the TVU exists to validate them.
