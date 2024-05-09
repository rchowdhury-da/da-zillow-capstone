# DA-Zillow
DA-Zillow is a homelisting service built with DAML

### I. Overview 
This project was created by using the `empty-skeleton` template. The project adopts and exemplifies the `proposal-accept` design pattern. 

A party can create a `HomeListing` contract which is visibile to the public party. Another party can `SubmitOffer` for the listing with a bid price. This creates a `ListingOffer` that the party which listed the home can then either `AcceptOffer` or `RejectOffer`. If the offer is accepted, a `HomeSaleAgreement` contract is created.

Ownership of property is **not** modelled within this project.

An extension of this project can be to then model the change in ownership of the property which was listed.

### II. Workflow
  1. A lister creates a `HomeListing` contract
  2. A bidder exercises the `SubmitOffer` choice for the listing with a bid price. This creats a `ListingOffer` contract.
  3. The lister accepts the offer by exercising the choice `AcceptOffer` on the `ListingOffer` contract.
  4. A `HomeSaleAgreement` contract is created with the details of the transaction

### III. Compiling & Testing
To view project in navigator with the setup script in `daml/Setup.daml` run
```
$ daml start
```

To run the test scripts run in `daml/Test.daml` run

```
$ daml test --files daml/Test.daml
```