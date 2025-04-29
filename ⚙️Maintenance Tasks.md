All actions I can do to **help maintain the vault** in good health or for routine cleanup and review. 
Some are used occasionally when needed, others should be run regularly to keep things tidy.


# 🔁 Regular maintenance

[[(Query) List Orphans|List orphans]]
	→ Finds notes that have no links in or out. 
	Useful for identifying isolated or forgotten content.
[[(Query) Short notes|Short notes]]
	→ Highlights very short notes (under 2000 bytes) in your project folder. 
	Good for spotting stubs that need expanding or deleting.
[[(Query) Image not uploaded to vault|Image not uploaded to vault]]
	→ Detects external image links instead of local ones. 
	Use this to convert remote images into locally stored files for long-term access.

# 📌 Useful maintenance (when needed)

[[(Query) To search for a tag|To search for a tag]]
	→ Quickly find notes tagged with YourTag (can be adapted to any tag). 
	Use regularly to monitor tagged content and maintain structure.
[[(Query) Oldest file|Oldest file]]
	→ Surfaces the note that hasn't been modified in the longest time. 
	Handy for rediscovery or cleanup.

# 🧩 Required plugins

These queries rely on the following community plugins being installed and enabled in your Obsidian vault:
- Dataview (for all the queries to function)

# 🧰 Community plugin: O2

**O2** is a community plugin that provides a workflow to manage note conversion and archiving.  

Folder structure it uses:
Your vault 
├── ready (where the notes you want to convert are placed) 
├── archive (where the original notes before converting are placed) 
└── attachments (where the attachments are placed)
