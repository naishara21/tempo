# Joyful PA - your personal diary and mood tracker

Joyful PA is a diary, mood tracker and Kanban board. Its main goals are to help you:

- Keep, organize and find your writings, logs or whatever piece of text you want
- Record and understand how your mood changes and evolves over time
- Remember what needs to be done and organize accordingly

![Joyful PA's Diary view](https://user-images.githubusercontent.com/1970915/158240795-f53c3566-507e-4508-92ac-e0b4af3499ae.png)

Joyful PA is also free to use, open source and web based. You can use it at no cost, from any compatible web browser, both on mobile and desktop, without even creating an account. The data entered in Joyful PA never leaves your device and isn't shared with any third-party. Finally, because Joyful PA is a Progressive Web App, it will continue to work on your device even without any internet connection. 

On a more personal note, Joyful PA is by far the most personal software project I've ever worked on. Since its birth in April 2020, I have put a lot of myself in it. Among other things, it helped me overcome serious mental health issues and still supports me on a daily basis. It was built to address very specific needs (i.e, mine) and also as an experiment.

As a result, Joyful PA isn't meant for everyone. I don't expect it to be used by many people and this is completely fine. There are a lot of other tools available out there that will probably be a better fit for you. But if that's not the case, well, you might want to give Joyful PA a try. 

With that in mind, let's proceed ;)

# Using Joyful PA

To start using Joyful PA, simply visit [https://Joyful PA.agate.blue/](https://Joyful PA.agate.blue/).

If you're using Joyful PA often on mobile, you will probably want to use the "Install app" or "Add to homescreen" feature of your web browser. This will let you launch and use Joyful PA as you would with any other native app.

The [About Page](https://Joyful PA.agate.blue/#/about) in Joyful PA itself should answer most the questions you have while using the app. You can also read more about Joyful PA's features below.

## Diary

![Joyful PA's Diary view](https://user-images.githubusercontent.com/1970915/158240795-f53c3566-507e-4508-92ac-e0b4af3499ae.png)

Joyful PA's diary should be relatively straightforward to use. Simply type your text in the text area, hit save and tada! You've recorded a new note in your diary. There is no hard limit to the size of a single note.

In addition, the diary support advanced use cases and features. All these features are enterily optional and you can use Joyful PA without even thinking about it, but there are in if you ever need them.

### Markdown

You can use titles, bullet list, links, emphasis and other Markdown syntax inside your entries, and have them rendered properly once the note is saved. If you are not familiar with Markdown syntax, you can [learn how to use it in a couple minutes](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Favorites

Entries can be favorited to be quickly found when you most need them.

### Tags

Prefixing any word with a `#` will render it as a hashtag, like this: `Played some #guitar tonight.`. As hashtags can easily be clicked and searched for, this helps you organize your diary without spending too much time thinking about it

Similarly, prefixing a word with an exclamation mark, like this: `Got my first !tattoo today`, will tag entries as important and give you a way to quickly retrieve and browse them afterwards.

Joyful PA supports several other type of tags, related to its mood tracking capabilities and thus described below. 

### Threads

Entries in the diary can have replies, which is especially useful if you want to group them. For instance, you can use a single thread to gather everything related to an event (planning, notes, feedback, etc.)

Thread replies are regular diary entries and, as such, can be queried, favorited, contain tags, annotations, etc.

### Annotations

Entries can contain annotations, beginning with a `@` that let you track more structured data, such as weight, sleep duration, medication increase or decrease, hormone levels, pain levels, etc. 

Here is an example note with two annotations below:

```
Got my blood test results:

@estradiol="114" (pg/mL)
@testosterone="22.3" (ng/dL)
```

This data can then be used to build graphical visualizations such as charts, tables, or even be exported for use in other tools. You can read more on annotations in the dedicated section below.

### Querying and search

Joyful PA includes a search bar and a powerful query language you can use to quickly find entries:

- Full text search: `guitar` gives you entries containing `guitar`
- Tag search: `tag:music` gives you entries tagged with `#music` or `!music`
- Date search:
    - `date:2021` gives you entries recorded in 2021 
    - `date:2021-05` gives you entries recorded in May 2021 
    - `date:2021-05-13` gives you entries recorded in May 13th, 2021 
- Tag type search:
    - `#` gives you entries with any hashtag
    - `!` gives you all important entries
- Other operators:
    - `is:favorite` gives you all favorited entries
    - `is:thread` gives you all first entries of a thread
    - `is:reply` gives you all replies thread
    - `not:guitar` gives you all entries not containing `guitar`. `not:` can be used before other operators, such as `not:is:reply` or `not:date:2021`

All these operators can be combined to further refine your search:

- `! date:2021-05` gives you important entries recorded in May 2021
- `music jam` gives you entries that includes both `music` and `jam` in their body
- `tag:music piano` gives you entries tagged with `music` and containing `piano` in their body

You can use a coma separator to express `OR` queries:

- `piano, guitar` gives you entries including `piano` or `guitar` in their body
- `date:2021-01, date:2022-01` gives you entries submitted in January 2021 or January 2022

Finally, if this isn't enough for you, Joyful PA support defining query aliases. It's not uncommon to use several variations of a word or tag inside entries. For instance, if you record your dreams, you may have some that are tagged with `#dream`, others with `#dreams`, other with `#nightmares`, etc. To easily find all those entries without typing all the possible variations every time, you can define a `$dreams` alias, corresponding to the following search query: `tag:dream, tag:dreams, tag:nightmare`.

You can then use the `$dreams` alias in place of the original, longer query.


## Mood tracker

Mood tracking in Joyful PA is done by leveraging your diary. As a result, while it is totally possible to use Joyful PA as a diary without any of the mood tracking features, you'll have to use the diary at least a little bit in order to track your mood in Joyful PA. You don't have to worry though, it doesn't mean you have to write *a lot*.

### Moodtags

For instance, the following diary entries contain enough information for Joyful PA to act as a mood tracker:

```
-sad
```

```
+happy
```

```
+excited
```

```
-exhausted
```

The `+` and `-` in front of words tells Joyful PA that the corresponding note is linked to your mood, in a positive or negative way, respectively. In Joyful PA's vocabulary, they are called moodtags.

This gives you the opportunity to include more context about how you are feeling, which tends to be very helpful when you're going trying to understand why your mood changed at a given point in time. 

For instance:

```
I had an -exhausting day at work.

I was already tired because of -insomnia and it just got worse.
```

Moodtags can be repeated to convey greater intensity:

```
I am very +++excited about tomorrow
```

```
That was a --bad nightmare
```

Because mood isn't binary, you can use as many and different moodtags in the same note to express nuances:

```
I had a pretty decent night of +sleep and was in a good mood this morning.

However, I received a phone call that made me quite --anxious
```

Joyful PA will keep a track that this note include both positive and negative moods, but that it was predominently negative. Internally, a mood score is attached to the note, based on the number of moodtags and repetitions:

- `guitar` gets a score of 0
- `+excited` gets a score of 1
- `--anxious` gets a score of -2
- `-tired but ++happy` gets a score of +1 (`-1 + 2`)

### Visualization

At some point, you will probably want to use this information to actually understand what's going on with your mood. Joyful PA use moodtags in various places:

- In the Diary view, at the top corner of each note, a color badge showsyou the predominent mood of a note
- Similarly, in the Calendar view, entries have a color matching their predominent mood
- In the Visualization view, Joyful PA display several charts:
    - A day to day chart, showing your mood variations, using the total mood scores of each day's entries
    - A "Common tags" table, showing you the most used tags and their associated mood score
- In search queries, via the `-` and `+` operators, to filter negative or positive entries respectively

## Kanban board

The "Tasks" menu gives you access to a relatively simple Kanban Board.

You can customize the number of lists (columns) shown in the board, their name, and optionally define a few categories. Once you're done with this initial configuration (you can change the appearance of your board afterwards if needed), you can start using the board:

- Creating tasks in various columns
- Move them between columns
- Check them to mark them as done
- Filter them via the search bar, using keyword search or their category

## Using Joyful PA on multiple devices

By default, all the data you put in Joyful PA stays in your web browser. It never leaves your device, which is a good thing in terms of privacy and simplicity but becomes an issue when you want to use Joyful PA on multiple devices, for instance on your phone and laptop.

The good news is that Joyful PA does support multi-device synchronization, giving you a full read and write access to your data on as many devices as you want.

However, this feature requires an access to a CouchDB database to store this data and synchronize it. As I don't have the resources to host such as service and provide it for free, it means you'd have to do it yourself, if you have the skills, or find someone who can do it for your.

Once you have access to a CouchDB database server, fill your credentials in Joyful PA Settings page. You have to do this on all the devices that you plan to use.

Your local data will be pushed on the remote database, and vice-versa, during the initial synchronization. Afterwards, all modifications to your data such as adding, updating, deleting and note or task will be forwarded to your CouchDB database and other devices that are connected to it.

The "Sync" button in the menu let you force the data synchronization. This can be useful if you were offline for a while, and want to immediatly push your changes without waiting for Joyful PA to resume the syncing process.

## Backing up data

The settings page lets you export your notes, board and other settings for backup and restore purpose. 

## Importing data

From the "Settings" page, you can import your notes, board and settings from a previously generated backup file. A couple important things:

- When you import notes, your existing diary will be preserved, unless some notes have the same timestamp. In that case, existing notes will be replaced by the ones from the backup.
- Importing your board will work in the same way. Existing tasks will be preserved. However, your existing board configuration will be replaced by the new one, which could lead to some inconsistencies if you have different columns and/or categories in the current and backed-up board.

## Deleting data

You will find a form to delete all your data from Joyful PA at the end of the settings page. Doing so will effectively and definitely remove all your notes, tasks and configuration, giving you a blank state. It isstrongly recommended to perform a JSON backup beforehand, just in case.

If you have connected Joyful PA to a CouchDB database before deletion, only your local copy of the data will be deleted. Data will remain unaffected on the CouchDB database and other devices.
