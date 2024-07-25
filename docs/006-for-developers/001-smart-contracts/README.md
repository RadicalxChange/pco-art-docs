# PCOArt Smart Contracts

There are six core functional components in the PCOArt smart contract system:

- **PCO Parameters** - Configuration of the core partial common ownership mechanism  
- **Stewardship License** - The art and its associated Stewardship rights and responsibilties
- **Stewardship Inauguration** - Periodic mechanism by which Stewardship is determined and transferred
- **Creator Circle** - Defines how Periodic Honorariums are distributed 
- **Inauguration Eligibility** - Methods for determining who can participate in an Stewardship Inauguration
- **Configuration Permissions** - Role-based capabilities to update parts of the PCOArt system after initialization
  
![PCOArt System Diagram](https://github.com/user-attachments/assets/a8ea14f4-9e35-40ca-b9e3-b03267db0704)

To promote configurability and extensibility, this system is implmented with the [ERC-2535 Diamonds, Mutli-Facets Proxy](https://eips.ethereum.org/EIPS/eip-2535) standard. Each functional area is instantiated as a modular Diamond Facet--making it easy to mix and match different configurations and implmentation approaches. We see this as especially powerful for supporting unique Creator Circle (e.g. DAO stuctures, dyanimic splits, etc.) and Steward Inauguration (e.g. different auction types) approaches.

Each PCOArt collection is deployed via factory as a soveriegn set of contracts. Artists retain control of their art and community without platform lock-in or dependency.

## v1 Module Implementations

The technial reference of the 6 initial facet implementations and Diamond Proxy structure are included in the subsection pages that follow. 

* [`Periodic PCO Params`](periodic-pco-params)
* [`Steward License`](steward-license)
* [`English Periodic Auction`](english-periodic-auction)
* [`Beneficiary`](beneficiary)
* [`Allowlist`](allowlist)
* [`Access Control`](access-control)
* [`Diamonds`](diamonds)

:::tip

If you have a requirement or idea to adapt PCOArt to better fit your artistic practice or community, please [get in touch](mailto:victoriai@serpentinegalleries.org)! PCOArt is an open-source project and we'd love to support community led development of new facet implementations.

:::

## Github Repository
https://github.com/RadicalxChange/pco-art

## Security Audits
PCOArt is an experimental system and is offered as-is without any warranty or representations to its efficacy or security. 

The PCOArt team did however engage [Sherlock](https://sherlock.xyz) for a partial system scope security audit and contest:

| Auditor | Report Date | Scope | Review Commit Hash |
| ---- | ---- | ----------- | ------ |
| Sherlock | May 12, 2024 | English Periodic Auction | [1c4021c](https://github.com/RadicalxChange/pco-art/commit/1c4021cd96aa2ba1e24d48c299ed3c784bf7a57a) |
