<style>@import url("//readme.codeadam.ca/readme.css");</style>

## Process

This applciation includes a handful of tools to work with the LEGO® colour palette:

1. A colour directory including colour names and a sample colour.
2. A colour profile page including name, sample, alternative names, links to colours on other websites, and a sample brick, and other data.
3. A tool to enter a colour into a textbox and convert it to the closet LEGO® colour.

There is no backend for this project. All backend functionality in completed by running the import script. Once deployed, this script will run once a month using [CRON](https://en.wikipedia.org/wiki/Cron).

### Completed by Instructor

The [colours-v2](https://github.com/BrickMMO/colours-v2) includes a basic PHP core also used in [flow-v1](https://github.com/BrickMMO/flow-v2) and [stop-start-continue-v1](https://github.com/BrickMMO/stop-start-continue-v1).

There are two tables names `colours`:

```sql
CREATE TABLE `colours` (
  `id` int(11) NOT NULL,
  `name` varchar(255) DEFAULT NULL,
  `rgb` varchar(255) DEFAULT NULL,
  `is_trans` enum('yes','no') DEFAULT NULL,
  `rebrickable_id` int(11) NOT NULL,
  `created_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `updated_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

And externals:

```sql
CREATE TABLE `externals` (
  `id` int(11) NOT NULL,
  `name` varchar(255) DEFAULT NULL,
  `source` enum('brickowl','bricklink','ldraw','lego','peeron') DEFAULT NULL,
  `external_id` int(11) NOT NULL,
  `colour_id` int(11) NOT NULL,
  `created_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `updated_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```

There is an import script that imports a list of colours from the [Rebrickable API](https://rebrickable.com/api/v3/docs/) into the `colours` and `externals` tables. This file is located at `/import.php`.

There is a home page named `index.php` that displays a list of the colours from the `colours` table.

### Steps

1. **Design**