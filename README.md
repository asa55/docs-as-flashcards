## Docs are boring, but very important.

I am a working professional. I have a metric ton of information for various technologies I need crammed into my brain to perform day to day tasks.

101's, bootcamps, and introductory courses haven't cut it for a long time at this point in my career, it only matters that I know certain tooling deeply. To this extent, the only thing that really does the trick is reading and understanding the official documentation.

Equally unfortunately is that few tasks are as potent a sedative 😪.

For me personally, a more engaging learning path was necessary in order to make sure I could keep all the information I need at front of mind. Solving this pain point is why `docs-as-flashcards` exists.

All `*-docs-as-flashcards` code repositories I own contain markdown files, which have a GitHub Action that converts them into a flashcard deck. The flashcard deck itself is a `.apkg` file, which is compatible with a popular and free open source flashcard app called Anki.

### To use these flashcards:

1. Download Anki on desktop or mobile
2. Download the `.apkg` files from any or all of the below listed projects (instructions are provided)
3. Use Anki to import the `.apkg` file
4. You're off and running
5. Each of these projects use CalVer (a datetime-based versioning convention). Keep a lookout for updated versions, you can delete the old deck from Anki and import the new one when you're ready. Old versions will be retained here on GitHub as previous releases

### Current offerings:

- [asa55 Azure Virtual Machines Docs](https://github.com/asa55/azure-virtual-machines-docs-as-flashcards/releases) flashcard deck derived from these [official docs](https://learn.microsoft.com/azure/virtual-machines/)
- [asa55 Azure Virtual Network Docs](https://github.com/asa55/azure-virtual-network-docs-as-flashcards/releases) flashcard deck derived from these [official docs](https://learn.microsoft.com/azure/virtual-network/)
- [asa55 Azure Blob Storage Docs](https://github.com/asa55/azure-blob-storage-docs-as-flashcards/releases) flashcard deck derived from these [official docs](https://learn.microsoft.com/azure/storage/blobs/)
