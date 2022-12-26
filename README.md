# Journal

The `journal` script is a tool for documenting your work day by day. It saves records by date and allows you to specify a journal type, or "namespace," for organizing your entries.

## Usage

To use the `journal` script, you can run it with the following options:

```
$ journal [--type <journal-type>]
$ journal show [<time-specifier>] [--type <journal-type>]
```


### Time Specifier

- The `journal` script allows you to specify a time period to view your journal entries.
- Time specifier can be either one day (=one record), or range of days.
- Single day can be any date string accepted by the `date` command. Examples: `2022-12-26`,
  `yesterday`, `last Thu` etc.
- Range can be:
  * `YY-MM-DD:YY-MM-DD` where the first date is earlier than the second, or it can
  * last week/month/year
  * current week/month/year
  * all

### Options

`--type`, `-t`: Specify the journal type, or "namespace," for organizing your entries. The default 
is "daily". Other types might be "weekly", "workout", "coaching-sessions" etc.

## Examples

Here are a few examples of how you might use the `journal` script:

- To create a new journal entry for today:

```
$ journal
```

- To view your journal entries for the past week:

```
$ journal show "1 week ago"
```

- To view your journal entries for the month of June 2021:

`$ journal show "2021-06-01:2021-06-30"`


- To create a new journal entry for a specific project:

`$ journal --type project`


- To view your journal entries for a specific project:

`$ journal show --type project`

