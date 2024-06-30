# Guide to the experiments

To verify all the lemmas within a theory through Tamarin Prover, open a terminal in the current directory and execute

```bash
tamarin-prover [file].sphty --prove
```

Alternatively, to verify only a single lemma, run

```bash
tamarin-prover [file].sphty --prove=[lemma]
```

Finally, to run the tool in the interactive mode on all files within the current folder, execute

```bash
tamarin-prover interactive .
```

## Results

File ```NS.spthy``` contains the formalization of the standard Needham-Schroeder Symmetric Key protocol. Running Tamarin on it will produce the following output:

```bash
==============================================================================
summary of summaries:

analyzed: NS.spthy

  processing time: 7.70s
  
  types (all-traces): falsified - found trace (36 steps)
  Sanity (exists-trace): verified (14 steps)
  Confidentiality (all-traces): verified (48 steps)
  Attack (exists-trace): verified (18 steps)

==============================================================================
```

Confirming the existence of an attack.

On the other hand, the theory ```NS_fixed.sphty``` solves the issue by incorporating Denning and Sacco's fix:

```bash
==============================================================================
summary of summaries:

analyzed: NS_fixed.spthy

  processing time: 6.37s
  
  types (all-traces): verified (684 steps)
  Sanity (exists-trace): verified (14 steps)
  Confidentiality (all-traces): verified (16 steps)
  Attack (exists-trace): falsified - no trace found (55 steps)

==============================================================================
```

Finally, theory ```X3DH.spthy``` is only included to show that sometimes Tamarin enters in an infinte loop during precomputation.