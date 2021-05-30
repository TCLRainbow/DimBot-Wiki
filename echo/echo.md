# Project Echo
`Echo` is the module responsible for storing messages within the database.

There are 2 different message storage: `Quote` and `Tag`.

[Quotes](quote.md) are designed to store a message said by a person. They can be used in cases like storing memes said by your friends.

Tags are essentially shortcuts for pins. They only store links and can be used in cases like sending an answer of a FAQ to a member.

Here is a comparison table:

| |Quote|Tag
|---|:-:|:-:
|**Content type**|Plain text|Link
|**Server specific**|No|Yes
|**Searching**|ID/Quoter & Quoter group/Uploader/Content|Name
|**Who can create?**|Anyone|Members with `Manage Message` permission
|**Who can manage?**|The creator|Members with `Manage Message` permission