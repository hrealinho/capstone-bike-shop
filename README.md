# BikeShop Project

## I. Overview

This project was created by using the empty-skeleton template. The project adopts and exemplifies the proposal-accept design pattern. 
A signatory party (shop) can create a RepairJobProposal template for a customer. The customer can exercise the AcceptJobProposal or RejectJobProposal choice as a controller. If the customer accepts the proposal, a RepairJob is created. If the customer rejects the proposal, the proposal gets archived.
A signatory party can also create a BikeShopService template. the shop can exercise the FetchRepairJob on to get a RepairJob contract payload, if the RepairJob exists. If it does not exist, an exception is thrown.

## II. Workflow

1. Shop party creates a RepairJobProposal contract for a given customer party.
2. Customer accepts the RepairJobProposal by exercising the AcceptJobProposal, with the details and observers that the customer can specify being passed as arguments. The AcceptJobProposal archives the RepairJobProposal contract and creates a RepairJob contract. 
  Customer can also reject the job proposal by exercising RejectJobProposal on the RepairJobProposal contract, which archives the proposal contract.
3. Shop party exercises FinishJob on a RepairJob contract to archive the RepairJob.

## III. Challenges

The init-script value on `daml.yaml` was updated to:
`init-script: Test:test`

## IV. Building

To compile the project
`$ daml build`

## V. Testing

To test all scripts:Run the pre-written script `test` in the Test.daml 

## VI. Running

To load the project into the sandbox and start navigator:
`$ daml start`
