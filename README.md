# [WIP] open-proposal-standard
```Note: This standard is work in progress and not final yet!```

Open standard which provides a unified structure for the exchange of grant proposals between different systems.

## Background
Ocean Pearl wants to introduce a standardized data structure for sharing proposals and projects between third party systems.

## Fundamentals
- Data structure is based on json objects (see [RFC 8259](https://tools.ietf.org/pdf/rfc8259.pdf))
- Encoding is based on **UTF-8** to avoid character escaping
- Versioning for breaking changes or new features

## Models
This standard follows the approach that one project can have multiple grant proposals in total (1 to n relation).
Per funding round only one proposal is allowed for every project.

The relationship between project and proposal is based on the provided wallet-address. A specific wallet-address can only be claimed by one project (1 to 1 relation).
- [project](models/project.json5)
- [proposal](models/proposal.json5)

## Constraints
- [Data-Types](constraints/DATA-TYPES.md)
- [Enumerations](constraints/ENUMERATIONS.md)