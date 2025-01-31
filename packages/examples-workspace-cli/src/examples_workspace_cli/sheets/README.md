# `sheets` - Google Sheets API example

## Table of Contents <!-- omit in toc -->

- [`sheets` - Google Sheets API example](#sheets---google-sheets-api-example)
  - [examples](#examples)
    - [`quickstart`](#quickstart)
    - [`simple`](#simple)
    - [`gspread`](#gspread)

## examples

### `quickstart`

- [Python quickstart - Google](https://developers.google.com/sheets/api/quickstart/python?hl=ja)
- [quickstart - Github](https://github.com/googleworkspace/python-samples/tree/main/sheets/quickstart)

Need a `credentials.json` file in the current directory.

```shell
examples-workspace-cli sheets quickstart
```

### `simple`

These are examples of simple CRUD operations.

This command requires these scopes:

- <https://www.googleapis.com/auth/drive.file>
- <https://www.googleapis.com/auth/spreadsheets>

Create a new spreadsheet file in Drive:  
After creating it, retrieve file information using the Sheet API.

```shell
examples-workspace-cli -A user sheets simple create -t pythonで作成したスプレッドシート -d {directory id}
```

Appends a new sheet to the specified file:

```shell
examples-workspace-cli -A user sheets simple add {file id}
```

Write some data to the sheet:

```shell
examples-workspace-cli -A user sheets simple write {file id}
```

Read some data from a sheet:

```shell
examples-workspace-cli -A user sheets simple read {file id}
```

Finally, delete the file.

```shell
examples-workspace-cli -A user sheets simple delete {file id}
```

`--force` will permanently delete the file from the trash.

```shell
examples-workspace-cli -A user sheets simple delete {file id} -f
```

### `gspread`

CRUD example using the gspread library.

- [gspread](https://docs.gspread.org/en/v6.0.0/index.html)

This command requires these scopes:

- <https://www.googleapis.com/auth/drive>
- <https://www.googleapis.com/auth/spreadsheets>

Create a new spreadsheet file in Drive:  

```shell
examples-workspace-cli -A user sheets gspread create -t gspreadで作成したスプレッドシート -d {directory id}
```

Appends a new sheet to the specified file:

```shell
examples-workspace-cli -A user sheets gspread add -n シート2 {file id}
```

Write some data to the sheet:

```shell
examples-workspace-cli -A user sheets gspread write {file id}
```

Read some data from a sheet:

```shell
examples-workspace-cli -A user sheets gspread read {file id}
```

Finally, delete the file.

```shell
examples-workspace-cli -A user sheets gspread delete {file id}
```

`--force` will permanently delete the file from the trash.

```shell
examples-workspace-cli -A user sheets gspread delete {file id} -f
```
