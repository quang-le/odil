# How to add a grammar for syntax highlight in Eclipse

1. Add the file in TextMate


Go to `Window > Preferences > TextMate > Grammar` and add your file. Good news if your importing from VSCode, JSON format is supported. If you're importing a grammar file straight from a VSCode extension, you will need to add a ` fileTypes` array:

```json
{
    "scope": "source.extension",
    "fileTypes": [".this", ".that"]
}
```

Pretty easy so far, right?

2. Define a Content Type

Go to `Window > Preferences > General > Content Type and choose a content type for your grammar. You'll see the extensions under File Associations (which you can edit) and the associated Editors under (you guessed it:) Associated editors, which you can also edit. At this stage, it seems all set, right? Well...no.

3. Associate Editors

If this feels redundant to you, you're not alone, but here it goes:

Go to `Window > Preferences > General > Editors > File Associations and add your file extension(s). You can also add/remove associated Editors, like in step 2. PSA: I had to change the default Editor for my file extension for the grammar to be taken into account.

Now, apply the changes, and you're all set. It's nothing crazy, but it's too many steps if you ask me, and also quite annoying to figure out.
