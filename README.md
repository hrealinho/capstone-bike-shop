I. Overview
This project was created by using the empty-skeleton template. The project adopts and exemplifies the proposal-accept design pattern. 
A signatory party (shop) can create a RepairJobProposal template for a customer. The customer can exercise the AcceptJobProposal or RejectJobProposal choice as a controller. If the customer accepts the proposal, a RepairJob is created. If the customer rejects the proposal, the proposal gets archived.
A signatory party can also create a BikeShopService template. the shop can exercise the FetchRepairJob on to get a RepairJob contract payload, if the RepairJob exists. If it does not exist, an exception is thrown.

II. Workflow


III. Challenges
The init-script value on daml.yaml was updated to:
init-script: Test:test

IV. Building
To compile the project

$ daml build
V. Testing
To test all scripts: Either run the pre-written script in the Test.daml under /daml OR run:

$ daml start

VI. Running
To load the project into the sandbox and start navigator:

$ daml start