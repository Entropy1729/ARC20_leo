# ARC20_leo

##  About The Project
Implementation of the 6 mandatory rules in Leo Programming Language so that they can be invoked in a Smart contract.

They are: **BalanceOf**, **TotalSupply**, **Approve**, **TransferFrom**, **Transfer**, and **Allowance**.

## Usage

### To run *BalanceOf* function:

Input file ARC20_leo/inputs/arc20_leo.in
```
[balanceof]
owner_balance: Balance = Balance {
    owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7,
    gates: 0u64,
    amount: 269u64,
    _nonce: 0group,
};
```

`leo run BalanceOf`

Console output
```
 • Executing 'arc20_leo.aleo/balanceof'...
 • Executed 'balanceof' (in 11642 ms)

➡️  Output

 • 269u64
```

### To run *total_supply* function:

Input file ARC20_leo/inputs/arc20_leo.in
```
[total_supply]
amount_supply: u64 = 1729u64;
```

`leo run total_supply`

Console output.
```
 • Executing 'arc20_leo.aleo/total_supply'...
 • Executed 'total_supply' (in 5944 ms)

➡️  Output

 • 1729u64
```

### To run *Approve* function:

Input file ARC20_leo/inputs/arc20_leo.in
```
[approve]
owner: address = aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7;
amount_owner: u64 = 164u64;
spender: address = aleo1mgfq6g40l6zkhsm063n3uhr43qk5e0zsua5aszeq5080dsvlcvxsn0rrau;
amount_desired: u64 = 64u64;
```

`leo run Approve`

Console output.
```
 • Executing 'arc20_leo.aleo/approve'...
 • Executed 'approve' (in 9745 ms)

➡️  Output

 • true
```

### To run *TransferFrom* function:

Input file ARC20_leo/inputs/arc20_leo.in
```
[test_transferfrom]
from_balance: Balance = Balance {
    owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7,
    gates: 0u64,
    amount: 25u64,
    _nonce: 0group,
};
from: address = aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7;
to_address: address = aleo1mgfq6g40l6zkhsm063n3uhr43qk5e0zsua5aszeq5080dsvlcvxsn0rrau;
to_gates: u64 = 0u64;
to_amount: u64 =  30u64;
amount: u64 = 5u64;
```
`leo run TransferFrom`

Console output.
```
 • Executing 'arc20_leo.aleo/transferfrom'...
 • Executed 'transferfrom' (in 21740 ms)

➡️  Outputs

 • {
  owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7.private,
  gates: 0u64.private,
  amount: 20u64.private,
  _nonce: 6431287615986696097612324621785026814136142669749924915411966793544219414836group.public
}
 • aleo1mgfq6g40l6zkhsm063n3uhr43qk5e0zsua5aszeq5080dsvlcvxsn0rrau
 • 35u64
 • 0u64
```

### To run *Transfer* function:

Input file ARC20_leo/inputs/arc20_leo.in
```
[transfer]
to_balance: Balance = Balance {
    owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7,
    gates: 0u64,
    amount: 25u64,
    _nonce: 0group,
};
to: address = aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7;
amount: u64 = 5u64;
```

`leo run Transfer`

Console output.
```
 • Executing 'arc20_leo.aleo/transfer'...
 • Executed 'transfer' (in 14139 ms)

➡️  Output

 • {
  owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7.private,
  gates: 0u64.private,
  amount: 30u64.private,
  _nonce: 5223267181059685515422878880245687591758320347768724919987298470390181053809group.public
}
```

### To run *Allowance* function:
Input file ARC20_leo/inputs/arc20_leo.in
```
[allowance]
owner: address = aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7;
spender: address = aleo1mgfq6g40l6zkhsm063n3uhr43qk5e0zsua5aszeq5080dsvlcvxsn0rrau;
balance_owner: Balance = Balance {
    owner: aleo1ht2a9q0gsd38j0se4t9lsfulxgqrens2vgzgry3pkvs93xrrzu8s892zn7,
    gates: 0u64,
    amount: 250u64,
    _nonce: 0group,
};
amount_remaining: u64 = 78u64;

```

`leo run Allowance`

Console output.
```
 • Executing 'arc20_leo.aleo/allowance'...
 • Executed 'allowance' (in 16274 ms)

➡️  Output

 • 78u64
```

##  Optional functions
ARC20 includes 3 optional rules. They are: **decimals**, **name**, and **symbol**.

### To run *decimals* function:
Input file ARC20_leo/inputs/arc20_leo.in
```
[decimals]
quantity_decimals: u64 = 8u64;
```

`leo run decimals`

Console output.
```
 • Executing 'arc20_leo.aleo/decimals'...
 • Executed 'decimals' (in 4244 ms)

➡️  Output

 • 8u64
```

### To run *name* function:
Input file ARC20_leo/inputs/arc20_leo.in
```
[name]
is_dummmy: u64 = 0u64;
```

`leo run name`

Console output.
```
 • Executing 'arc20_leo.aleo/name'...
 • Executed 'name' (in 6431 ms)

➡️  Outputs

 • 65u64
 • 76u64
 • 69u64
 • 79u64
```

### To run *symbol* function:
Input file ARC20_leo/inputs/arc20_leo.in
```
[symbol]
is_dummmy: u64 = 0u64;
```

`leo run symbol`

Console output.
```
 • Executing 'arc20_leo.aleo/symbol'...
 • Executed 'symbol' (in 6450 ms)

➡️  Outputs

 • 76u64
 • 69u64
 • 79u64
```
